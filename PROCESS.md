# Contribution Process

Thank you for your interest in contributing to our project!

## Getting started

Our contribution protocol is built upon three core principles:   
1. **Goal** – a business goal describes the proposed solution to a problem in the market. This could be a new product, a new service, or an additional feature to an existing product or service.   
2. **Problem** – an observed matter or situation regarded as unsatisfactory AND is an obstacle in the way of acheiving the business goal.   
3. **Solution** –  the actual deliverable which resolves the problem.

> [!NOTE]
> This guide provides an overview of the contribution workflow: from finding a Goal, identifying a Problem, and the process of delivering your solutions.

### Goal

As soon as you get involved in one of our projects, you must understand the goal you are working on by:

1. investigating any conversations and related documents
1. understanding how things are already moving towards achieving the goal 

It's crucial to understand the business context of the goal and how achieving the goal will impact the organization.

> [!NOTE]
> A Goal is represented as a GitHub issue in the relevant repository and has the following naming pattern: `Goal: [statement]`.  
> Goals are created and curated by the product coordinator.

### Problem

Once the Goal is clear, you must identify what stops you from achieving it. Anything that is stopping you - is a “Problem”. A typical question to ask is: "Why is this Goal not achieved and what is the Problem?".

Sometimes, a Goal already has a few identified problems, but not always.

> [!NOTE]
> Once a Problem is identified, we log it as a Github issue with the following naming pattern: `Problem: [statement]`.  
> We’re counting on our contributors to identify problems. Keep a Problem title short (under 65 chars) and crystal clear.

Make sure each Problem issue is interlinked with it's Goal issue:
- add a Problem issue link into the Goal description
- add a Goal issue link to the Problem description

It's essential to maintain clear links between Goals and related Problem issues. This helps everyone stay informed and team members can easily track progress and understand the context.

Problems that are too big to solve in 3-4 hours need to be decomposed into smaller Problems, which must be interlinked with the goal and the parent problem.

### Solution

The third pillar of successful contribution is the Solution.

Different problems may require different sets of skills.  
Whether it’s code, design, or marketing material, we expect a lean and clean solution from the contributor.

> [!NOTE]
> Solution is presented in GitHub as [Pull Requests (PR)](https://docs.github.com/en/pull-requests) in compliance with [PR Requirements](#pr-requirements).

# PR Requirements
All PRs, whether for source code, design, or copy changes, must comply with our PR Requirements.

> [!WARNING]
> PRs that do not correspond to the following criteria are usually rejected.

## Workflow
1. Assign yourself to the problem you are solving (in the issue tracker). This communicates to others that you are starting work and that they should not work on the same problem.
2. Follow the [step-by-step instructions](#) for forking the repo, creating your own local branch, and sending a pull request back to `main`.
3. Report the time spent by including a line in the PR: `time spent: xxx minutes`

> [!NOTE]
> When contributing, it's essential to report time accurately, including all stages of development (planning, implementation, QA). Programming and designing isn't just about writing code or creating designs; it also involves research, planning, and QA. 
> 


## Scoping

You must be able to complete your PR within 3-4 hours.  

If the solution requires more time, then decompose the problem into smaller independent child problems and interlink them with the original problem. 

If your PR can't be used in production until the parent problem is fully resolved, use feature flags.

When creating a PR, you must [link it](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword) to the corresponding Problem (issue).

### Design PRs

Create a PR with a modification to the DESIGN.md file detailing the design aspects being addressed. 
Design PRs use `docs(ui)` as the "type" and "scope" of its name. i.e.: `docs(ui) problem: no designs for table component`

Structure the design file with the following markup

```
## Feature
- [/page](https://figma.com/your-design-file-url)
  - ./page/{params} 
    - (group)
      - [[state]](https://figma.com/your-design-file-url)
```
#### Key:
- **`/...`** - Represents a page.
- **`{...}`** - Represents a dynamic parameter within a URL.
- **`(...)`** - Used for grouping related features or components.
- **`[...]`** - Indicates a specific state of the page or component, such as a popup or modal state.

- Indentation in the list represents the tree structure or hierarchy, showing how components or features are nested or related.

Example:
```
## Time Vaults
- [/lending](https://figma.com/your-design-file-url)
  - ./vaults/{poolAddr} 
    - (Auction)
      - [[Withdraw Popup]](https://figma.com/your-design-file-url)
      - [[Bid Popup]](https://figma.com/your-design-file-url)
```

If there isn't an existing DESIGN.md file:

1. Create a new file named DESIGN.md.
1. Link it from README.md.


#### Code Quality and Reviews
We use the following metrics when judging PRs:
1. Is this the simplest possible solution to the problem? Could less lines of code be used?
2. Does this add any additional learning curve for the end user?
3. Does this introduce any new problems?
