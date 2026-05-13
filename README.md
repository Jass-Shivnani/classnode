# 📚 Classnode — Student Learning Platform

> A cross-platform student app with realtime sync, built with Kotlin Multiplatform.

**Classnode** is a student-focused platform we've been building since early 2025 and we're still actively working on it. It started as a way to help our class stay organized — track attendance, share notes, manage timetables — and it turned into a full cross-platform app that runs on both Android and iOS from a single codebase.

This is a **showcase repository** — the source code is in a private repo since I plan to publish Classnode on the Play Store.

---

## ✨ What It Does

- **Subjects & Timetables** — Add your subjects, set up weekly schedules, and keep everything in one place.
- **Attendance Tracking** — Mark and track attendance for each subject. See percentages at a glance.
- **Notes Sharing** — Share study materials and notes across your class in realtime.
- **Realtime Sync** — Everything syncs in realtime across the entire class. If someone updates attendance or uploads a note, everyone sees it instantly.
- **Offline-First** — Works without internet. All data saves locally in Room DB and syncs automatically when you're back online using WorkManager.
- **Cross-Platform** — Single Kotlin codebase targets both Android and iOS using Kotlin Multiplatform (KMP).

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Language** | Kotlin |
| **UI Framework** | Jetpack Compose (Multiplatform) |
| **Architecture** | Kotlin Multiplatform (KMP) — shared business logic across Android & iOS |
| **Local Database** | Room DB |
| **Background Sync** | WorkManager |
| **State Management** | Kotlin Flows + ViewModel |
| **Networking** | Ktor Client |

---

## 📱 Platforms

- ✅ Android (primary)
- ✅ iOS (via KMP shared module)

---

## 🏗️ Architecture

```
┌─────────────────────────────────┐
│         Compose UI Layer        │  ← Platform-specific UI
├─────────────────────────────────┤
│       Shared KMP Module         │  ← ViewModels, Use Cases, Repos
├─────────────────────────────────┤
│    Room DB     │   Ktor Client  │  ← Local storage + Network
└────────────────┴────────────────┘
         ↕ WorkManager (Background Sync)
```

- **Offline-first**: All reads come from Room. Network data syncs in the background.
- **Realtime updates**: Changes pushed to all connected users in the class.
- **Single source of truth**: Room DB acts as the cache layer; network is the sync layer.

---

## 🚀 Status

🟢 **Actively in development** — new features being added regularly.  
📱 **Play Store release planned** — working toward a public launch.

---

## 👥 Developers

**Jass Suraj Shivnani**  
B.E. Computer Engineering, VESIT Mumbai (Batch 2027)  
[LinkedIn](https://linkedin.com/in/jass-shivnani-409b5a35a) · [GitHub](https://github.com/Jass-Shivnani)

**Riya Sanjay Khialani**  
B.E. Computer Engineering, VESIT Mumbai (Batch 2027)  
[LinkedIn](https://www.linkedin.com/in/riya-khialani-596a4a3b6/) · [GitHub](https://github.com/Riya-Khialani)

---

*This is a showcase repository. Source code is private.*
