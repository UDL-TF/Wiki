# Task Lists

Task lists (also called checklists) allow you to create a list of items with checkboxes. They're particularly useful for tracking progress on projects, creating to-do lists, and documenting requirements.

## Creating Task Lists

To create a task list, add dashes (-) and brackets with a space ([ ]) in front of task list items. To mark a task as complete, put an x inside the brackets ([x]).

```markdown
- [x] Completed task
- [ ] Incomplete task
- [ ] Another incomplete task
```

**Output**:

- [x] Completed task
- [ ] Incomplete task
- [ ] Another incomplete task

## Nested Task Lists

You can create nested task lists by indenting items.

```markdown
- [x] Main task
  - [x] Subtask 1
  - [ ] Subtask 2
- [ ] Another main task
  - [ ] Subtask 1
  - [ ] Subtask 2
```

**Output**:

- [x] Main task
  - [x] Subtask 1
  - [ ] Subtask 2
- [ ] Another main task
  - [ ] Subtask 1
  - [ ] Subtask 2

## Task Lists in Different Contexts

### Project Planning

```markdown
## Project Milestones

- [x] Project setup
  - [x] Initialize repository
  - [x] Configure build system
- [ ] Development
  - [x] Implement core features
  - [ ] Add documentation
  - [ ] Write tests
- [ ] Release
  - [ ] Create release notes
  - [ ] Deploy to production
```

**Output**:

## Project Milestones

- [x] Project setup
  - [x] Initialize repository
  - [x] Configure build system
- [ ] Development
  - [x] Implement core features
  - [ ] Add documentation
  - [ ] Write tests
- [ ] Release
  - [ ] Create release notes
  - [ ] Deploy to production

### Bug Tracking

```markdown
## Bug Fixes for v1.2

- [x] Fix login issue (#123)
- [x] Resolve database connection timeout (#124)
- [ ] Address UI rendering bug (#125)
- [ ] Fix API response format (#126)
```

**Output**:

## Bug Fixes for v1.2

- [x] Fix login issue (#123)
- [x] Resolve database connection timeout (#124)
- [ ] Address UI rendering bug (#125)
- [ ] Fix API response format (#126)

### Feature Checklist

```markdown
## New Feature Requirements

- [ ] User authentication
  - [x] Login page
  - [x] Registration page
  - [ ] Password reset
  - [ ] Email verification
- [ ] User profile
  - [ ] Profile page
  - [ ] Edit profile
  - [ ] Upload avatar
```

**Output**:

## New Feature Requirements

- [ ] User authentication
  - [x] Login page
  - [x] Registration page
  - [ ] Password reset
  - [ ] Email verification
- [ ] User profile
  - [ ] Profile page
  - [ ] Edit profile
  - [ ] Upload avatar

## Interactive Task Lists

On platforms like GitHub, GitLab, and similar services, task lists are often interactive. Users can click checkboxes directly in the rendered Markdown to toggle task completion.

!!! info
    When you check a task in an interactive task list on GitHub, the Markdown source is automatically updated.

## Formatting Within Task Lists

You can use other Markdown formatting within task list items.

```markdown
- [x] **Important**: Complete the documentation
- [ ] *Optional*: Add more examples
- [ ] Review the `configuration.md` file
- [x] Check out [this reference](https://example.com)
```

**Output**:

- [x] **Important**: Complete the documentation
- [ ] *Optional*: Add more examples
- [ ] Review the `configuration.md` file
- [x] Check out [this reference](https://example.com)

## Best Practices

1. **Be specific**: Write clear, actionable tasks
2. **Use hierarchy**: Organize related tasks with nesting
3. **Update regularly**: Keep your task lists current
4. **Limit scope**: Don't create overly long task lists
5. **Combine with issues**: Link tasks to issue trackers for better management

## Limitations

- Not all Markdown processors support task lists
- Some platforms don't support interactive checkboxes
- The syntax may vary slightly between different implementations

!!! warning
    Task lists are an extension to the original Markdown specification and may not work in all Markdown processors.
