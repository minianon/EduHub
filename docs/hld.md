# EduHub: High-Level Design

A responsive e-learning website front end: home, courses, video playlists, watch page, teachers and tutor profiles, student profile, login, register and contact pages, with dark mode. Live at [edu-hub-tb.vercel.app](https://edu-hub-tb.vercel.app). For code-level detail see the [Low-Level Design](lld.md).

## 1. Context

```mermaid
flowchart LR
  V([Student / tutor]) -->|browser| Pages[12 static HTML pages<br/>css/style.css + js/script.js]
  Host[Vercel static hosting] --> Pages
```

The site is a front-end template: there is no backend, so login, register, profile update and comments are UI only.

## 2. Pages

```mermaid
flowchart TB
  Home[home.html] --> Courses[courses.html]
  Courses --> Playlist[playlist.html]
  Playlist --> Watch[watch-video.html]
  Home --> Teachers[teachers.html] --> TP[teacher_profile.html]
  Home --> About[about.html]
  Home --> Contact[contact.html]
  Home --> Profile[profile.html] --> Update[update.html]
  Home --> Login[login.html]
  Home --> Register[register.html]
```

## 3. Tech

| Item | Choice |
|---|---|
| Markup / style | HTML5, one shared stylesheet |
| Behavior | Vanilla JavaScript (`js/script.js`) |
| Icons | Font Awesome |
| Hosting | Vercel |
