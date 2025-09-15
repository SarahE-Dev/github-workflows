# Merge Conflict Exercise - In-Class Breakout

**Duration:** 15 minutes  
**Format:** Individual work with team support  
**Objective:** Practice intelligent merge conflict resolution

---

## Scenario Setup

Two developers worked on the same Python API file simultaneously:

**Branch A (Authentication):** Added login validation and JWT tokens  
**Branch B (Database):** Added database integration and user persistence

You need to merge both branches intelligently, preserving the best of both features.

---

## Branch A: Authentication Features

```python
from flask import Flask, request, jsonify
import jwt
import bcrypt
from datetime import datetime, timedelta

app = Flask(__name__)
app.config['SECRET_KEY'] = 'your-secret-key'

@app.route('/users', methods=['POST'])
def create_user():
    data = request.get_json()
    
    # Input validation added
    if not data.get('username') or len(data.get('username', '')) < 3:
        return jsonify({"error": "Username must be at least 3 characters"}), 400
    
    if not data.get('password') or len(data.get('password', '')) < 8:
        return jsonify({"error": "Password must be at least 8 characters"}), 400
    
    # Secure password hashing
    password_hash = bcrypt.hashpw(data['password'].encode('utf-8'), bcrypt.gensalt())
    
    return jsonify({
        "id": 1, 
        "username": data['username'],
        "message": "User created successfully"
    })

@app.route('/login', methods=['POST'])
def login():
    data = request.get_json()
    username = data.get('username')
    password = data.get('password')
    
    # Validate credentials (simplified for demo)
    if username and password:
        # Generate JWT token
        token = jwt.encode({
            'username': username,
            'exp': datetime.utcnow() + timedelta(hours=24)
        }, app.config['SECRET_KEY'])
        
        return jsonify({"token": token, "message": "Login successful"})
    
    return jsonify({"error": "Invalid credentials"}), 401
```

---

## Branch B: Database Features

```python
from flask import Flask, request, jsonify
from sqlalchemy import create_engine, Column, Integer, String
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy.orm import sessionmaker

app = Flask(__name__)

# Database setup
engine = create_engine('sqlite:///users.db')
Base = declarative_base()
Session = sessionmaker(bind=engine)

class User(Base):
    __tablename__ = 'users'
    id = Column(Integer, primary_key=True)
    username = Column(String(50), unique=True, nullable=False)
    password = Column(String(100), nullable=False)

Base.metadata.create_all(engine)

@app.route('/users', methods=['GET'])
def get_users():
    session = Session()
    users = session.query(User).all()
    result = [{"id": u.id, "username": u.username} for u in users]
    session.close()
    return jsonify({"users": result})

@app.route('/users', methods=['POST'])
def create_user():
    data = request.get_json()
    session = Session()
    
    user = User(
        username=data.get('username'),
        password=data.get('password')  # This needs the secure hashing from Branch A!
    )
    
    session.add(user)
    session.commit()
    
    result = {"id": user.id, "username": user.username}
    session.close()
    return jsonify(result)
```

---

## Your Challenge (15 minutes)

### Step 1: Analyze Both Branches (3 minutes)
**What does each branch accomplish?**

**Branch A (Authentication):**
- Input validation for user creation
- Secure password hashing with bcrypt
- JWT token generation for login
- Proper error handling

**Branch B (Database):**
- SQLAlchemy ORM for data persistence  
- User model with database schema
- Get users endpoint
- Session management

### Step 2: Plan Your Integration (3 minutes)
**How will you combine these features?**

Your merged solution should:
- ✅ Use database persistence from Branch B
- ✅ Include input validation from Branch A
- ✅ Use secure password hashing from Branch A
- ✅ Have JWT authentication from Branch A
- ✅ Keep all endpoints working

### Step 3: Create the Merged Solution (7 minutes)

Write the intelligent merge that combines both features:

```python
# Your merged solution here
# Combine the best of both branches
```

### Step 4: Test Your Logic (2 minutes)
Walk through your merged code:
- Does user creation validate input AND save to database?
- Does password hashing work with database storage?
- Are all imports included?
- Do all endpoints still work?

---

## Discussion Questions (Team sharing)

1. **What was your strategy for combining the features?**
2. **What conflicts did you encounter and how did you resolve them?**
3. **What would you test to make sure your merge works?**
4. **How is this different from just "picking one side" of the conflict?**

---

## Expected Intelligent Solution

A good merge should:
1. **Combine imports** from both branches
2. **Use database models** with **secure password hashing**
3. **Include input validation** in the database-saving endpoint
4. **Preserve all functionality** from both branches
5. **Follow consistent patterns** throughout

---

## Real-World Application

This mirrors actual development scenarios:
- **Feature teams** often work on overlapping code
- **Good merges** preserve everyone's work
- **Smart resolution** is better than random conflict picking
- **Testing** your merge prevents broken deployments

The skills you practice here prevent the "it worked on my machine" problems that break production systems.