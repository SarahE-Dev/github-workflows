# Instructor Guide: Professional Git Workflows Class

**Duration:** 3 hours  
**Format:** Lecture + Breakout Exercises + Individual GitHub Classroom Assignment  
**Alignment:** Matches original lesson plan timing and content

---

## Class Structure Overview

### Opening (15 minutes) - 6:30-6:45
- Git horror stories and today's mission
- Review GitHub Classroom assignment structure
- Team assignments for breakout collaboration

### Lecture: Workflows & Standards (20 minutes) - 6:45-7:05  
- Custom workflows and professional standards
- Branch naming and commit message conventions
- Team exercise: design your workflow

### Lecture: Pull Request Mastery (15 minutes) - 7:05-7:20
- Professional PR examples
- Code review focus areas and comment examples

### Breakout 1: Code Review Practice (15 minutes) - 7:20-7:35
**Exercise:** Review Python authentication code for security issues  
**Individual work** on GitHub Classroom assignment with **team discussion**

### Lecture: Merge Conflicts (20 minutes) - 7:35-7:55
- Understanding conflict types
- Systematic resolution process
- Complex conflict scenarios

### Break (10 minutes) - 7:55-8:05

### Breakout 2: Merge Conflict Resolution (15 minutes) - 8:05-8:20
**Exercise:** Combine authentication + database features intelligently  
**Individual work** with **team support**

### Lecture: Git Recovery & Crisis Management (20 minutes) - 8:20-8:40
- Common disasters and quick fixes
- Git recovery toolkit
- Real-world crisis scenarios

### Breakout 3: Crisis Management (15 minutes) - 8:40-8:55
**Exercise:** Respond to API key leak scenario  
**Individual work** with **team discussion**

### Lecture: Quality Gates & Automation (15 minutes) - 8:55-9:10
- Branch protection setup
- Pre-commit hooks for security
- GitHub Actions for quality

### Workshop: Professional Repository Setup (15 minutes) - 9:10-9:25
**Exercise:** Configure security measures and automation  
**Individual GitHub Classroom work**

### Wrap-up & Next Steps (5 minutes) - 9:25-9:30

---

## GitHub Classroom Setup

### Before Class:
1. **Create GitHub Classroom assignment** with starter code
2. **Distribute assignment links** to students
3. **Test all starter code** works without errors
4. **Prepare breakout room assignments** (3-4 students each)

### Starter Materials:
- **Simple Python Flask API** (`starter-code-simple/`)
- **Basic requirements.txt**
- **README with setup instructions**
- **Intentional security vulnerabilities** for learning

---

## Breakout Exercise Management

### Breakout 1: Code Review (15 min)
**Materials:** `breakout-exercises/code_review_exercise.md`

**Individual Task:** Find security vulnerabilities, write professional review comments  
**Team Discussion:** Share findings, discuss review quality

**Instructor Role:**
- Visit each breakout room briefly
- Check students are finding major security issues
- Help with technical questions about vulnerabilities

### Breakout 2: Merge Conflicts (15 min)  
**Materials:** `breakout-exercises/merge_conflict_exercise.md`

**Individual Task:** Merge authentication + database branches intelligently  
**Team Support:** Help each other understand both branches

**Instructor Role:**
- Ensure students understand both branches' features
- Check they're combining (not just picking one side)
- Help with Git command syntax if needed

### Breakout 3: Crisis Management (15 min)
**Materials:** `breakout-exercises/crisis_management_exercise.md`

**Individual Task:** Respond to API key leak emergency  
**Team Discussion:** Compare response strategies

**Instructor Role:**
- Emphasize credential rotation as first step
- Check understanding of Git recovery commands
- Share real-world incident examples

---

## Assessment Approach

### Individual GitHub Classroom Assignment:
- **Repository setup and security** (40 points)
- **Code review mastery** (25 points) 
- **Merge conflict resolution** (20 points)
- **Git crisis management** (15 points)

### In-Class Participation:
- Active participation in breakout discussions
- Quality of questions and insights shared
- Helping team members learn

### Take-Home Completion:
- Final repository setup and documentation
- Written reports on code review and conflict resolution
- Due 1 week after class

---

## Common Student Challenges

### Technical Issues:
**"GitHub Classroom link not working"**
- Have backup: students can fork from public repo
- Help with GitHub authentication issues

**"Starter code won't run"**  
- Check Python version and virtual environment
- Verify Flask installation

### Learning Challenges:
**"Can't find security vulnerabilities"**
- Guide to look for hardcoded passwords, SQL injection
- Show one example, let them find rest

**"Merge conflict too confusing"**
- Help them understand what each branch does first
- Show how to test small changes

**"Git commands are scary"**
- Emphasize `git status` to see current state
- Show recovery commands are safer than they think

---

## Key Learning Moments

### Professional Standards:
- **Branch naming:** Help students see value of descriptive names
- **Commit messages:** Show how conventional commits enable automation
- **Code reviews:** Practice constructive, specific feedback

### Security Awareness:
- **Real vulnerabilities:** Use actual CVE examples
- **Impact stories:** Share real-world breach consequences  
- **Prevention mindset:** Security as everyone's responsibility

### Team Collaboration:
- **Conflict resolution:** Combining vs. choosing
- **Crisis response:** Systematic approach under pressure
- **Professional communication:** Clear, helpful, respectful

---

## Success Indicators

### During Class:
- Students actively discussing security issues found
- Teams helping each other with technical challenges
- Questions show understanding of professional workflows

### Assignment Quality:
- Repositories have working security measures
- Code review comments are specific and actionable
- Merge resolutions preserve functionality from both branches
- Crisis response follows systematic approach

### Long-term Impact:
- Students report using skills at work
- Increased confidence with Git workflows
- Better security awareness in their projects

---

## Resources for Students

### Immediate:
- [Git Documentation](https://git-scm.com/doc)
- [Interactive Git Tutorial](https://learngitbranching.js.org/)
- [OWASP Python Security](https://owasp.org/www-project-python-security/)

### Continued Learning:
- [GitHub Skills](https://skills.github.com)
- [Python Security Best Practices](https://python-security.readthedocs.io/)
- [Professional Git Workflows](https://www.atlassian.com/git/tutorials/comparing-workflows)

This simplified approach maintains the professional focus while making it manageable for both students and instructor, with clear alignment to your original lesson plan structure.