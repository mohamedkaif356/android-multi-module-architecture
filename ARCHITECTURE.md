# Architecture Overview

This repository contains code examples and patterns from the blog post: **"Scaling Android Apps: Building a Unified Multi-Module Framework with Clean Architecture and CI/CD"**

## Module Structure

```
app/
├── src/
│   └── main/
│       ├── java/com/yourcompany/app/
│       │   └── MainActivity.kt
│       └── res/
│
feature-chatbot/
├── src/
│   └── main/
│       ├── java/com/yourcompany/chatbot/
│       │   ├── ui/
│       │   ├── viewmodel/
│       │   └── repository/
│       └── res/
│
core-network/
├── src/
│   └── main/
│       └── java/com/yourcompany/core/network/
│           ├── ApiService.kt
│           └── NetworkModule.kt
│
core-database/
├── src/
│   └── main/
│       └── java/com/yourcompany/core/database/
│           ├── AppDatabase.kt
│           └── Dao.kt
│
core-security/
├── src/
│   └── main/
│       └── java/com/yourcompany/core/security/
│           ├── SecureKeyManager.kt
│           └── EncryptionModule.kt
│
foundation-ui/
├── src/
│   └── main/
│       └── java/com/yourcompany/foundation/ui/
│           └── components/
│
foundation-design/
├── src/
│   └── main/
│       └── java/com/yourcompany/foundation/design/
│           └── Theme.kt
```

## Dependency Graph

- **app** → depends on all feature modules
- **feature-*** → depends on core modules and foundation modules
- **core-*** → depends on foundation modules only
- **foundation-*** → no dependencies (base layer)

## Getting Started

1. Clone the repository
2. Open in Android Studio
3. Build and run the app
4. Refer to README.md for detailed explanations
