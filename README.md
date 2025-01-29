# PixlGrade

A SaaS web app for real-time code/design comparison with integrated editor and preview system.

![PixlGrade Demo](docs/demo.gif) <!-- Add a demo GIF later -->

## Project Overview

PixlGrade enables developers to:
- Write code in HTML/CSS/JS/React/Vue
- Upload design files (Figma/Sketch/PNG/SVG)
- Toggle between design reference and live preview
- Collaborate in real-time

## Features

### MVP Features
- Split-view editor/preview interface
- Monaco code editor with syntax highlighting
- Design file upload (PNG/SVG)
- Real-time preview rendering
- User authentication (JWT)
- Project management (CRUD)
- Dockerized environment

## Tech Stack

### Frontend
- **Next.js** (TypeScript)
- React
- Monaco Editor
- Axios

### Backend
- **Go** (Gin framework)
- GORM (MySQL ORM)
- Azure Storage SDK (Blob uploads)

### Database
- MySQL

### Infrastructure
- Docker
- **Azure** (Virtual Machines, Azure Database for MySQL, Blob Storage)
- Terraform

## Getting Started

### Prerequisites
- Node.js v18+
- Go 1.21+
- Docker 24+
- Azure CLI (for deployment)

### Installation

1. **Clone Repository**
```bash
git clone https://github.com/dev-arhaan/pixlgrade.git
cd pixlgrade
```

# **PixlGrade WebContainer Integration Checklist**

## **Phase 1: Setup & Initialization**
- [x] **Set up a Next.js project**  
  - Install dependencies: `@webcontainer/api monaco-editor`  
- [x] **Initialize WebContainers**  
  - Boot a WebContainer instance (`WebContainer.boot()`)  
- [x] **Create a virtual filesystem**  
  - Add default files: `index.html`, `script.js`, `package.json`  

---

## **Phase 2: Code Editor Integration**
- [x] **Integrate Monaco Editor for user code input**  
  - Create an `Editor.tsx` component  
- [x] **Sync Monaco Editor with WebContainer**  
  - Bind the editor state to WebContainer's filesystem  

---

## **Phase 3: Running User Code**
- [x] **Implement code execution inside WebContainers**  
  - Run JavaScript using `webContainer.spawn('node', ['script.js'])`  
- [x] **Capture and display console output**  
  - Pipe WebContainer output to a UI console  

---

## **Phase 4: Live Preview Panel**
- [ ] **Set up an HTTP server inside WebContainer**  
  - Add `serve` or a lightweight Node server  
- [ ] **Display live preview inside an iframe**  
  - Load WebContainer’s hosted output in `<iframe>`  

---

## **Phase 5: Advanced Features**
- [ ] **Enable React/Vue Support**  
  - Install React (`npm install react react-dom`)  
  - Handle React/Vue project structures inside WebContainer  
- [ ] **Implement Hot Reloading**  
  - Auto-refresh preview on code changes  

---

## **Phase 6: Scoring System & Performance Metrics**
- [ ] **Define a scoring algorithm**  
  - Compare user code vs. expected output  
- [ ] **Implement time-based evaluation**  
  - Track execution time for solutions  
- [ ] **Generate reports on code quality & correctness**  

---

## **Phase 7: Deployment & Optimization**
- [ ] **Persist user sessions**  
  - Use IndexedDB for caching user progress  
- [ ] **Optimize WebContainer performance**  
  - Minimize memory usage & optimize package installations  
- [ ] **Deploy PixlGrade MVP**  
  - Ensure WebContainers work smoothly in production
