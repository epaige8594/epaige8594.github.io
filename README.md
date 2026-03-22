# epaige8594.github.io
# Emmitt Paige - Technical Writing Portfolio

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen)](https://epaige8594.github.io)
[![Jekyll](https://img.shields.io/badge/Jekyll-4.3-red)](https://jekyllrb.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A professional technical writing portfolio and document library built with **Jekyll**, **GitHub Pages**, and **custom CSS**. Features an interactive document reader, responsive design, and categorized documentation library with a modern dark blue/teal aesthetic.

🔗 **Live Site:** [https://epaige8594.github.io](https://epaige8594.github.io)

---

## 📚 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation--setup)
- [Running Locally](#running-locally)
- [Project Structure](#project-structure)
- [Customization Guide](#customization-guide)
- [Deployment](#deployment)
- [Troubleshooting](#troubleshooting)
- [License](#license)

---

## Overview

This portfolio site showcases technical writing samples, API documentation, cybersecurity runbooks, and policy documentation. Built with **documentation as code** principles, the site demonstrates proficiency in:

- Git/GitHub version control workflows
- Markdown content authoring
- Jekyll static site generation
- Custom CSS styling with dark blue/teal theme
- JavaScript interactive components

---

## Features

| Feature | Description |
|---------|-------------|
| **Interactive Document Library** | Click-to-load reader with categorized documents (Policy, Cybersecurity, API, Knowledge Base) |
| **Responsive Design** | Mobile-friendly navigation and layout adapt to any screen size |
| **Dropdown Navigation** | CSS-only dropdown menu with hover activation and smooth animations |
| **CSS Variables** | Centralized theming for easy color scheme modification (dark blue/teal theme) |
| **Jekyll Templating** | Reusable layouts and includes for maintainable code |
| **GitHub Pages Integration** | Automatic deployment on push to main branch |
| **Glass-morphism Effects** | Modern translucent card styling with backdrop blur |
| **Animated Background** | Subtle floating gradient animations |

---

## Technology Stack

| Technology | Purpose | Version |
|------------|---------|---------|
| **Jekyll** | Static site generator | 4.3.0+ |
| **GitHub Pages** | Hosting and deployment | Built-in |
| **Markdown** | Content authoring | CommonMark |
| **Liquid** | Jekyll templating language | 4.0.0+ |
| **HTML5/CSS3** | Structure and styling | - |
| **JavaScript** | Interactive document loading | ES6+ |
| **Git** | Version control | 2.x+ |

---

## Prerequisites

Before installing, ensure you have the following installed:

### Required Software

```bash
# Check Ruby version (2.5.0 or higher recommended)
ruby --version

# Check RubyGems
gem --version

# Check Git
git --version
Install Ruby (if not installed)

macOS:

bash
# Ruby comes pre-installed on macOS
# If needed, install via Homebrew
brew install ruby
Linux (Ubuntu/Debian):

bash
sudo apt update
sudo apt install ruby-full ruby-bundler build-essential
Windows:

Download and install Ruby+Devkit from rubyinstaller.org
Select "MSYS2" option during installation
Installation & Setup

1. Clone the Repository

bash
# Clone using HTTPS
git clone https://github.com/epaige8594/epaige8594.github.io.git

# Navigate into the project directory
cd epaige8594.github.io
2. Install Jekyll and Dependencies

bash
# Install bundler
gem install bundler

# Install project dependencies
bundle install
3. Verify Installation

bash
# Check Jekyll version
jekyll --version
Running Locally

Start the Local Development Server

bash
# Build and serve the site with auto-regeneration
bundle exec jekyll serve

# Or with specific port (default: 4000)
bundle exec jekyll serve --port 4000
View the Site

Open your browser and navigate to:

http://localhost:4000
Live Reload

The server automatically watches for file changes and rebuilds the site. Just refresh your browser to see updates.

Build Only (No Server)

bash
# Build the site to the _site directory
bundle exec jekyll build
Project Structure

text
epaige8594.github.io/
├── _config.yml              # Jekyll site configuration
├── _layouts/                # Page templates
│   └── tech.html            # Main layout with navigation and styling
├── assets/                  # Static assets
│   └── css/                 # Stylesheets
│       └── tech-style.css   # Main CSS file (dark blue/teal theme)
├── about/                   # About page
│   └── index.md             # About page content
├── portfolio/               # Portfolio section
│   └── index.md             # Document library main page (includes JavaScript)
├── index.md                 # Homepage
├── Gemfile                  # Ruby dependencies
└── README.md                # This file
Customization Guide

Changing Colors

Edit assets/css/tech-style.css and modify the CSS variables at the top of the file:

css
:root {
  --bg-dark: #0a1929;      /* Dark blue background */
  --bg-darker: #051321;     /* Darker blue for footer */
  --primary: #00e5ff;       /* Bright teal accent */
  --secondary: #00d4aa;     /* Green-teal accent */
  --accent: #00b8d4;        /* Medium teal accent */
  --text-light: #e3f2fd;    /* Light blue-white text */
  --text-gray: #90a4ae;     /* Gray text for secondary content */
  --card-bg: rgba(255, 255, 255, 0.08);  /* Semi-transparent card background */
}
Adding a New Document

Open portfolio/index.md
Locate the JavaScript documents object (around line 400)
Add a new entry:
javascript
'your-document-id': {
    title: 'Your Document Title',
    content: `# Document Title

## Section Header
Your content here with markdown formatting.
This supports headers, lists, and **bold text**.
- Bullet point 1
- Bullet point 2

### Subsection
Additional content here.`
}
Add a link to the left sidebar (in the appropriate category section):
html
<li style="margin-bottom: 0.5rem;">
    <a href="#" onclick="loadDocument('your-document-id'); return false;" 
       style="color: #90a4ae; text-decoration: none; display: block; padding: 0.5rem; border-radius: 5px; transition: all 0.3s;" 
       onmouseover="this.style.backgroundColor='rgba(0,229,255,0.1)'; this.style.color='#00e5ff';" 
       onmouseout="this.style.backgroundColor='transparent'; this.style.color='#90a4ae';">
        📄 Your Document Title
    </a>
</li>
Modifying Navigation

Edit _layouts/tech.html and update the <div class="nav-links"> section:

html
<div class="nav-links">
    <a href="/">Home</a>
    <a href="/about/">About</a>
    <div class="dropdown">
        <span class="dropbtn">Portfolio</span>
        <div class="dropdown-content">
            <a href="/portfolio/">All Work</a>
            <a href="/portfolio/#policy">📋 Policy & Governance</a>
            <a href="/portfolio/#cybersecurity">🛡️ Cybersecurity</a>
            <a href="/portfolio/#api">🔗 API Documentation</a>
            <a href="/portfolio/#knowledge-base">📚 Knowledge Base</a>
        </div>
    </div>
    <a href="https://www.linkedin.com/in/emmitt-paige" target="_blank">LinkedIn</a>
    <a href="mailto:e.t.paige@gmail.com" class="btn-gradient">Contact</a>
</div>
Updating Profile Information

Edit the following files:

Contact info: _layouts/tech.html (footer section)
Homepage content: index.md
About page bio: about/index.md
Deployment

Automatic Deployment (GitHub Pages)

This repository is configured to automatically deploy to GitHub Pages on every push to the main branch.

Manual Deployment Steps:

Commit your changes:
bash
git add .
git commit -m "Describe your changes"
Push to GitHub:
bash
git push origin main
Wait 1-3 minutes for GitHub Pages to build and deploy
View live at: https://epaige8594.github.io
Verify Deployment

Check deployment status:

Go to your repository on GitHub
Click the Actions tab
Look for a green checkmark ✓ on the latest workflow run
Troubleshooting

Common Issues and Solutions

Issue	Solution
bundle install fails	Ensure Ruby is installed: ruby --version. Update Ruby if necessary.
Jekyll serve errors	Run bundle update to refresh dependencies.
Changes not appearing	Clear browser cache or hard refresh (Cmd+Shift+R on Mac, Ctrl+Shift+R on Windows)
Port already in use	Use a different port: bundle exec jekyll serve --port 4001
GitHub Pages not updating	Check Actions tab for build errors; verify _config.yml syntax
CSS not loading	Verify file paths in _layouts/tech.html; check that assets/css/tech-style.css exists
Dropdown menu disappears too quickly	The CSS includes an invisible bridge to prevent this; ensure .dropdown::after styling is present
Debugging Commands

bash
# Check Jekyll configuration
bundle exec jekyll doctor

# Clear generated site and rebuild
rm -rf _site
bundle exec jekyll build

# Run with verbose output
bundle exec jekyll serve --verbose
Git Workflow Reference

Common Commands

bash
# Check status of changed files
git status

# Add all changes
git add .

# Commit with message
git commit -m "Description of changes"

# Push to GitHub
git push origin main

# Pull latest changes
git pull origin main

# View commit history
git log --oneline
Branching Strategy

bash
# Create a new branch for features
git checkout -b feature/new-document

# Switch back to main
git checkout main

# Delete a branch (after merging)
git branch -d feature/new-document
License

This project is licensed under the MIT License - see the LICENSE file for details.

Credits

Built with: Jekyll and GitHub Pages
Fonts: Inter by Google Fonts
Icons: Emoji for visual categorization
Color Scheme: Custom dark blue/teal theme
Contact

Emmitt Paige

📧 Email: e.t.paige@gmail.com
🔗 LinkedIn: linkedin.com/in/emmitt-paige
💻 Portfolio: epaige8594.github.io
🐙 GitHub: github.com/epaige8594
Acknowledgments

Special thanks to the open-source community for the tools that make projects like this possible.

Last Updated: March 2026
