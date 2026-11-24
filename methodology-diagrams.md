# Methodology diagrams, both directions

## 1. §2 core loop: current (outer TB, stages LR)

```mermaid
---
config:
  layout: dagre
---
flowchart TB
  subgraph before [Before you build]
    direction LR
    explore[Explore] --> plan[Plan] --> challenge[Challenge] --> persist[Persist plan]
    challenge -. rethink .-> plan
  end
  subgraph build [Build]
    direction LR
    execute[Execute] --> review[Review] --> accept[Accept] --> status[Update status]
    accept -. not done .-> execute
  end
  before --> build
  build -. plan end .-> retro[Retro: config changes]
```

End of chart 1.

## 2. §2 core loop: outer TB, stages TB

```mermaid
---
config:
  layout: dagre
---
flowchart TB
  subgraph before [Before you build]
    direction TB
    explore[Explore] --> plan[Plan] --> challenge[Challenge] --> persist[Persist plan]
    challenge -. rethink .-> plan
  end
  subgraph build [Build]
    direction TB
    execute[Execute] --> review[Review] --> accept[Accept] --> status[Update status]
    accept -. not done .-> execute
  end
  before --> build
  build -. plan end .-> retro[Retro: config changes]
```

End of chart 2.

## 3. §2 core loop: outer LR, stages LR

```mermaid
---
config:
  layout: dagre
---
flowchart LR
  subgraph before [Before you build]
    direction LR
    explore[Explore] --> plan[Plan] --> challenge[Challenge] --> persist[Persist plan]
    challenge -. rethink .-> plan
  end
  subgraph build [Build]
    direction LR
    execute[Execute] --> review[Review] --> accept[Accept] --> status[Update status]
    accept -. not done .-> execute
  end
  before --> build
  build -. plan end .-> retro[Retro: config changes]
```

End of chart 3.

## 4. §2 core loop: outer LR, stages TB

```mermaid
---
config:
  layout: dagre
---
flowchart LR
  subgraph before [Before you build]
    direction TB
    explore[Explore] --> plan[Plan] --> challenge[Challenge] --> persist[Persist plan]
    challenge -. rethink .-> plan
  end
  subgraph build [Build]
    direction TB
    execute[Execute] --> review[Review] --> accept[Accept] --> status[Update status]
    accept -. not done .-> execute
  end
  before --> build
  build -. plan end .-> retro[Retro: config changes]
```

End of chart 4.

## 5. §6 hook flow: current (LR)

```mermaid
---
config:
  layout: dagre
---
flowchart LR
  call[Tool call] --> guard{PreToolUse guard}
  guard -- "exit 2: reason to Claude" --> blocked[Blocked]
  guard -- "ask: reason to you" --> you{You}
  guard -- no decision --> perms{Permissions}
  perms -- denied --> blocked
  perms -- prompt --> you
  perms -- allowed --> run[Tool runs]
  you -- deny --> blocked
  you -- allow --> run
  run --> check[PostToolUse check] --> result[Result to Claude]
```

End of chart 5.

## 6. §6 hook flow: TB

```mermaid
---
config:
  layout: dagre
---
flowchart TB
  call[Tool call] --> guard{PreToolUse guard}
  guard -- "exit 2: reason to Claude" --> blocked[Blocked]
  guard -- "ask: reason to you" --> you{You}
  guard -- no decision --> perms{Permissions}
  perms -- denied --> blocked
  perms -- prompt --> you
  perms -- allowed --> run[Tool runs]
  you -- deny --> blocked
  you -- allow --> run
  run --> check[PostToolUse check] --> result[Result to Claude]
```

End of chart 6.
