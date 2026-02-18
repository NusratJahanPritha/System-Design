# 📸 Instagram LLD - User & Feed Microservice (Java)

Welcome to the Low-Level Design of a core **Instagram-like backend microservice**, built in Java.

This microservice handles:
- 👤 User creation and following
- 🖼️ Post uploads
- 📰 Feed fanout (push/pull logic)
- 🧠 Redis-simulated sorted sets for real-time feeds

---

## 🔧 Modules Implemented

| Module        | Description                                  |
|---------------|----------------------------------------------|
| **UserService**  | Manages users and follower relationships     |
| **PostService**  | Uploads media posts with metadata            |
| **FeedService**  | Pushes/pulls posts to follower feeds using strategy pattern |
| **RedisClient**  | In-memory simulation of Redis Sorted Set (`ZADD`, `ZRANGE`) |

---

## 🧠 Design Patterns Used

- **Singleton**: `UserService`, `RedisClient`  
- **Strategy**: `FanoutStrategy` → `Push` vs `Pull` logic  
- **Adapter**: `RedisClient` wraps Redis logic  
- **Immutable Models**: `User`, `Post` have final fields  

---

## 📁 Folder Structure

org.example/
├── models/ // Entities: User, Post
├── services/ // Core logic: Feed, User, Post
├── feed/ // Strategy pattern: PushFanout, PullFanout
└── Main.java // Entry point


---


## 🛠️ Tech Stack

- Java 17
- No external dependencies (fully in-memory)
- Designed for education & YouTube LLD series


