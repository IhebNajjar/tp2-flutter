# Waiting Room App — Workshop 2: Local State Management & TDD

A Flutter application developed for **Workshop 2**, focusing on local state management using `setState()`, separating logic into a manager class (`WaitingRoomManager`), and building features with **Test-Driven Development (TDD)**.

---

## 📌 Workshop 2 Overview

In this workshop, the app evolves from a static card to an interactive client waiting room queue:

- **Interactive Queue View:** Add clients by entering their name and tapping **Add**.
- **Real-Time Queue Counter:** Displays `Clients in Queue: X`, updated dynamically.
- **Client Removal:** Remove individual clients from the queue with the delete icon button (`Icons.delete`).
- **Local State Management:** Manages UI updates via `setState()` within a `StatefulWidget` (`WaitingRoomScreen`).
- **Decoupled Manager:** State logic is encapsulated in `WaitingRoomManager` (`lib/waiting_room_manager.dart`).

---

## 🏗️ Architecture

```
lib/
├── main.dart                  # App entry point, WaitingRoomApp & WaitingRoomScreen (StatefulWidget)
└── waiting_room_manager.dart  # Business logic manager for adding/removing clients
test/
├── waiting_room_manager_test.dart # Unit tests for WaitingRoomManager logic
└── waiting_room_widget_test.dart  # Widget tests for UI interactions and setState updates
```

---

## 🧪 Test-Driven Development (TDD)

### 1. Unit Tests (`test/waiting_room_manager_test.dart`)
- `should add a client to the waiting list`
- `should remove a client from the waiting list`

### 2. Widget Tests (`test/waiting_room_widget_test.dart`)
- `should add a new client to the list on button tap`
- `should remove a client from the list when the delete button is tapped`

---

## 🚀 How to Run

```bash
# Install packages
flutter pub get

# Run all tests
flutter test

# Run application
flutter run -d chrome # or edge / windows
```
