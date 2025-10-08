## 1. Title

A clear, concise title for the Epic.

- _Example: GPU Usage and Optimization for Kubernetes Workloads_

## 2. Problem Statement

This section should clearly articulate the "why" behind the work.

- **What is the customer's current situation?** Describe the pain point or challenge they face today.
- **Why is the current situation not good enough?** What are the negative consequences (e.g., wasted cost, inefficiency, security risks)?
- **Who is the target customer/persona?** (e.g., Platform Engineer, FinOps Practitioner)

## 3. Vision & Goal

Describe the ideal future state for the customer once this Epic is complete.

- **What will the customer be able to achieve?**
- **How will this solve the problem outlined above?**
- **What does success look like from the customer's perspective?**

## 4. Success Criteria (Definition of Done)

This defines the scope and what must be delivered for the Epic to be considered complete.

- **Need-to-Have:** These are the binary, non-negotiable requirements. The Epic is not "done" until these are met.
    - _Example: Users can view GPU allocation data in the cost allocation dashboard._
    - _Example: The product accurately accounts for HPA behavior when making vertical scaling recommendations._
- **Nice-to-Have:** These are valuable additions that are not critical for the initial release but would be great to include if possible.
    - _Example: Users receive an automated email summary of GPU cost savings._

## 5. Market Context & Competitive Landscape

This is where we can collaborate to ensure our solution is competitive and differentiated.

- **How do competitors solve this problem today?** (e.g., what does CAST AI or other tools do?)
- **What is our unique value proposition or differentiator?**
- **What market trends are relevant here?** (e.g., the rise of AI/ML workloads on Kubernetes)

## 6. Ticket Closure Summary

To be completed when the Epic is closed. This is crucial for closing the loop.

- **Summary of what was delivered:** Briefly describe the final functionality.
- **How it solves the initial problem:** Connect the solution back to the original problem statement.
- **Final User Journey:** Describe how a user interacts with the new feature.
- **Criteria Met:** List the "Need-to-Have" and "Nice-to-Have" items that were completed.

---

## Story Template

Stories that roll up to an Epic can be simpler but should still connect to the overall goal.

- **Goal:** What part of the Epic's vision does this story accomplish?
- **User Story:** As a [Persona], I want to [Action] so that I can [Achieve Outcome].
- **Tasks:** A checklist of technical tasks required to complete the story.
- **Acceptance Criteria:** How we'll verify the story is working as intended.

---

## Bug Fix / Minor Task Template

For smaller items like the **HPA reliability fix**, a lightweight template is sufficient. We don't need a full strategic brief for bug fixes.

- **Issue:** What is the reported problem or unexpected behavior?
- **Expected Behavior:** How is the feature supposed to work?
- **Resolution:** What was done to fix the issue? This can be used directly in release notes.