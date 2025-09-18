# 🌊 Chaoxi - Tidal Tools

## 📋 Table of Contents
- [📖 About](#-about)
- [🚀 Getting Started](#-getting-started)
- [🔨 How to Build / How to Run](#-how-to-build--how-to-run)
- [🏗️ Project Structure](#️-project-structure)
- [🎯 Features](#-features)
- [📚 Dependencies](#-dependencies)
- [🌊 Tidal Tools Workflow](#-tidal-tools-workflow)
- [💡 Usage](#-usage)
- [🔧 Command Line Interface](#-command-line-interface)
- [🌐 Web Interface](#-web-interface)
- [📄 License](#-license)

## 📖 About
Chaoxi is an opensource microservice Vue.js component builder with REST API connection capabilities. Built around the philosophy of tidal movements, it provides a complete toolkit for scaffolding, structuring, and managing web application projects using three core tools inspired by ocean tides.

The project uses Chinese maritime terminology:
- **涨潮 (zhangchao)** - Rising tide: Project scaffolding
- **退潮 (tuichao)** - Falling tide: Structure extraction
- **海地 (haidi)** - Seabed: Project structure storage

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm package manager
- Modern web browser for web interface

### 📦 Installation
```bash
git clone https://github.com/Mino75/chaoxi.git
cd chaoxi
npm install
```

## 🔨 How to Build / How to Run

### Web Interface (GitHub Pages)
The project is automatically deployed to GitHub Pages and accessible at:
```
https://chaoxi.github.io
```

### Local Development
```bash
# Clone the repository
git clone https://github.com/Mino75/chaoxi.git
cd chaoxi

# Open index.html in your browser or serve with a local server
python -m http.server 8000
# or
npx serve .
```

### Command Line Usage
```bash
# Scaffold a new project (Rising Tide)
node zhangchao.js myproject

# Extract project structure (Falling Tide)
node tuichao.js myproject

# Use custom structure file
node zhangchao.js myproject custom-structure.json
node tuichao.js myproject custom-output.json
```

## 🏗️ Project Structure
```
chaoxi/
├── index.html              # Web interface for tidal tools
├── main.js                 # Client-side ZIP download logic
├── zhangchao.js           # 涨潮 - Project scaffolding tool
├── tuichao.js             # 退潮 - Structure extraction tool
├── haidi.json             # 海地 - Default project structure
├── _config.yml            # GitHub Pages configuration
├── LICENSE                # MIT License
├── README.md              # Project documentation
├── .gitattributes         # Git line ending configuration
└── .github/workflows/     # GitHub Actions
    └── static.yml         # Pages deployment workflow
```

## 🎯 Features
- **Project Scaffolding**: Instantly create new projects with predefined structure
- **Structure Extraction**: Generate JSON representations of existing projects
- **Web Interface**: Browser-based tool download and management
- **Command Line Tools**: Powerful CLI for automation and scripting
- **Flexible Configuration**: Customizable project templates via JSON
- **GitHub Pages Integration**: Automatic deployment and hosting
- **Zero Dependencies**: Pure Node.js implementation
- **Cross-Platform**: Works on Windows, macOS, and Linux

### Default Project Template
Each scaffolded project includes:
- **index.html** - Main application entry point
- **main.js** - Core application logic
- **styles.js** - Styling and UI components
- **server.js** - Backend server configuration
- **service-worker.js** - PWA service worker
- **dockerfile** - Docker containerization
- **manifest.json** - PWA manifest

## 📚 Dependencies

### Core Requirements
- **Node.js**: Built-in `fs` and `path` modules
- **No external dependencies**: Pure JavaScript implementation

### Web Interface Dependencies
- **JSZip**: `3.10.1` - Client-side ZIP file generation
- **Modern Browser**: FileReader API and ES6+ support

### Development Dependencies
- **GitHub Actions**: Automated deployment
- **GitHub Pages**: Static hosting

## 🌊 Tidal Tools Workflow

### 1. Rising Tide (涨潮) - Scaffolding
Creates new projects from structure templates:
```bash
node zhangchao.js myproject        # Use default haidi.json
node zhangchao.js myproject custom.json  # Use custom template
```

### 2. Falling Tide (退潮) - Extraction
Generates structure files from existing projects:
```bash
node tuichao.js myproject          # Output to haidi.json
node tuichao.js myproject output.json    # Custom output file
```

### 3. Seabed (海地) - Structure Storage
JSON format for project templates:
```json
{
  "files": [
    {
      "name": "index.html",
      "content": "<!DOCTYPE html>..."
    },
    {
      "name": "main.js", 
      "content": "// main.js"
    }
  ]
}
```

## 💡 Usage

### Creating a New Project
```bash
# Create project with default structure
node zhangchao.js my-new-app

# Verify the created structure
ls my-new-app/
# Output: dockerfile  index.html  main.js  manifest.json  server.js  service-worker.js  styles.js
```

### Extracting Project Structure
```bash
# Extract from existing project
node tuichao.js existing-project

# Creates haidi.json with the project structure
cat haidi.json
```

### Custom Templates
Create your own structure file:
```json
{
  "files": [
    {
      "name": "package.json",
      "content": "{\n  \"name\": \"my-app\",\n  \"version\": \"1.0.0\"\n}"
    },
    {
      "name": "src/index.js",
      "content": "console.log('Hello World');"
    }
  ]
}
```

## 🔧 Command Line Interface

### zhangchao.js (Project Scaffolding)
```bash
Usage: node zhangchao.js <projectName> [inputFile]

Parameters:
  projectName    Name of the project folder to create
  inputFile      JSON structure file (default: haidi.json)

Examples:
  node zhangchao.js myapp
  node zhangchao.js myapp custom-template.json
```

### tuichao.js (Structure Extraction)
```bash
Usage: node tuichao.js <projectName> [outputFile]

Parameters:
  projectName    Name of existing project folder
  outputFile     Output JSON file (default: haidi.json)

Examples:
  node tuichao.js existing-project
  node tuichao.js existing-project backup.json
```

## 🌐 Web Interface

### Features
- **Download All Tools**: Get all tidal tools as a ZIP archive
- **Tool Information**: Chinese names, Latin descriptions, and emojis
- **Responsive Design**: Works on desktop and mobile devices
- **Analytics Integration**: Built-in usage tracking

### Accessing the Web Interface
1. Visit: https://chaoxi.github.io
2. Click "Download All Files" to get the complete toolkit
3. Extract and use the command-line tools locally

### File Structure in ZIP
The downloaded archive contains:
- `zhangchao.js` - Scaffolding tool
- `tuichao.js` - Extraction tool  
- `haidi.json` - Default structure template

## 📄 License
MIT License

Copyright (c) 2024 Mino

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
