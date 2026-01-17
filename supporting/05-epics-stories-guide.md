# Epics & Stories Writing Guide

A reference guide for the Epics & Stories Agent to create Spec-Kit compatible output.

---

## Core Principle: WHAT, Not HOW

### ✅ Good (WHAT - Observable Outcomes)
- "User can create an account with email and password"
- "User sees their profile picture on the dashboard"
- "User receives email confirmation within 5 minutes"
- "Error message displays when password is less than 8 characters"
- "Data loads within 2 seconds"
- "User stays logged in for 7 days"

### ❌ Bad (HOW - Implementation Details)
- "System stores user data in PostgreSQL"
- "Implement JWT authentication with RS256"
- "Use React Query for data fetching"
- "Create users table with email column"
- "Deploy to AWS Lambda"
- "Use SendGrid API for emails"

---

## Epic Design Principles

### 1. User Value Focus
Each Epic should deliver standalone value to users.

**Good Epic:** "User Authentication" - Users can securely access their accounts
**Bad Epic:** "Database Setup" - Technical task, no direct user value

### 2. Logical Cohesion
Group related functionality together.

**Good:** All registration, login, password reset in "User Authentication" Epic
**Bad:** Mixing unrelated features in one Epic

### 3. Independence
Epics should be workable without waiting for others (where possible).

**Good:** "User Profile" Epic can start after basic auth is done
**Bad:** Epic that requires 5 other Epics to be complete first

### 4. Right Size
- Too small: "Add login button" (that's a task, not an Epic)
- Too big: "Build entire application" (that's the whole project)
- Just right: "User Authentication" (3-8 stories, 1-2 weeks work)

---

## Story Sizing Guide

### Ideal Story Size: 1-3 Days

| Too Small | Just Right | Too Big |
|-----------|------------|---------|
| "Add button" | "User can register with email" | "Complete user management system" |
| "Change color" | "User can reset password via email" | "Build authentication + authorization + admin" |
| "Fix typo" | "User can update profile information" | "Implement all dashboard features" |

### Splitting Large Stories

**Before (Too Big):**
> "As a user, I want to manage my account settings"

**After (Split):**
1. "As a user, I want to update my display name"
2. "As a user, I want to change my email address"
3. "As a user, I want to update my password"
4. "As a user, I want to delete my account"

---

## User Story Template

```markdown
**User Story:**
As a [user role],
I want [goal/desire],
So that [benefit/value].

**Acceptance Criteria:**
- [ ] [Observable outcome 1]
- [ ] [Observable outcome 2]
- [ ] [Edge case handling]
- [ ] [Error scenario handling]
```

### User Role Examples
- New user (first-time visitor)
- Registered user
- Returning user
- Team admin
- Team member
- Guest user
- System administrator

### Goal Examples (WHAT)
- Create an account
- Log into my account
- Reset my forgotten password
- Update my profile information
- Invite team members
- View my activity history

### Benefit Examples (WHY)
- So that I can access the platform
- So that I can continue where I left off
- So that I can regain access to my account
- So that my profile reflects current information
- So that my colleagues can collaborate with me

---

## Acceptance Criteria Guidelines

### Characteristics of Good Criteria
1. **Observable** - Can be seen/verified by a user
2. **Specific** - No ambiguity
3. **Testable** - Clear pass/fail
4. **Independent** - Each criterion stands alone

### Format Options

**Checklist Style (Recommended for Spec-Kit):**
```
- [ ] User can enter email address
- [ ] User can enter password
- [ ] Password field masks input
- [ ] "Create Account" button is visible
- [ ] Error shows if email is invalid
- [ ] Error shows if password < 8 characters
- [ ] Success message appears after registration
- [ ] Confirmation email arrives within 5 minutes
```

**Given-When-Then Style:**
```
Given I am on the registration page
When I enter a valid email and password
And I click "Create Account"
Then my account is created
And I see a success message
And I receive a confirmation email
```

---

## Common Acceptance Criteria Patterns

### Form Input
- [ ] User can enter [field name]
- [ ] [Field] accepts [valid input types]
- [ ] [Field] shows error for [invalid input]
- [ ] [Field] has maximum length of [X] characters
- [ ] Required fields are marked with indicator

### Actions/Buttons
- [ ] [Button] is visible on [page/section]
- [ ] [Button] is disabled until [condition]
- [ ] Clicking [button] triggers [action]
- [ ] Loading indicator shows during [action]
- [ ] Success message appears after [action]

### Display/View
- [ ] [Data] is visible on [page/section]
- [ ] [List] shows maximum [X] items per page
- [ ] [Content] loads within [X] seconds
- [ ] Empty state message shows when no [data]

### Validation/Error
- [ ] Error message "[text]" shows when [condition]
- [ ] Error message disappears when [correction made]
- [ ] User can retry after error
- [ ] Form preserves entered data after error

### Email/Notification
- [ ] [Notification type] is sent within [timeframe]
- [ ] [Email] contains [required information]
- [ ] User can [action] from notification

---

## Epic Structure Template

```markdown
## Epic [N]: [Epic Title]

### Overview
[1-2 sentences describing the user value this Epic delivers]

### Stories

#### Story [N].1: [Story Title]
**User Story:** As a [role], I want [goal] so that [benefit].

**Acceptance Criteria:**
- [ ] [Criterion 1]
- [ ] [Criterion 2]
- [ ] [Criterion 3]

---

#### Story [N].2: [Story Title]
**User Story:** As a [role], I want [goal] so that [benefit].

**Acceptance Criteria:**
- [ ] [Criterion 1]
- [ ] [Criterion 2]

---
```

---

## Requirements Coverage Mapping

Ensure every Functional Requirement (FR) from PRD is covered:

```markdown
## Requirements Coverage

| FR ID | Requirement | Covered By |
|-------|-------------|------------|
| FR-01 | User registration | Epic 1, Story 1.1 |
| FR-02 | User login | Epic 1, Story 1.2 |
| FR-03 | Password reset | Epic 1, Story 1.3 |
| FR-04 | Profile update | Epic 2, Story 2.1 |
```

### Coverage Checklist
- [ ] Every FR has at least one Story
- [ ] No orphan Stories (all link to FRs)
- [ ] NFRs are addressed in relevant Stories' criteria

---

## Dependency Management

### Epic Dependencies
```
Epic 1: User Authentication (Foundation)
    └── Epic 2: User Profile (needs auth)
           └── Epic 3: Team Management (needs profile)
```

### Story Dependencies
Keep dependencies minimal. If Story B depends on Story A:

| Story | Depends On | Reason |
|-------|------------|--------|
| Story 2.1 | Story 1.1 | Needs user to be registered |
| Story 3.1 | Story 2.1 | Needs profile to exist |

### Reducing Dependencies
- Can we make this Story work with mock data first?
- Can we split the Story to remove the dependency?
- Is the dependency truly necessary or just convenient?

---

## Quality Checklist

Before finalizing Epics & Stories:

### Epic Level
- [ ] Each Epic delivers clear user value
- [ ] Epics are logically cohesive
- [ ] Epic order reflects priority and dependencies
- [ ] All FRs from PRD are covered

### Story Level
- [ ] Each Story is 1-3 days of work
- [ ] User Story format is complete (role, goal, benefit)
- [ ] Acceptance Criteria are observable (WHAT, not HOW)
- [ ] Edge cases are covered
- [ ] Error scenarios are included

### Spec-Kit Compatibility
- [ ] No implementation details in criteria
- [ ] Language is user-centric
- [ ] Criteria are testable without knowing implementation
- [ ] Each criterion is independently verifiable
