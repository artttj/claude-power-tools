# Example: Brainstorming a New Feature

## Scenario

You want to add a real-time chat feature to your application.

## Workflow

### Step 1: Activate Brainstorming Skill

```bash
/brainstorming I want to add real-time chat to my React app
```

### Step 2: Answer Clarifying Questions

The skill will ask:
- What's the scale? (1:1, group, broadcast)
- What's the persistence requirement?
- Do you need message history?
- Any offline support?

### Step 3: Review Approaches

The skill presents options:
- **A)** WebSockets with custom server
- **B)** Server-Sent Events + polling
- **C)** Third-party service (Pusher, Ably)

### Step 4: Get Design Spec

The skill outputs a markdown spec with:
- Architecture diagram
- API endpoints needed
- Component structure
- Data flow

### Step 5: Move to Implementation

Use the design spec with `/writing-plans` to create the implementation plan.

## Key Takeaway

Brainstorming prevents premature implementation by forcing you to think through requirements before writing code.
