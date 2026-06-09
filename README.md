# Roomify

Roomify is an AI-powered architectural visualization platform that transforms 2D floor plans into realistic rendered spaces. Users can upload architectural layouts, generate AI-enhanced visualizations, compare results side-by-side, export rendered images, and share projects with others.

---

## Overview

Architects, interior designers, students, and homeowners often struggle to visualize how a floor plan will look once completed. Roomify bridges that gap by leveraging artificial intelligence to generate realistic visual representations from architectural plans.

The platform provides a simple workflow:

1. Upload a floor plan.
2. Create a project.
3. Generate an AI-powered visualization.
4. Compare the original plan with the generated render.
5. Export or share the final result.

---

## Features

### AI Visualization

- Generate realistic 3D-style renders from floor plans.
- Automatic processing through AI services.
- Persistent storage of generated results.

### Project Management

- Create and save visualization projects.
- Retrieve previously generated projects.
- Private project storage.

### Before / After Comparison

- Interactive comparison slider.
- Compare original floor plan against AI-generated render.
- Real-time visual inspection.

### Export

- Download generated renders as PNG images.
- High-quality image export.

### Share

- Native sharing support through the Web Share API.
- Automatic clipboard fallback when sharing is unavailable.
- Easy project distribution.

### Error Handling

- User-friendly error messages.
- Project loading validation.
- AI generation failure notifications.
- Graceful recovery from unexpected failures.

---

# Screenshots

Add screenshots of the application here.

## Home Page

```text
Upload Floor Plan
      ↓
Create Project
      ↓
Open Visualizer
```

## Visualizer

```text
Original Plan  ←→  AI Generated Render
```

---

# Tech Stack

## Frontend

- React 19
- React Router 7
- TypeScript
- Tailwind CSS
- Vite

## Libraries

### UI & UX

- lucide-react
- react-compare-slider

### AI Integration

- @heyputer/puter.js

---

# Project Structure

```text
roomify/
│
├── app/
│   ├── routes/
│   │   ├── home.tsx
│   │   └── visualizer.$id.tsx
│   │
│   ├── root.tsx
│   └── routes.ts
│
├── components/
│   ├── ui/
│   │   └── Button.tsx
│   │
│   └── ...
│
├── lib/
│   ├── ai.action.ts
│   └── puter.action.ts
│
├── public/
│
├── package.json
│
└── README.md
```

---

# Architecture

```text
┌───────────────┐
│     User      │
└───────┬───────┘
        │
        ▼
┌────────────────────┐
│      Home Page     │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│   Create Project   │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│ Project Storage    │
│ (Puter Services)   │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│    Visualizer      │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│ AI Render Service  │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│ Rendered Image     │
└────────────────────┘
```

---

# Installation

## Clone Repository

```bash
git clone https://github.com/Pa004/roomify.git
```

```bash
cd roomify
```

---

## Install Dependencies

```bash
npm install
```

---

## Run Development Server

```bash
npm run dev
```

The application will be available at:

```text
http://localhost:5173
```

---

# Production Build

Generate a production build:

```bash
npm run build
```

Preview the build:

```bash
npm run preview
```

---

# Configuration

Roomify relies on Puter services for:

- Authentication
- Project persistence
- AI image generation

Before deployment, ensure the corresponding Puter configuration and credentials are correctly configured.

---

# Main Workflow

## 1. Upload Floor Plan

Users upload an architectural layout.

```text
Image Upload
      ↓
Validation
      ↓
Project Creation
```

---

## 2. Generate Visualization

The system sends the source image to the AI rendering service.

```text
Source Image
      ↓
AI Processing
      ↓
Rendered Visualization
```

---

## 3. Compare Results

Users can compare:

- Original floor plan
- Generated render

using the interactive comparison slider.

---

## 4. Export

Download the generated render as a PNG image.

---

## 5. Share

Share the project URL through:

- Native mobile sharing
- Browser sharing
- Clipboard copy fallback

---

# Error Handling

The application includes:

### Project Loading Errors

```text
Project not found.
```

### AI Rendering Errors

```text
Unable to generate the 3D visualization.
Please try again.
```

### Share Errors

```text
Unable to share the project.
```

### Clipboard Fallback

```text
Project link copied to clipboard.
```

---

# Recent Improvements

### Version 1.1

#### Metadata Improvements

Updated application metadata:

- Custom title
- SEO-friendly description

#### Share Functionality

Implemented:

- Web Share API
- Clipboard fallback
- Share validation

#### Error Management

Added:

- Project loading validation
- Generation error handling
- User-facing feedback messages

#### Better Project IDs

Replaced timestamp-based identifiers with:

```typescript
crypto.randomUUID()
```

to improve uniqueness and scalability.

---

# Roadmap

Planned features:

- Public project gallery
- Multiple rendering styles
- User profiles
- Collaborative editing
- Cloud synchronization
- Project comments
- Version history
- Favorite projects
- Export to additional formats
- Dark mode

---

# Contributing

Contributions are welcome.

1. Fork the repository.
2. Create a feature branch.

```bash
git checkout -b feature/new-feature
```

3. Commit your changes.

```bash
git commit -m "Add new feature"
```

4. Push to your branch.

```bash
git push origin feature/new-feature
```

5. Open a Pull Request.

---

# License

This project is licensed under the MIT License.

---

# Author

Developed as part of the Roomify architectural visualization platform.

GitHub Repository:

https://github.com/Pa004/roomify