# Complete Setup Guide: Building Your GitHub Portfolio with Cisco ISE Project

## 📚 Table of Contents
1. [Overview](#overview)
2. [Prerequisites](#prerequisites)
3. [Step-by-Step Instructions](#step-by-step-instructions)
4. [How to Use This Portfolio](#how-to-use-this-portfolio)
5. [Next Steps](#next-steps)

---

## Overview

This guide walks you through creating a professional GitHub portfolio showcasing a Cisco ISE (Identity Services Engine) deployment project. By following these steps, you'll have a portfolio ready to share with recruiters and hiring managers.

**What You'll Build:**
- Professional GitHub repository
- 191-line technical documentation (README)
- Organized folder structure for screenshots, docs, and configs
- Live demo access to Cisco ISE environment

**Time Required:** 2-3 hours

---

## Prerequisites

### Required Accounts
1. **GitHub Account**
   - Create at: https://github.com/signup
   - Free account is sufficient

2. **Cisco.com Account** (for dCloud lab access)
   - Create at: https://identity.cisco.com/register
   - Free account

### Required Knowledge
- Basic understanding of network security concepts
- Familiarity with GitHub (we'll guide you through)
- Understanding of Cisco ISE concepts (or willingness to learn)

---

## Step-by-Step Instructions

### PHASE 1: Create GitHub Repository

#### Step 1: Log into GitHub
1. Go to https://github.com
2. Click "Sign in" (top right)
3. Enter your credentials

#### Step 2: Create New Repository
1. Click the "+" icon (top right)
2. Select "New repository"
3. Fill in details:
   - **Repository name**: `cisco-ise-deployment`
   - **Description**: "Enterprise Cisco ISE deployment project - 802.1X authentication, guest access, device profiling, and network segmentation"
   - **Visibility**: Select "Public"
   - **Initialize**: Check ✅ "Add a README file"
4. Click "Create repository"

✅ **Result:** You now have an empty repository!

---

### PHASE 2: Write Professional README

#### Step 3: Edit README File
1. In your new repository, click on "README.md"
2. Click the pencil icon (✏️) to edit
3. Delete the default content
4. Copy and paste the complete README content (provided separately or from template)

**README Structure (191 lines):**
```
# Cisco ISE Deployment Project

## Overview
[Project description]

## Project Scope
### Business Requirements
### Technical Objectives

## Architecture
### ISE Deployment Model
### Network Integration

## Key Features Implemented
1. 802.1X Authentication
2. MAC Authentication Bypass (MAB)
3. Guest Access
4. Device Profiling
5. TrustSec Security Group Tagging
6. Compliance and Posture Assessment

## Authentication Flow
[Diagram]

## Technologies Used

## Configuration Highlights

## Challenges & Solutions

## Results & Outcomes

## Monitoring & Reporting

## Future Enhancements

## Skills Demonstrated

## Documentation

## Contact
```

5. Scroll down and click "Commit changes"
6. Add commit message: "Update README.md with ISE deployment documentation"
7. Click "Commit changes" (green button)

✅ **Result:** Professional documentation is now live!

---

### PHASE 3: Create Folder Structure

#### Step 4: Create `screenshots` Folder
1. In your repository main page, click "Add file" → "Create new file"
2. In the filename field, type: `screenshots/.gitkeep`
3. Click "Commit changes"
4. Add commit message: "Add screenshots folder for ISE demo screenshots"
5. Click "Commit changes"

✅ **Result:** screenshots/ folder created!

#### Step 5: Create `docs` Folder
1. Click "Add file" → "Create new file"
2. Type: `docs/.gitkeep`
3. Commit with message: "Add docs folder for deployment guides and documentation"

✅ **Result:** docs/ folder created!

#### Step 6: Create `configs` Folder
1. Click "Add file" → "Create new file"
2. Type: `configs/.gitkeep`
3. Commit with message: "Add configs folder for ISE configuration exports"

✅ **Result:** configs/ folder created!

**Your repository now has:**
```
cisco-ise-deployment/
├── README.md
├── screenshots/
├── docs/
└── configs/
```

---

### PHASE 4: Access Cisco ISE Demo Lab

#### Step 7: Access Cisco dCloud
1. Go to: https://dcloud.cisco.com
2. Log in with your Cisco.com credentials
3. Select your region (choose closest: US-East, US-West, Europe, Asia-Pacific)

#### Step 8: Find ISE Demo
1. In the dCloud catalog, search for "ISE" or "Identity Services Engine"
2. Look for: **"Explore Cisco Identity Services Engine"** or **"ISE 3.5"**
3. Click on the demo

#### Step 9: Launch Instant Demo
1. Click "Explore" button
2. Select **ISE 3.5** (latest version)
3. Click "Try It"
4. Wait 1-2 minutes for lab to provision

✅ **Result:** You're now in a live ISE environment!

---

### PHASE 5: Explore ISE Environment

#### Step 10: Navigate ISE Dashboard
Once logged in, explore these key sections:

1. **Dashboard (Home)**
   - Shows total endpoints
   - Authentication summary
   - Quick links

2. **Policy → Policy Sets**
   - View configured policies:
     - MAC Based Authentication
     - Corporate Posture
     - MDM
     - Employee Access
     - Remote Access VPN
     - Default

3. **Operations → RADIUS → Live Logs**
   - See real-time authentication attempts
   - Green checkmarks = Success
   - Red X = Failed
   - Blue icon = Info/Warning

4. **Administration → System → Deployment**
   - View ISE node architecture
   - See Primary/Secondary PAN
   - Policy Service Nodes (PSN)

✅ **Result:** You understand ISE components!

---

### PHASE 6: Take Screenshots for Portfolio

#### Step 11: Capture ISE Screenshots
**Take these 5 screenshots:**

1. **ISE Dashboard**
   - Show home page with endpoint count
   - Save as: `ise-dashboard.png`

2. **Policy Sets**
   - Show all 6 policy sets
   - Save as: `ise-policy-sets.png`

3. **RADIUS Live Logs**
   - Show authentication attempts (green/red status)
   - Save as: `ise-live-logs.png`

4. **ISE Deployment Architecture**
   - Show node topology
   - Save as: `ise-deployment.png`

5. **Context Visibility - Endpoints**
   - Show endpoint profiling
   - Save as: `ise-endpoints.png`

**How to take screenshots:**
- **Windows**: Press `Win + Shift + S` or use Snipping Tool
- **Mac**: Press `Cmd + Shift + 4`

✅ **Result:** You have 5 ISE screenshots!

---

### PHASE 7: Upload Screenshots to GitHub

#### Step 12: Upload Files
1. In your GitHub repository, navigate to `screenshots/` folder
2. Click "Add file" → "Upload files"
3. Drag and drop your 5 PNG screenshots
4. Add commit message: "Add ISE demo screenshots from dCloud lab"
5. Click "Commit changes"

✅ **Result:** Screenshots are now in your portfolio!

---

### PHASE 8: Finalize Portfolio

#### Step 13: Update README with Screenshot References
1. Edit README.md
2. Find the "Documentation" section
3. Update to reference your screenshots:
```markdown
## Documentation

- Network topology diagrams (in `/diagrams` folder)
- ISE policy configuration exports (in `/configs` folder)  
- Deployment runbook and troubleshooting guide (in `/docs` folder)
- ISE demo screenshots (in `/screenshots` folder):
  - Dashboard overview
  - Policy Sets configuration
  - RADIUS Live Logs
  - Deployment architecture
  - Endpoint profiling
```

#### Step 14: Update Contact Information
1. Find the "Contact" section in README
2. Replace placeholder LinkedIn URL with your actual profile:
```markdown
## Contact

For questions about this project, feel free to reach out via 
[LinkedIn](https://www.linkedin.com/in/YOUR-PROFILE) or email.
```

✅ **Result:** Portfolio is complete and professional!

---

## How to Use This Portfolio

### In Your Resume
Add under "Projects" or "Technical Portfolio":
```
GitHub Portfolio: github.com/YOUR-USERNAME/cisco-ise-deployment
- Enterprise Cisco ISE deployment with distributed architecture
- 802.1X authentication, device profiling, and TrustSec segmentation  
- Comprehensive documentation with architecture diagrams
```

### In LinkedIn
Add to "Featured" section or "About":
```
Check out my technical portfolio documenting enterprise network security 
projects: github.com/YOUR-USERNAME/cisco-ise-deployment
```

### In Job Applications
When application asks for portfolio/GitHub:
```
https://github.com/YOUR-USERNAME/cisco-ise-deployment
```

### In Interviews
When asked about ISE experience:
```
"I've documented a complete ISE deployment in my GitHub portfolio. It covers 
distributed architecture, 802.1X authentication with multiple EAP methods, 
device profiling, guest access, and TrustSec segmentation. I also have hands-on 
experience from Cisco dCloud labs. I can walk you through the architecture if 
you'd like."
```

---

## Next Steps

### Immediate Actions (This Week)
1. ✅ Share portfolio link on LinkedIn
2. ✅ Update resume with portfolio URL
3. ✅ Apply to networking/security jobs with portfolio link

### Short-Term (Next 2 Weeks)
4. Create second portfolio project:
   - Enterprise Wi-Fi Design (for wireless roles)
   - ACI Data Center Migration (leveraging your Nexus/ACI experience)
   - Network Automation Scripts (Python/Ansible)

5. Practice interview talking points:
   - Explain ISE architecture
   - Describe authentication flow
   - Discuss policy design decisions
   - Troubleshooting scenarios

### Long-Term (This Month)
6. Build 3-5 portfolio projects total
7. Add blog posts explaining concepts
8. Contribute to open-source networking projects
9. Create video walkthrough of your portfolio

---

## Troubleshooting Common Issues

### Issue 1: Can't Access dCloud
**Solution:** Ensure you have a Cisco.com account. Some demos require partner access level. Use "Instant Demo" versions which are publicly available.

### Issue 2: GitHub Folder Not Creating
**Solution:** You must add a file inside the folder (like `.gitkeep`) for GitHub to create it. Empty folders aren't tracked by Git.

### Issue 3: README Not Formatting Correctly
**Solution:** Ensure you're using Markdown syntax correctly:
- Use `#` for headings
- Use `-` for bullet points
- Use ``` for code blocks

### Issue 4: ISE Lab Session Expired
**Solution:** dCloud sessions typically last 2-4 hours. Schedule a new session or use "Instant Demo" for immediate access.

---

## Additional Resources

### Cisco ISE Learning
- Cisco ISE Documentation: https://cisco.com/go/ise
- Cisco dCloud: https://dcloud.cisco.com
- Network Node (ISE Blog): http://www.network-node.com/

### GitHub Learning  
- GitHub Docs: https://docs.github.com
- Markdown Guide: https://www.markdownguide.org/

### Portfolio Examples
- Awesome GitHub Profile: https://github.com/abhisheknaiidu/awesome-github-profile-readme

---

## Summary Checklist

Use this checklist to track your progress:

- [ ] Created GitHub account
- [ ] Created Cisco.com account  
- [ ] Created `cisco-ise-deployment` repository
- [ ] Added professional README (191 lines)
- [ ] Created `screenshots/` folder
- [ ] Created `docs/` folder
- [ ] Created `configs/` folder
- [ ] Accessed Cisco dCloud
- [ ] Explored ISE demo environment
- [ ] Took 5 ISE screenshots
- [ ] Uploaded screenshots to GitHub
- [ ] Updated README with LinkedIn URL
- [ ] Added portfolio to resume
- [ ] Shared portfolio on LinkedIn
- [ ] Applied to jobs with portfolio link

---

## Questions?

If you have questions or need clarification on any step, refer back to this guide or:
1. Review the main README.md in the repository
2. Check GitHub documentation
3. Explore additional Cisco dCloud demos
4. Practice explaining the project to yourself

---

**Congratulations! You've built a professional portfolio that demonstrates enterprise network security expertise. This will significantly improve your chances in job applications and interviews.**

**Repository URL to share:**  
`https://github.com/YOUR-USERNAME/cisco-ise-deployment`

---

*Last Updated: January 14, 2026*
