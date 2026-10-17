---
name: art-bible-explore
description: Generate candidate images, models, video, sound, music or writing from a project's references. Use for broad artistic exploration, comparisons between models or focused revisions after feedback; deliver actual candidates and carry a requested taste pass through to review.
license: MIT
metadata:
  author: Spencer MacBeth
  version: "0.4.0"
---

# Make alternatives worth comparing

Use the user's references and the current art bible to generate work they can inspect. Preserve the properties they have already chosen.

## Choose what to explore

For early exploration, make the directions substantially different. Change structure, silhouette, composition, materials, atmosphere, instrumentation or writing voice as appropriate. A suspended fabric shelter, a carved stone chamber and exposed industrial framing explore different possibilities; recoloring the same room does not.

Explain briefly what each direction takes from its seeds. Let the user combine properties from several candidates in a later pass. For refinement, keep the accepted properties and vary the unresolved ones.

Treat model choice as part of the exploration. Compare promising models on a shared subject when the task warrants it, using the controls each actually supports. Separate a preference for a direction from a preference for the model that happened to generate it.

## Generate the work

Use the project's generation tools and chosen providers, or implement the needed API calls in the user's project. A platform offering several models can make comparisons convenient. Choose models for the medium and task, and use their reference inputs and controls deliberately: composition, duration, motion, instrumentation or geometry requirements can change the result substantially.

Keep the references, model and useful settings with each candidate so a successful direction can be developed further. Preserve original outputs and keep source images beside derived models. When the workflow uses concept selection before image-to-3D, present the concepts before reconstructing them.

## Put the results in front of the user

If the task includes a taste pass, load the candidates into the existing review interface or build a suitable local one. Run it, check that the actual files display or play, and give the user the working link. Include the seed references and a short description of what differs between candidates.

If the user requested assets only, deliver the files and enough context to compare them. Keep the presentation centered on the creative differences and the decision the user is making.

[Example exploration and model-connection requests](references/prompts.md).
