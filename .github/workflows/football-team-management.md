---
description: Complete football team management using agentic workflow in VS Code. Handles player roster, match scheduling, training sessions, performance tracking, communication, and tactical management. All data is stored in YAML files in the repository.
on:
  workflow_dispatch:
roles: all
permissions:
  contents: read
  issues: read
  pull-requests: read
tools:
  github:
    toolsets: [default]
safe-outputs:
  create-pull-request:
  add-comment:
---

# Football Team Management Agent

You are an AI agent managing a football team. Your primary task is to initialize and manage the team's data structure.

## Your Initial Task

When first triggered, create the complete football team management structure by creating these YAML files in the `data/` directory:

### 1. **data/roster.yaml** - Player roster
```yaml
team_name: "Football Team"
created_at: "2026-02-14"
players:
  - id: 1
    name: "Player Example"
    position: "Midfielder"
    number: 10
    status: "active"
```

### 2. **data/matches.yaml** - Match schedule
```yaml
matches:
  - id: 1
    opponent: "Opponent Team"
    date: "2026-03-01"
    time: "19:00"
    location: "Home"
    status: "scheduled"
```

### 3. **data/training.yaml** - Training sessions
```yaml
training_sessions:
  - id: 1
    date: "2026-02-15"
    type: "Regular Practice"
    focus: "Offensive Tactics"
    duration_minutes: 90
```

### 4. **data/performance.yaml** - Player performance stats
```yaml
performance:
  - player_id: 1
    matches_played: 0
    goals: 0
    assists: 0
    rating: 0
```

### 5. **data/communication.yaml** - Team communications and logs
```yaml
logs:
  - timestamp: "2026-02-14T21:00:00Z"
    type: "System"
    message: "Football team management system initialized"
```

### 6. **data/tactics.yaml** - Tactical plans
```yaml
tactics:
  - id: 1
    name: "Default Formation"
    formation: "4-3-3"
    description: "Standard attacking formation"
```

## Instructions

1. Check if the `data/` directory exists; if not, create it
2. Create all 6 YAML files with the template structure above
3. Create a Pull Request with all these new files
4. Add a comment summarizing what was created

## Safe Outputs

- Use `create-pull-request` to submit the new data files
- Use `add-comment` to confirm completion

## Important Notes

- All files should be well-structured YAML
- The `data/` directory should be at the repository root
- Each YAML file represents a different aspect of team management
- Future workflows can read and update these files

