# Code Review Exercise - In-Class Breakout

**Duration:** 15 minutes  
**Format:** Individual work with team discussion  
**Objective:** Practice identifying security vulnerabilities and writing professional code review comments

---

## The Code to Review

You're reviewing this Python authentication code that has multiple security issues. Your job is to find them and provide professional feedback.

```python
# auth_system.py - Find the security issues
import requests
import sqlite3
import hashlib

# Issue 1: Hardcoded secrets
API_KEY = "sk-live-1234567890abcdef"
DATABASE_URL = "postgresql://admin:password123@localhost/prod"
DEBUG_MODE = True

def authenticate_user(username, password):
    # Issue 2: SQL injection vulnerability
    conn = sqlite3.connect("users.db")
    query = f"SELECT * FROM users WHERE username='{username}' AND password='{password}'"
    
    # Issue 3: No error handling
    result = conn.execute(query).fetchone()
    
    # Issue 4: Password in logs
    print(f"Login attempt: {username}:{password}")
    
    # Issue 5: API call without validation
    response = requests.post("https://api.auth.com/verify", 
                           data={"user": username, "key": API_KEY})
    
    # Issue 6: No status check
    return response.json()

def reset_password(user_id, new_password):
    # Issue 7: No input validation
    # Issue 8: Plain text password storage
    conn = sqlite3.connect("users.db")
    query = f"UPDATE users SET password='{new_password}' WHERE id={user_id}"
    conn.execute(query)
    conn.commit()
    
def hash_password(password):
    # Issue 9: Weak hashing algorithm
    return hashlib.md5(password.encode()).hexdigest()

def admin_check(user_id):
    # Issue 10: Hardcoded admin backdoor
    if user_id == 1 or user_id == "admin":
        return True
    return False
```

---

## Your Task (10 minutes individual work)

**Find and document at least 6 security issues** using this professional format:

```markdown
## Code Review Comments

**🔴 SECURITY: [Issue Type]**
**Line X:** [Specific problem description]
**Impact:** [What could go wrong if exploited]
**Suggestion:** 
```python
# Instead of this vulnerable code:
vulnerable_example()

# Use this secure approach:
secure_example()
```
**Priority:** Critical/High/Medium/Low
```

---

## Expected Issues (Instructor Reference)

1. **Hardcoded API Keys (Lines 6-8)** - Critical
2. **SQL Injection (Lines 12, 31)** - Critical  
3. **Password Logging (Line 17)** - High
4. **Weak MD5 Hashing (Line 35)** - High
5. **No Input Validation (Line 28)** - Medium
6. **Missing Error Handling (Line 15)** - Medium
7. **Insecure API Call (Line 20)** - Medium
8. **Admin Backdoor (Line 38)** - Critical
9. **Debug Mode in Production (Line 8)** - Low
10. **Plain Text Password Storage (Line 31)** - Critical

---

## Team Discussion (5 minutes)

**Share with your breakout room:**
1. Which issues did you find?
2. Which ones did you miss?
3. How would you prioritize fixing them?
4. What was challenging about writing professional review comments?

**Discussion Questions:**
- What makes a code review comment helpful vs. just critical?
- How do you balance being thorough with being constructive?
- What would you want to see in a review of your own code?

---

## Success Criteria

**Good Work:**
- Found 4-6 security issues
- Used professional, constructive language
- Provided specific suggestions for fixes

**Excellent Work:**
- Found 6+ security issues including subtle ones
- Provided code examples in suggestions
- Correctly prioritized issues by severity
- Comments would genuinely help improve code quality

---

## Real-World Application

These are the exact types of issues you'll encounter in professional code reviews:
- **Hardcoded secrets** appear in ~15% of repositories
- **SQL injection** remains a top security vulnerability
- **Weak password hashing** affects millions of users
- **Missing input validation** leads to data breaches

The review skills you practice here directly apply to protecting your team's production systems.