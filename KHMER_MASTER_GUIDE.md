# 🇰🇭 JAXSETH TEST THE DREAM EXPERIENCE
# Master Course — Khmer Reading Edition

## 1. គោលដៅរបស់ Project

JaxSeth Test The Dream Experience គឺជា Roblox social hangout
experience ដែលផ្ដោតលើ:

- ការដើរលេង
- ការសង្គមជាមួយអ្នកលេង
- ការរុករកពិភពលោក
- Missions
- Coins
- Rewards
- NPC
- Shop
- Achievements
- Leaderboards
- Community
- Discovery

វាមិនគួរត្រូវបានបម្លែងទៅជា RPG ដែលស្មុគស្មាញដោយមិនចាំបាច់ទេ។

---

# 2. គោលការណ៍សំខាន់

## CLIENT = UNTRUSTED

Client អាចផ្ញើ request ប៉ុណ្ណោះ។

## SERVER = AUTHORITY

Server ត្រូវជាអ្នកពិនិត្យ និងសម្រេច:

- Coins
- Rewards
- Purchases
- Missions
- Permissions
- Roles
- Achievements
- Teleports
- License state

---

# 3. World Zones

### Dream Plaza
តំបន់កណ្ដាលសម្រាប់ Spawn និង Social។

### Sky Garden
តំបន់កោះអណ្ដែតលើមេឃ។

### Dream City
ទីក្រុងដែលមានផ្លូវ អគារ និង NPC។

### Dream Café
កន្លែង Café និង Mission NPC។

### Dream Stage
កន្លែង Music, Dance និង Events។

### Dream Forest
ព្រៃសម្រាប់ Exploration និង Collectibles។

### Secret Dream Area
តំបន់សម្ងាត់ដែលអាច Unlock តាម Exploration។

### Community Center
កន្លែងសម្រាប់ Rules, FAQ, Events និង Community។

---

# 4. Mission System

Mission មានប្រភេទ:

- Exploration
- Social
- Daily
- Discovery
- Collection
- NPC
- Community
- Event

Client មិនអាចនិយាយថា:

"ខ្ញុំបានបញ្ចប់ Mission"

ហើយឲ្យ Server ជឿដោយស្វ័យប្រវត្តិទេ។

Server ត្រូវ verify objective។

---

# 5. Coin Economy

Coins ត្រូវគ្រប់គ្រងដោយ Server។

ប្រភព Coins:

- Missions
- Achievements
- Events
- Exploration
- Daily activities

Client មិនត្រូវផ្ញើ:

"Give me 999999 Coins"

ហើយឲ្យ Server ទទួលយកឡើយ។

---

# 6. Shop

Shop មាន:

- Tools
- Cosmetics
- Emotes
- Effects
- Special Items

Server ត្រូវពិនិត្យ:

1. Item មានឬទេ?
2. តម្លៃត្រឹមត្រូវឬទេ?
3. Player មាន Coins គ្រប់គ្រាន់ឬទេ?
4. Player មាន Item រួចឬទេ?
5. Transaction ត្រូវបានបញ្ជូនម្ដងហើយឬនៅ?
6. Request spam ឬទេ?

Client មិនត្រូវកំណត់ Price។

---

# 7. License System

License states:

- CHECKING
- ACTIVE
- NOT_FOUND
- EXPIRED
- REVOKED
- INVALID
- USER_MISMATCH
- PRODUCT_MISMATCH
- SERVICE_UNAVAILABLE
- VERSION_UNSUPPORTED

Private secret ត្រូវនៅ Server។

---

# 8. Anti-Cheat

ប្រើ Defense in Depth:

Remote Validation
+
Rate Limiting
+
Permission Validation
+
State Validation
+
Distance Validation
+
Economy Validation
+
Movement Signals
+
Interaction Validation
+
Violation Scoring
+
Audit Logging

កុំ Ban Player ដោយសារតែ signal ខ្សោយតែមួយ។

---

# 9. Performance

ត្រូវគិតពី:

- FPS
- CPU
- GPU
- Memory
- Physics
- Network
- NPC
- VFX
- Audio

ប្រើ:

- Streaming
- LOD
- NPC Scheduler
- VFX Pool
- Cleanup System
- Network throttling

---

# 10. Development Rule

កុំបង្កើត script មួយធំដែលមាន system ទាំងអស់។

ប្រើ Modular Architecture:

Service
→ Validation
→ State
→ Action
→ Persistence

---

# 11. Development Phases

Phase 01 — Foundation

Phase 02 — Configuration

Phase 03 — Server Bootstrap

Phase 04 — Player System

Phase 05 — Data

Phase 06 — Security

Phase 07 — World

Phase 08 — NPC

Phase 09 — Missions

Phase 10 — Economy

Phase 11 — Shop

Phase 12 — Tools

Phase 13 — Levels

Phase 14 — Achievements

Phase 15 — Leaderboards

Phase 16 — Social

Phase 17 — Community

Phase 18 — License

Phase 19 — Premium UI

Phase 20 — Performance

Phase 21 — QA

Phase 22 — Production

---

# 12. Final Rule

Feature មួយត្រូវឆ្លងកាត់:

- Useful?
- Premium?
- Secure?
- Server-authoritative?
- Performant?
- Mobile-friendly?
- Scalable?
- Maintainable?
- Testable?

បើមិនបានទេ ត្រូវ redesign។
