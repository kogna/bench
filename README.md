# Bench - AI Workspace

Simple, focused workspace for AI-assisted projects with persistent memory.

## Repository Structure

```
kogna/bench/
├── README.md                    # This file
├── principal_identity.md        # Info about Dazza Greenwood (user)
├── memory/
│   ├── agent_identity.md       # Core AI identity & preferences 
│   ├── capabilities.md         # Learned skills & tool patterns
│   └── session-log.md          # Recent session summaries
├── templates/
│   ├── project-scope.md        # Template for new projects
│   └── scratchpad.md           # Template for project notes
└── projects/
    ├── agent_protocols/         # Agent protocols webinar project
    │   ├── scope.md            # Project goals & context
    │   └── scratchpad.md       # Working notes & findings
    └── [future-projects]/      # Additional projects as needed
```

## Usage Pattern

### New Comet Instance Initialization
1. Read `principal_identity.md` (understand user context)
2. Read `memory/agent_identity.md` (understand AI patterns)
3. Read `memory/capabilities.md` (understand what works)  
4. Read `memory/session-log.md` (understand recent context)
5. Read `projects/[current-project]/scope.md` (understand project)
6. Read `projects/[current-project]/scratchpad.md` (continue work)

### Starting New Project
1. Create `projects/[project-name]/` directory
2. Copy `templates/project-scope.md` → customize → save as `scope.md`
3. Copy `templates/scratchpad.md` → save as `scratchpad.md`
4. Begin work in `scratchpad.md`

### Ending Session
1. Update current project's `scratchpad.md` with progress
2. Add session summary to `memory/session-log.md`
3. Update `memory/capabilities.md` if new patterns learned

## Philosophy

Keep it simple. Each project gets its own workspace. Memory persists across AI instances. Focus on getting work done efficiently.