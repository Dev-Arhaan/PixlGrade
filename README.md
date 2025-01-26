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
