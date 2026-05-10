## 🧪 Edge Cases Handled

| Case | Status |
|---|---|
| Offline message delivery | ✅ |
| Same user multiple tabs | ✅ |
| Empty message validation | ✅ |
| Invalid receiver | ✅ |
| Server resilience | ✅ |

## 🏆 Key Design Decisions

**Why Kafka?**
Redis Pub/Sub drops messages for offline users. 
Kafka persists messages and delivers reliably 
across multiple server instances.

**Why PostgreSQL?**
Native full-text search, MVCC concurrency, 
ACID compliance — perfect for chat history.

**Why Redis?**
Sub-millisecond lookups for online status 
and pending message cache.

**Why WebSocket over REST for delivery?**
WebSocket connection is already established.
Using ready signal eliminates race conditions
and reduces latency from 1000ms to <10ms.

## 👨‍💻 Author

Dharanesh CA
- GitHub: [@Dharanesh64](https://github.com/Dharanesh64)
