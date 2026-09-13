# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Initial repository setup with combined frontend and backend
- Docker Compose configuration for local development
- CI/CD workflows for backend and frontend
- Comprehensive documentation and setup guides
- GitHub issue and PR templates
- Branch protection rules configuration
- Development contribution guidelines

### Coming Soon
- Self-hosting guide
- Plugin system
- Admin dashboard
- Multi-tenant support

## [0.1.0] - 2026-09-13

### Added
- Frontend (Clone): React 19 with Tailwind CSS
  - Landing page with showcase and features
  - Authentication system (signup/login)
  - Dashboard with builds and billing
  - AI Chat integration
  - React Router navigation
  
- Backend (CreatorApp24): FastAPI with MongoDB
  - REST API endpoints
  - JWT authentication
  - MongoDB integration
  - AI chat endpoints
  - AppMaker24 integration
  
- Infrastructure
  - Docker Compose setup for local development
  - Backend Dockerfile for containerization
  - Environment configuration files
  - .gitignore for full-stack project
  
- Documentation
  - README with architecture and quick start
  - Environment variables guide
  - API overview
  - Deployment instructions

### Initial Features
- User authentication (JWT-based)
- Waitlist signup API
- Chat API endpoints
- MongoDB data persistence
- React-based frontend UI
- FastAPI REST backend
- Docker containerization

---

## How to Update This File

When making releases:

1. Add new `## [X.Y.Z] - YYYY-MM-DD` section at the top
2. Move items from `[Unreleased]` section
3. Update version in package.json

## Categories

Use these categories:
- **Added**: for new features
- **Changed**: for changes in existing functionality
- **Fixed**: for any bug fixes
- **Security**: for security issue fixes

---

For detailed release notes, visit: https://github.com/ashleygeeeeg/Geeus-AI/releases
