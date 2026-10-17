---
name: art-bible-lock
description: Apply the user's taste-pass feedback, make the next iteration and record chosen direction in the art bible. Use after a review, when carrying an established direction across tasks, or when turning a recorded playthrough into follow-up work.
license: MIT
metadata:
  author: Spencer MacBeth
  version: "0.4.0"
---

# Use the feedback and keep moving

Read the user's notes alongside the candidates they reviewed. Carry their choices into the next iteration and the art bible so subsequent work builds on them.

## Understand what they liked

Keep their observations separate from your proposed solution. "Keep the hanging shape, but the metal is too shiny" means preserve the shape and change the surface. It does not ask for a new object. If they like different properties from several candidates, use that combination to guide the next pass.

Read actual feedback files or exports. Do not treat a high score, an agent recommendation or a filename containing `final` as a broader decision than the user made. Ask when a meaningful choice is genuinely ambiguous; continue with the revisions that are clear.

## Make the next version

Implement the requested changes. Work at the level responsible for the problem: the source artwork, geometry, placement, lighting, editing, mix or the review presentation itself. Reuse good work instead of regenerating everything.

Keep the earlier candidates and notes, give changed media a new revision, and put the new results back into the taste pass. Run it and return a working link with a short explanation of what changed. A request to iterate is work to carry out, not just a brief to leave behind.

## Record the direction the user chooses

Update the relevant bible section with the chosen examples, what to preserve, what to avoid and the recipe needed to make more work like it. Link the actual images, models, recordings or scenes. Keep unresolved properties visible. A selected concept can guide the next model without implying that its geometry or in-game presentation has been reviewed.

Keep the bible readable. Move contradictory old guidance into a dated history with the reason it changed. Use the optional [decision template](assets/decision.md) or the project's existing format when a decision needs more explanation. Check that the normal project instructions lead a new agent to the current direction.

## Carry the direction into production

Use the accepted work in a representative part of the game and inspect it in context. For parallel work, give each task the relevant bible revision and references, a clear area to change and its own output location. Changes to shared direction should be brought back for review rather than silently redefining it for other tasks.

Build or extend a playable slice when that is part of the request. The user needs to play it repeatedly to judge how the art, interface, sound and pacing come together.

For a recorded playthrough or spoken feedback, make follow-up tasks tied to the relevant moments. Preserve what the user experienced: "I couldn't tell whose turn it was" is the problem; a new animation is one possible fix. Implement requested changes within the task's scope, update the bible where the feedback changes shared direction, and say what to play again to check the result.

[The fictional worked pass](references/worked-pass.md) illustrates partial choices and refinement. [Example iteration and play-session requests](references/prompts.md) provide starting points.
