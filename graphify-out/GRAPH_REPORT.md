# Knowledge Graph Report

## Overview
Corpus: 3 files - 4,868 words

## God Nodes (Most Connected)

| Rank | Node | Degree |
|------|------|--------|
| 1 | admin.html | 11 |
| 2 | Shree Saraswati Secondary School | 7 |
| 3 | Teachers Panel | 2 |
| 4 | Notices Panel | 2 |
| 5 | Students Panel | 2 |

## Communities

- Community 0: Tech Stack (static HTML, vanilla HTML/CSS/JS, Google Fonts, base64 images, localStorage)
- Community 1: Admin Panel Hub (admin.html connecting to all panels)
- Community 2: Teacher Management (Teachers Panel, Teacher Fields)
- Community 3: Notice Management (Notices Panel, Notice Categories)
- Community 4: Student Data (Students Panel, Student Classes ECD-12)
- Community 5: Statistics (Statistics Panel, School Statistics)
- Community 6: Settings (Settings Panel, School Settings, Color Palette, Fonts)

## Surprising Connections

1. **admin.html** is the central hub connecting 6 different panel communities
2. **Shree Saraswati Secondary School** bridges the tech stack (Community 0) to the admin system (Community 1)

## Suggested Questions

1. Why does `admin.html` connect `Community 1` to all other communities? (High betweenness centrality - this is the cross-community bridge)
2. Why does `Shree Saraswati Secondary School` connect to both the website (index.html) and admin panel?
3. What is missing? 16 nodes are weakly connected - possible documentation gaps (index.html not fully analyzed)

## Architecture Summary

```
Shree Saraswati Secondary School (Satyawati, Gulmi, Nepal)
    |
    +-- Tech Stack: static HTML, vanilla HTML/CSS/JS, Google Fonts, base64 images
    |
    +-- index.html (main website)
    |
    +-- admin.html (CRUD admin panel)
            |
            +-- Dashboard
            +-- Teachers (name, gender, qualification, level, subject, photo)
            +-- Notices (exam, admission, event categories)
            +-- Students (ECD through Grade 12)
            +-- Statistics (total, male, female, staff counts)
            +-- Gallery
            +-- Admission Inquiries
            +-- Settings (name, phone, email, address, IEMIS code)
```