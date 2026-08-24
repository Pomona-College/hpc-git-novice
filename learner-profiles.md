---
title: Learner Profiles
---

## Who Should Take This Workshop?

This workshop is designed for researchers learning version control with Git for the first time. Below are three representative learner profiles. Do you see yourself in one of these?

---

## Profile 1: Marcus - Chemistry Student Losing Track of Versions

### Background
Marcus is a senior chemistry major at Pomona working on his honors thesis. He's been writing analysis code and data processing scripts for two years, but his file system looks like: `analysis_final.py`, `analysis_final_v2.py`, `analysis_final_REAL.py`, `analysis_final_actually_works.py`. He keeps losing track of which version is current, and accidentally uses old code. His advisor mentioned he should "use Git" but he has no idea what that means.

### What He Knows
- Comfortable writing and editing Python code
- Uses Unix shell (from previous workshop)
- Familiar with basic file organization
- No experience with version control
- Vaguely knows Git exists but thinks it's only for software developers

### Why He Needs This
- Multiple versions of code create confusion and errors
- Thesis deadline is approaching; can't afford to lose work
- Collaborators want to contribute code; can't easily share versions
- Wants to track *why* he made changes to analysis
- Lab is adopting Git for reproducible research

### His Goals
- Stop the `analysis_final_v5_actually_final.py` madness
- Track changes and know why he made them
- Work safely knowing previous versions are saved
- Eventually collaborate with lab members
- Have a clean, professional code repository

### Challenges He'll Face
- Git concepts (staging, commits, branches) are abstract
- Might not understand why you can't just use Dropbox
- Commands like `git checkout` might seem destructive
- Confusion between local and remote repositories
- Fear that he'll lose his work with one command

### Success Indicator
After this workshop, Marcus can:
- Initialize a Git repository for his thesis code
- Make meaningful commits with clear messages
- See the history of his changes over time
- Recover previous versions if needed
- Prepare to push code to GitHub

---

## Profile 2: Yuki - Computer Science Student, Currently Using Dropbox

### Background
Yuki is a junior double major in computer science and environmental science at Pomona. She's used cloud storage (Dropbox, Google Drive) to manage her project files and share code with classmates. This works okay for small projects, but she's starting a senior capstone on environmental data analysis and the team is struggling: multiple people editing the same files, unclear who changed what, and broken code when someone uploads a conflicting version.

### What She Knows
- Proficient programmer (several CS courses)
- Understands basic coding practices and style
- Uses cloud storage extensively
- Has never used version control
- Knows version control is "important" but hasn't felt the need
- High technical aptitude

### Why She Needs This
- Team capstone needs proper collaboration
- Cloud storage is not adequate for code collaboration
- CS internship expectations likely include Git knowledge
- Capstone repo could be portfolio piece for graduate school
- Wants to learn "how professionals do it"

### Her Goals
- Understand why Git is better than Dropbox for code
- Manage team contributions without conflicts
- Create a portfolio-ready GitHub repository
- Learn industry-standard workflows
- Be prepared for technical internships/grad school

### Challenges She'll Face
- Might not understand why version control is needed ("Dropbox works!")
- Might want to jump to advanced features too quickly
- Could over-engineer the workflow for a simple project
- Confusion between merge conflicts and broken code
- Temptation to skip good commit practices

### Success Indicator
After this workshop, Yuki can:
- Create a collaborative Git repository
- Resolve simple merge conflicts
- Write clear, meaningful commit messages
- Use branching for feature development
- Guide her capstone team through Git workflow

---

## Profile 3: Dr. Susan - Faculty Member Wanting Reproducible Research

### Background
Dr. Susan is an associate professor of neuroscience at Pomona. She runs a research lab with undergraduates and has published several papers, but she's concerned about reproducibility. Her papers describe analysis code verbally, and various versions of scripts exist across lab members' computers. When she wants to revisit an analysis, it's hard to find the exact version used. She's read about open science and wants her lab to adopt better practices.

### What She Knows
- Experienced scientist with strong research background
- Has written or edited code (R scripts, Python notebooks)
- Limited command line experience
- Never used formal version control
- Understands research reproducibility is important
- Aware that Git is an "industry standard"

### Why She Needs This
- Grant agencies increasingly require open, reproducible research
- Wants to publish analysis code alongside papers
- Lab collaboration is haphazard; Git would impose structure
- Needs to track which code produced which published results
- Setting example for lab members and students

### Her Goals
- Establish reproducible research practices for the lab
- Understand what version control is and why it matters
- Know how to advise students/postdocs on Git use
- Be able to discuss open science with peers
- Create clean, documented code archives with publications

### Challenges She'll Face
- Limited time; learning Git competes with research demands
- Might feel intimidated by command line
- Unclear how Git fits into her lab workflow
- Frustrated if Git concepts seem unnecessarily complex
- Worry about setting a "bad example" if she struggles

### Success Indicator
After this workshop, Dr. Susan can:
- Understand core Git concepts and terminology
- Create and maintain a lab repository
- Advise students on good Git practices
- Archive analysis code with publications
- Discuss reproducibility and open science with confidence

---

## Using These Profiles

**During teaching:**
- Reference Marcus when discussing why version control is needed: "Like Marcus with his analysis scripts..."
- Use Yuki's experience for collaboration examples: "When your capstone team wants to..."
- Draw on Dr. Susan's perspective for reproducibility: "For published research, we need..."

**When explaining concepts:**
- Connect staging/commits to research workflows
- Use real Pomona research examples for repositories
- Show how Git enables collaborative science

**For pacing:**
- Marcus needs reassurance about safety and clarity
- Yuki might want advanced topics but shouldn't skip foundations
- Dr. Susan appreciates "why" explanations over command syntax

---

## Common Threads

Despite different backgrounds, all three learners share:

1. **File chaos**: All struggling with multiple versions
2. **Collaboration concerns**: Need to work with others safely
3. **New to Git**: No prior version control experience
4. **Real motivation**: Each has concrete projects to organize
5. **Skepticism to overcome**: "Do I really need this?"

## Teaching to Diverse Learner Types

### What Works Well

- **Concrete scenarios**: Show how Git prevents the problems they're facing
- **Dropbox comparison**: Yuki and Marcus understand this; Dr. Susan appreciates the context
- **Live demonstration**: Show a messy repository, then show how Git solves it
- **Team simulation**: Have them practice collaboration in class
- **Reproducibility focus**: Connect to research integrity (resonates with Dr. Susan)
- **Real Pomona examples**: Show published research with clean Git repos

### Pacing Tips

- **For practical learners like Marcus**: Show immediate benefits ("Now you can find your old code")
- **For ambitious learners like Yuki**: Provide branch exercises, merge practice
- **For leadership-minded learners like Dr. Susan**: Discuss team practices and mentoring
- **For all**: Celebrate milestones ("Your first commit!", "Resolved a conflict!")

---

## After the Workshop

These learners won't be Git experts, but they will:

- Understand why version control matters
- Create and maintain a basic repository
- Make meaningful commits
- Navigate a remote repository (GitHub)
- Know where to learn more

Many will return for:
- **Intermediate Git** (branches, workflows, collaboration)
- **GitHub for Open Science** (publishing and archiving)
- **Workshop 0: Introduction to HPC** (Git is used in job submission)

Your role is to convince them that the initial effort pays off in peace of mind and professional practice.

---

## Real-World Connection

After this workshop, learners can:

- Start their own projects on GitHub
- Contribute to open-source software
- Archive and publish their own research
- Collaborate without fear of losing work
- Follow best practices expected in industry and academia
