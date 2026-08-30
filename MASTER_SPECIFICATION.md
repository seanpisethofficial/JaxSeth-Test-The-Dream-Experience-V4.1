# 🌌 JAXSETH TEST THE DREAM EXPERIENCE

> **SUPER ULTRA PROFESSIONAL PREMIUM — LEVEL MASTER**
>
> Roblox Studio 2026 • Luau • Mobile • Tablet • PC • Controller

A production-oriented specification for a premium social hangout experience combining **hangout, exploration, missions, rewards, collection, social interaction, and discovery**.

---

## 🎯 Project Vision

**JaxSeth Test The Dream Experience** is designed as a social-first dream world rather than an unnecessarily complicated RPG.

Core pillars:

- 🌌 Premium dream world
- 🗺️ Interactive map
- 🧭 Master guide
- 👥 Hangout/social spaces
- 🤖 NPC system
- 🎯 Mission system
- 🪙 Server-authoritative coin economy
- 🛍️ Premium shop
- 🧰 Secure tools
- ⭐ XP / level progression
- 🏆 Achievements
- 📊 Leaderboards
- 🎭 Emotes
- ☕ Café
- 🎵 Music / stage
- 🌲 Exploration
- 🌙 Secret area
- 🏘️ Community center
- 📢 Announcements
- 👑 Developer dashboard
- 🔐 License system
- 🆔 UserId authorization
- 🛡️ Multi-layer anti-cheat
- ⚡ Performance engineering
- 📱 Mobile optimization
- 🎮 Controller support
- 💾 Data persistence
- 🧪 QA system
- 📚 Documentation

---

# 🏗️ Architecture

```text
JAXSETH_TEST_THE_DREAM
│
├── CORE
│   ├── Bootstrap
│   ├── Configuration
│   ├── ServiceRegistry
│   ├── Signals
│   ├── Constants
│   └── Utilities
│
├── PLAYER
│   ├── PlayerService
│   ├── ProfileService
│   ├── LevelService
│   ├── StatisticsService
│   └── SessionService
│
├── GAMEPLAY
│   ├── MissionService
│   ├── RewardService
│   ├── CoinService
│   ├── ToolService
│   ├── InteractionService
│   ├── TeleportService
│   ├── ZoneService
│   └── AchievementService
│
├── NPC
│   ├── NPCService
│   ├── DialogueService
│   ├── QuestNPCService
│   └── NPCScheduler
│
├── SHOP
│   ├── ShopService
│   ├── ItemRegistry
│   ├── PurchaseService
│   └── InventoryService
│
├── SOCIAL
│   ├── EmoteService
│   ├── CommunityService
│   ├── AnnouncementService
│   └── EventService
│
├── LEADERBOARD
│   ├── LeaderboardService
│   ├── GlobalLeaderboard
│   └── LocalLeaderboard
│
├── SECURITY
│   ├── RemoteGuard
│   ├── Validator
│   ├── RateLimiter
│   ├── PermissionService
│   ├── AntiCheatService
│   ├── ViolationManager
│   └── AuditLogger
│
├── LICENSE
│   ├── LicenseService
│   ├── LicenseValidator
│   ├── LicenseProvider
│   └── LicenseCache
│
├── PERFORMANCE
│   ├── PerformanceManager
│   ├── LODManager
│   ├── VFXPool
│   ├── NPCScheduler
│   └── CleanupManager
│
├── DATA
│   ├── DataService
│   ├── Validation
│   ├── SaveManager
│   └── Migration
│
└── ADMIN
    ├── AdminService
    ├── CommandService
    └── DeveloperDashboard
```

## 📁 Roblox Explorer Layout

```text
ReplicatedStorage
├── Shared
│   ├── Config
│   ├── Constants
│   ├── Types
│   └── Utilities
├── Remotes
│   ├── Gameplay
│   ├── Missions
│   ├── Shop
│   ├── Social
│   ├── UI
│   ├── License
│   └── Security
└── Assets
    ├── UI
    ├── Animations
    ├── Sounds
    └── Effects

ServerScriptService
└── Server
    ├── Bootstrap.server.lua
    ├── Services
    ├── Security
    ├── License
    ├── Data
    ├── Admin
    └── Analytics

ServerStorage
├── PrivateAssets
├── ProtectedTools
├── ServerModules
└── ProtectedContent

StarterPlayer
└── StarterPlayerScripts
    └── Client
        ├── Bootstrap.client.lua
        ├── Controllers
        ├── UI
        ├── Camera
        ├── Input
        └── Effects

StarterGui
└── JaxSethUI

Workspace
├── World
├── Zones
├── NPC
├── Shops
├── MissionObjects
├── Interactive
├── Spawn
├── Leaderboards
└── Effects
```

---

# 🌎 World

### Zone 01 — Dream Plaza
Main hub with spawn, monument, mission board, shop, leaderboard, community portal, teleport hub, seating and social areas.

### Zone 02 — Sky Garden
Floating islands, clouds, bridges, waterfalls, trees, benches and secret collectibles.

### Zone 03 — Dream City
Streets, buildings, shops, apartments, café, NPCs and social spaces.

### Zone 04 — Dream Café
Café interior, counter, tables, chairs, staff NPCs, interactive objects and mission NPC.

### Zone 05 — Dream Stage
Main stage, dance floor, lighting, music, audience and event area.

### Zone 06 — Dream Forest
Trees, paths, lake, secret areas, collectibles, NPCs and exploration missions.

### Zone 07 — Secret Dream Area
Hidden entrance, Easter eggs, collectibles, special achievement and developer references.

### Zone 08 — Community Center
Rules, developer information, community information, announcements, events, FAQ and support.

---

# 🎯 Missions

Mission categories:

- Exploration
- Social
- Daily
- Discovery
- Collection
- NPC
- Community
- Event

Example registry:

```lua
return {
    Id = "ExploreDreamPlaza",
    Title = "Explore Dream Plaza",
    Description = "Visit the center of the dream world.",
    Type = "Exploration",

    Objective = {
        Type = "VisitZone",
        Target = "DreamPlaza",
        Amount = 1,
    },

    Rewards = {
        Coins = 50,
        XP = 25,
    },
}
```

### Security rule

The client may request an action, but **the server decides whether the objective was actually completed**.

Never treat:

```text
Client → "Mission completed!"
```

as proof.

---

# 🪙 Economy

The economy is server-authoritative.

Persist and validate:

- Coins
- XP
- Level
- Inventory
- Tools
- Achievements
- Mission progress
- Statistics
- Settings

Purchase pipeline:

```text
CLIENT REQUEST
      ↓
SERVER
      ↓
ITEM EXISTS?
      ↓
PLAYER OWNS?
      ↓
SERVER PRICE
      ↓
ENOUGH COINS?
      ↓
RATE LIMIT
      ↓
VALID TRANSACTION
      ↓
PURCHASE
      ↓
SAVE
```

The client never supplies the authoritative price or balance.

---

# 🛍️ Shop

Categories:

- Tools
- Cosmetics
- Emotes
- Effects
- Special Items

Validation requirements:

- Item exists
- Correct server-side price
- Player has sufficient coins
- Ownership checked
- Duplicate purchase prevented
- Availability checked
- Rate limit applied

---

# 🔐 License System

License states:

```text
CHECKING
ACTIVE
NOT_FOUND
EXPIRED
REVOKED
INVALID
USER_MISMATCH
PRODUCT_MISMATCH
SERVICE_UNAVAILABLE
VERSION_UNSUPPORTED
```

Configuration uses placeholders:

```lua
return {
    Enabled = true,
    ProductId = "YOUR_LICENSE_PRODUCT_ID",
    ProductVersion = "1.0.0",
}
```

Architecture:

```text
LicenseService
      ↓
LicenseValidator
      ↓
LicenseProvider
      ↓
External Provider (optional)
```

**Never place private license secrets in replicated/client code.**

License failure UX should provide safe, non-secret status information and actions such as **Retry** and **Contact Developer**.

---

# 🛡️ Anti-Cheat & Security

Core principle:

> **CLIENT = UNTRUSTED**
>
> **SERVER = AUTHORITY**

Defense in depth:

```text
REMOTE VALIDATION
+
RATE LIMITING
+
PERMISSION VALIDATION
+
STATE VALIDATION
+
DISTANCE VALIDATION
+
ECONOMY VALIDATION
+
MOVEMENT SIGNALS
+
INTERACTION VALIDATION
+
VIOLATION SCORING
+
AUDIT LOGGING
```

Validate every remote request for:

- Type
- Structure
- Size
- Rate
- Permission
- State
- Distance
- Value
- Game rule

Never trust client-provided:

- Coins
- Price
- Rewards
- Roles
- Permissions
- License status
- Achievement completion
- Teleport CFrame

### Violation model

Do not automatically ban from one weak signal.

Possible responses:

```text
IGNORE
LOG
THROTTLE
BLOCK ACTION
ESCALATE
```

Movement detection must account for legitimate teleports, respawns, vehicles, cutscenes and developer tools.

---

# 👤 Permissions

```lua
return {
    OwnerUserId = 0,
    Developers = {},
    Administrators = {},
    Moderators = {},
    Testers = {},
}
```

Roles:

```text
OWNER
DEVELOPER
ADMIN
MODERATOR
TESTER
VIP
PLAYER
```

Use real UserIds only after developer configuration. Never accept a UserId from the client as an authorization claim.

---

# 👑 Developer Dashboard

Protected panels:

- Server
- Performance
- Players
- Security
- License
- Missions
- Announcements
- Moderation
- Debug

All privileged actions require server-side authorization.

---

# 🎨 Premium UI/UX

Unified components:

- Button
- Panel
- Card
- Modal
- Notification
- Tab
- ProgressBar
- IconButton
- Tooltip
- LoadingState
- ErrorState
- EmptyState

Design goals:

**Premium • Modern • Elegant • Dreamlike • Minimal • Responsive**

Support:

- Touch
- Large controls
- Safe-area handling
- Controller navigation
- No hover-only interactions
- Accessibility settings
- UI scale
- Reduced VFX
- Camera shake toggle

---

# ⚡ Performance

Treat performance as a first-class system.

Optimize:

- Rendering
- CPU
- GPU
- Memory
- Physics
- Network
- Script execution
- Replication
- NPC AI
- VFX
- Audio

Use appropriate streaming and LOD strategies.

```text
NEAR   → HIGH DETAIL
MEDIUM → REDUCED DETAIL
FAR    → LOW DETAIL
```

NPC architecture:

```text
NPC MANAGER
     ↓
NPC SCHEDULER
     ↓
NEAR → FULL AI
MEDIUM → REDUCED AI
FAR → MINIMAL AI
```

Use reusable VFX pools and clean temporary connections/instances.

---

# 🧪 QA Matrix

## Missions

- [ ] Objective validation
- [ ] Duplicate completion
- [ ] Reward duplication
- [ ] Invalid mission
- [ ] Aborted mission

## Shop

- [ ] Invalid item
- [ ] Fake price
- [ ] Insufficient coins
- [ ] Duplicate purchase
- [ ] Remote spam

## Security

- [ ] Invalid remote
- [ ] Invalid type
- [ ] Invalid permission
- [ ] Invalid distance
- [ ] Remote spam
- [ ] Fake reward
- [ ] Fake achievement
- [ ] Fake license

## Performance

- [ ] Large map
- [ ] Many players
- [ ] Many NPCs
- [ ] Many VFX
- [ ] Mobile
- [ ] Low-end device
- [ ] Long session

Quality workflow:

```text
PROFILE
  ↓
IDENTIFY BOTTLENECK
  ↓
OPTIMIZE
  ↓
TEST
  ↓
PROFILE AGAIN
```

---

# 🔄 Development Stages

1. Experience foundation
2. Folder architecture
3. Configuration
4. Server bootstrap
5. Player foundation
6. Data layer
7. Security foundation
8. World
9. NPC framework
10. Missions
11. Economy
12. Shop
13. Tools
14. Levels
15. Achievements
16. Leaderboards
17. Social
18. Community
19. License
20. Premium UI
21. Performance
22. Security testing
23. Performance testing
24. Polish
25. Production release

Every stage must integrate with the previous stages without breaking existing APIs.

---

# 📚 Documentation

Required project documentation:

```text
README.md
ARCHITECTURE.md
SETUP_GUIDE.md
BUILD_GUIDE.md
WORLD_BUILDING.md
UI_GUIDE.md
MISSION_GUIDE.md
SHOP_GUIDE.md
NPC_GUIDE.md
ECONOMY.md
DATA_GUIDE.md
SECURITY.md
ANTI_CHEAT.md
LICENSE_SYSTEM.md
COMMUNITY.md
USERID_PERMISSIONS.md
PERFORMANCE.md
TESTING.md
TROUBLESHOOTING.md
CHANGELOG.md
```

---

# 🤖 Ultimate AI Coding Prompt

Use the following master instruction with an AI coding assistant:

```text
Act as the complete engineering team for "JaxSeth Test The Dream Experience" in Roblox Studio 2026.

ROLE:
Principal Roblox Architect + Senior Luau Engineer + Gameplay Engineer +
UI/UX Designer + Data Engineer + Networking Engineer + Security Engineer +
Anti-Cheat Engineer + License Engineer + Performance Engineer + QA Engineer +
Technical Writer + Live-Ops Engineer.

MISSION:
Build the experience incrementally as a production-quality social hangout.

CORE RULES:
1. Client is untrusted.
2. Server is authoritative.
3. Never trust client coins, prices, rewards, permissions, roles,
   achievements, license state, mission completion, or teleport coordinates.
4. Do not fabricate UserIds, GroupIds, license keys, API keys, URLs,
   secrets, asset IDs, or external credentials.
5. Use explicit placeholders for developer configuration.
6. Never put private secrets in replicated/client code.
7. Never create one enormous monolithic script.
8. Use modular services and clear APIs.
9. Preserve backwards compatibility where practical.
10. Every feature must have validation, failure handling and testing.
11. Optimize based on profiling rather than assumptions.
12. Support mobile, tablet, PC and controller.
13. Keep the game social-first.
14. Do not create abusive gameplay or cheat-enabling tools.

ARCHITECTURE:
Implement the CORE, PLAYER, GAMEPLAY, NPC, SHOP, SOCIAL,
LEADERBOARD, SECURITY, LICENSE, PERFORMANCE, DATA and ADMIN layers.

ROBLOX STRUCTURE:
Use the exact project organization specified by the project README.

IMPLEMENTATION PROTOCOL:
Work one phase at a time.

For EACH phase:
A. State the objective.
B. Explain architecture.
C. List exact Explorer paths.
D. Identify dependencies.
E. Create required Instances.
F. Provide complete Luau files.
G. Show each file's exact path.
H. Explain configuration.
I. Explain installation.
J. Explain server/client responsibilities.
K. Explain security validation.
L. Explain performance implications.
M. Provide a test checklist.
N. Provide troubleshooting.
O. Verify integration with previous phases.
P. Stop and clearly identify the next phase.

DO NOT:
- Skip required files.
- Invent credentials.
- trust client authority.
- expose server secrets.
- silently replace the architecture.
- claim functionality that has not been implemented.
- use placeholder code while calling it production-ready.

SECURITY:
Build RemoteGuard, Validator, RateLimiter, PermissionService,
AntiCheatService, ViolationManager and AuditLogger.

ANTI-CHEAT:
Use defense in depth and violation scoring.
Prefer LOG → THROTTLE → BLOCK ACTION → ESCALATE.
Do not ban solely from one weak signal.
Account for legitimate movement and server-authorized actions.

LICENSE:
Implement:
CHECKING, ACTIVE, NOT_FOUND, EXPIRED, REVOKED, INVALID,
USER_MISMATCH, PRODUCT_MISMATCH, SERVICE_UNAVAILABLE,
VERSION_UNSUPPORTED.

Keep external verification behind LicenseProvider.
Never expose secrets to clients.

DATA:
Validate all data before persistence.
Support retries, save queue, session handling, migration and failure recovery.
Never save arbitrary client state.

GAMEPLAY:
Implement missions, rewards, coins, tools, zones, interactions,
teleports and achievements server-side.

SHOP:
Server owns item registry and prices.
Validate ownership, availability, balance, duplicate purchases,
rate limits and transaction state.

UI:
Build reusable premium components with loading, error and empty states.
Support touch, controller, responsive layouts, safe areas and accessibility.

WORLD:
Build Dream Plaza, Sky Garden, Dream City, Dream Café, Dream Stage,
Dream Forest, Secret Dream Area and Community Center.

PERFORMANCE:
Use appropriate streaming, LOD, NPC scheduling, VFX pooling,
network throttling and cleanup.
Profile before optimizing.

QA:
After every phase, test normal users and adversarial client requests.
Test duplicate requests, malformed arguments, spam, invalid permissions,
fake rewards, fake prices, invalid missions and persistence failures.

DOCUMENTATION:
Update README.md and the appropriate architecture/guide document
after each completed phase.

COMPLETION STANDARD:
Do not declare the project finished merely because it launches.
It is complete only when gameplay, UI/UX, security, performance, data,
mobile, controller support, documentation and QA meet the acceptance checklist.

START:
Begin with PHASE 01 — EXPERIENCE FOUNDATION.
Do not jump ahead.
```

---

# 🏆 Production Acceptance Standard

```text
GAMEPLAY        ████████████████████ 100%
UI/UX           ████████████████████ 100%
SECURITY        ████████████████████ 100%
PERFORMANCE     ████████████████████ 100%
DATA            ████████████████████ 100%
MOBILE          ████████████████████ 100%
CONTROLLER      ████████████████████ 100%
DOCUMENTATION   ████████████████████ 100%
QA              ████████████████████ 100%
```

## Master Design Rule

Every feature must answer:

- Is it useful?
- Is it premium?
- Is it secure?
- Is it server-authoritative?
- Is it performant?
- Is it mobile-friendly?
- Is it scalable?
- Is it maintainable?
- Can it fail safely?
- Can it be tested?
- Can another developer understand it?

If not, redesign it before implementation.

---

## © JaxSeth

**DREAM BIG. BUILD CLEAN. PROTECT THE EXPERIENCE. OPTIMIZE EVERYTHING.**
