# Professional Git Workflows - Class Materials

**Duration:** 3 hours  
**Audience:** Developers with basic Git/GitHub knowledge  
**Focus:** Production-ready workflows, code reviews, merge conflicts, security  
**Format:** Lecture + Breakout exercises + Individual GitHub Classroom assignment

---

## 🎯 What Students Will Learn

By the end of this session, students will be able to:
- Design custom Git workflows that fit their team's needs
- Write professional pull requests and provide constructive code reviews
- Resolve merge conflicts systematically and safely
- Implement security best practices and catch common vulnerabilities
- Set up automated quality gates with branch protection and hooks
- Handle Git disasters and recovery scenarios
- Use advanced GitHub features for team coordination

---

## 📚 Class Structure & Materials

### 1. GitHub Classroom Assignment (Individual Work)
**File:** `github_classroom_assignment.md`

**What Students Do:**
- Receive individual GitHub repository with vulnerable Python Flask API
- Transform basic code into secure, professionally configured repository
- Complete 4 parts: Repository Setup, Code Review, Merge Conflicts, Crisis Management
- Work individually but collaborate during breakout sessions

**Instructor Setup:**
- Create GitHub Classroom assignment using `starter-code-simple/` 
- Students get their own copy to work on
- Due 1 week after class (started in class, finished at home)

### 2. Starter Code for Students
**Directory:** `starter-code-simple/`

**Contains:**
- `app.py` - Basic Flask API with intentional security vulnerabilities
- `requirements.txt` - Python dependencies
- `README.md` - Setup instructions and assignment overview

**Vulnerabilities Included for Learning:**
- Hardcoded API keys and database passwords
- SQL injection vulnerabilities
- Weak MD5 password hashing
- Missing input validation
- Insecure logging of sensitive data

### 3. Breakout Exercises (15 minutes each)
**Directory:** `breakout-exercises/`

Students work individually on their GitHub Classroom assignment while discussing with teammates:

**Exercise 1: Code Review Practice**
- File: `code_review_exercise.md`
- Task: Find security vulnerabilities in Python authentication code
- Skills: Professional code review comments, security awareness

**Exercise 2: Merge Conflict Resolution**  
- File: `merge_conflict_exercise.md`
- Task: Intelligently combine authentication + database features
- Skills: Smart conflict resolution, preserving functionality

**Exercise 3: Crisis Management**
- File: `crisis_management_exercise.md`  
- Task: Respond to API key leak emergency
- Skills: Incident response, Git recovery commands

### 4. Instructor Materials
**File:** `instructor_guide.md`

**Contains:**
- Detailed class timeline (matches original lesson plan exactly)
- Setup instructions for GitHub Classroom
- Common student challenges and solutions
- Assessment criteria and success indicators
- Resources for continued learning

---

## 🚀 Quick Start for Instructors

### Before Class:
1. **Set up GitHub Classroom:**
   - Create new assignment
   - Upload contents of `starter-code-simple/` as template
   - Test that students can access and run the code

2. **Prepare Materials:**
   - Review `instructor_guide.md` for timeline
   - Print or bookmark breakout exercise files
   - Test all starter code runs correctly

3. **Plan Breakout Rooms:**
   - 3-4 students per room
   - Mixed experience levels if possible
   - Assign rooms for efficient management

### During Class:
1. **Follow Original Lesson Plan Structure:**
   - 6:30-6:45: Opening and assignment overview
   - 6:45-7:05: Workflows and standards lecture
   - 7:05-7:20: Pull request mastery lecture
   - 7:20-7:35: **Breakout 1** - Code review exercise
   - 7:35-7:55: Merge conflicts lecture
   - 7:55-8:05: Break
   - 8:05-8:20: **Breakout 2** - Merge conflict exercise
   - 8:20-8:40: Git recovery and crisis management lecture
   - 8:40-8:55: **Breakout 3** - Crisis management exercise
   - 8:55-9:10: Quality gates and automation lecture
   - 9:10-9:25: Repository setup workshop
   - 9:25-9:30: Wrap-up and next steps

2. **Manage Breakout Sessions:**
   - Students work on their individual GitHub repos
   - Teams discuss approaches and help each other
   - Visit rooms to answer questions and check progress

### After Class:
- Students complete their repositories and documentation
- Grade individual GitHub Classroom submissions
- Provide feedback on professional Git skills demonstrated

---

## 💡 Key Teaching Points

### Professional Standards Focus:
- **Security First:** Every exercise emphasizes catching vulnerabilities
- **Real-World Skills:** Direct application to professional development
- **Team Collaboration:** Balances individual work with team learning
- **Crisis Preparedness:** Practice handling real Git disasters

### Python-Specific Elements:
- Security vulnerabilities common in Python web applications
- Tools like `bandit` for Python security scanning
- Flask API scenarios students will recognize
- Pre-commit hooks configured for Python projects

### Immediate Applicability:
- Students can implement these workflows at work Monday
- Skills directly prevent security breaches and Git disasters
- Professional code review practices improve team productivity
- Crisis management procedures protect production systems

---

## ✅ Success Criteria

### During Class:
- [ ] Students actively finding security vulnerabilities
- [ ] Teams helping each other understand Git concepts
- [ ] Professional discussion about real-world applications
- [ ] Confident use of Git recovery commands

### Assignment Completion:
- [ ] Repositories have working branch protection and security scanning
- [ ] Professional-quality code review comments
- [ ] Intelligent merge conflict resolutions
- [ ] Documented incident response procedures

### Long-Term Impact:
- [ ] Students report using skills in their actual work
- [ ] Increased confidence with advanced Git workflows
- [ ] Better security awareness in their projects
- [ ] Ability to handle Git crises systematically

---

## 📂 File Organization

```
github-workflows/
├── README.md                           # This overview file
├── github_classroom_assignment.md      # Student assignment instructions
├── instructor_guide.md                 # Detailed instructor timeline
├── starter-code-simple/               # GitHub Classroom template
│   ├── app.py                         # Flask API with vulnerabilities
│   ├── requirements.txt               # Python dependencies
│   └── README.md                      # Student setup instructions
└── breakout-exercises/                # 15-minute team exercises
    ├── code_review_exercise.md        # Security vulnerability hunting
    ├── merge_conflict_exercise.md     # Intelligent conflict resolution
    └── crisis_management_exercise.md  # Git disaster response
```

---

## 🎓 Alignment with Learning Objectives

This class structure directly develops the skills outlined in the original lesson plan:

**Custom Git Workflows** → Repository setup exercise with branch protection  
**Professional Code Reviews** → Code review exercise with security focus  
**Merge Conflict Resolution** → Hands-on conflict exercise with real scenarios  
**Security Best Practices** → Vulnerability hunting throughout all exercises  
**Quality Gates & Automation** → GitHub Actions and pre-commit hook setup  
**Git Disaster Recovery** → Crisis management exercise with time pressure  
**Team Coordination** → Breakout collaboration while maintaining individual accountability

Students leave with immediately applicable professional Git skills that protect production systems and improve team productivity.