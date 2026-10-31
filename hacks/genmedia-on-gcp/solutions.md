# New Citizen of Cymbal Circuit: From Concept to Creation with GenMedia

## Introduction

Welcome to the coach's guide for the *New Citizen of Cymbal Circuit: From Concept to Creation with GenMedia* gHack. Here you will find links to specific guidance for coaches for each of the challenges.

> [!NOTE]  
> If you are a gHacks participant, this is the answer guide. Don't cheat yourself by looking at this guide during the hack!

## Coach's Guides

- Challenge 1: From Idea to Character Narrative
- Challenge 2: The Visual Blueprint
- Challenge 3: From Stills to Motion
- Challenge 4: The Assembly
- Challenge 5: Giving It a Voice
- Challenge 6: The Soundtrack

## Challenge 1: From Idea to Character Narrative

### Notes & Guidance

If the participants are using Agent Platform Studio for generating the character backstory and scene descriptions, encourage them to turn on auto-save or keep their final outputs in a shared Google Doc. This way they can keep track of their progress and easily hand over the generated descriptions to the next driver.

> [!NOTE]  
> As mentioned in the instructions, using Gemini is fair game, but using the first response verbatim often leads to generic outputs (like yet another architect named Elara). Adding their own creative twist or iterating a couple of times produces much stronger character concepts.

It is helpful for teams to set clear context or system instructions when using Gemini so the generated material fits *Cymbal Circuit*:

```text
We are creating a 45-60 second animated character teaser introducing a brand-new citizen to the series Cymbal Circuit. Set in Cymbal Arcology—split between sunlit, bio-engineered Cymbal Green above and neon-drenched Circuit Ward below, with siblings Ori and Rook running a border transit hub—help us design a distinctive, visually memorable character and scene breakdown.
```

Although it's subjective to assess creative deliverables, teams' outputs should be consistent, coherent, faithful to the *Cymbal Circuit* setting, and concise.

We're expecting *at least* three scenes, and having 5-7 shorter, focused shots works best for a 45-60 second teaser. Video generation models struggle when too many distinct events are crammed into a single clip:

> Attempting to prompt "A courier leaps off a sky-garden balcony, rides a cargo lift into Circuit Ward, and haggles with a synth-bot merchant" in a single clip will likely result in a muddled or incomplete sequence. Instead, break each beat into its own focused storyboard scene and video clip.

Encourage teams to spotlight *their new character* visually rather than trying to design full reference sheets for Ori, Rook, and an entire cast—ties to Ori and Rook's transit hub can easily be woven in through setting details or voice-over narration.

#### Pro Tips for the Students

- Take **5-10 mins** with your team discussing who your character is, whether they belong to *Cymbal Green*, *Circuit Ward*, or the border between them, and what animation style fits best. Be creative and don't overthink!
- Focus on your story and keep in mind that you have 45-60 seconds to tell it. Keep each scene focused on one clear action or moment.
- Parallelize your work:
  - One person can work on the Character Core Identity and detailed physical/wardrobe description.
  - One person on Animation Style and Color Palette—contrast the warm sunlit greens/golds of *Cymbal Green* with the electric magentas/cyans of *Circuit Ward*. [Cinema palette inspiration here](https://digitalsynopsis.com/design/cinema-palettes-famous-movie-colors/).
  - Rest of the team on the scene-by-scene storyline, title card, and stinger.

## Challenge 2: The Visual Blueprint

### Notes & Guidance

Participants should take their descriptions from Challenge 1 and use either Gemini or the *AI-powered prompt writing* capabilities in Agent Platform Studio to craft image generation prompts. *Gemini Native Image* (aka *Nano Banana*) should be used both to establish the initial character look and to generate multi-angle views (or a combined character contact sheet).

> [!IMPORTANT]  
> Participants should avoid using the *Imagen* family of models for iterative multi-angle character sheets, as *Gemini Native Image* (aka *Nano Banana*) is much better suited for conversational subject consistency across shots.

For storyboard scene generation, *Nano Banana* is again the recommended choice. Teams should supply their character reference image(s) (or contact sheet) alongside each scene description to generate 16:9 storyboard frames.

> [!WARNING]  
> Keep an eye on request payload and reference image limits in Agent Platform Studio. Including too many large images in a single conversation or exceeding the model's per-prompt reference image limit can cause errors or cause extra images to be ignored. Encourage participants to combine angles into a single contact sheet, start fresh conversations per scene when needed, and import assets directly from their Cloud Storage bucket.

#### Pro Tips for the Students

- The more specific the visual details from Challenge 1 (silhouette, clothing, colors, signature props), the more consistent your character will look across storyboard frames.
- Keep compositions clean and make sure every storyboard frame is generated in **16:9** format so it maps directly to Challenge 3's video generation.
- Google models enforce IP and Safety filters strictly. Do **not** reference real people, trademarked animation studios, or copyrighted film/show characters—describe the visual style directly instead (e.g., "painterly 2.5D cel-shaded animation with expressive brushwork").
- Generate a clean title card or graphic overlay asset if you want to feature your character's name and stinger visually in Challenge 4.

## Challenge 3: From Stills to Motion

### Notes & Guidance

The 16:9 storyboard images and character sheet created in Challenge 2 **must** be used as visual references (such as start/end frames or subject references) when prompting the *Gemini Omni Flash* family of models in Agent Platform Studio. If participants skip image references and rely on text alone, their character's appearance will drift between clips. **DO NOT** let teams struggle too long before checking how they are passing reference images.

Remind teams that if they want on-screen lip-synced dialogue spoken directly by their character, they should include that dialogue in the *Gemini Omni Flash* video prompt at generation time; narrator voice-overs and off-screen lines will be layered in during Challenge 5.

#### Pro Tips for the Students

- Video generation takes time—parallelize scenes across **two or three team members** simultaneously, then compare and pick the best clips in your shared Cloud Storage bucket.
- For smoother shot-to-shot continuity between consecutive beats, consider using the final frame of Scene 1 as the starting frame for Scene 2.
- Review the [Generate videos with Agent Platform](https://docs.cloud.google.com/gemini-enterprise-agent-platform/models/video/overview) docs and the [Omni Prompting Guide](https://deepmind.google/models/gemini-omni/prompt-guide/) to direct camera movement, lighting, and character motion clearly.
- Keep prompts free of real actors, directors, copyrighted franchises, or studio names so IP and safety filters don't block video generation.
- If a character's design drifts in a clip, return to Challenge 2 to refine the reference frame rather than fighting the video prompt alone.

## Challenge 4: The Assembly

### Notes & Guidance

In the remaining challenges, teams assemble their final 45-60 second character teaser. Unless a team member already prefers a local non-linear editor (DaVinci Resolve, Premiere Pro, Final Cut Pro, CapCut, iMovie), strongly recommend **Google Vids**.

Google Vids is a web-based video creation app that makes assembling clips, text overlays, and multi-track audio as approachable as editing a slide deck, with no prior video editing experience required.

#### Pro Tips for the Students

- Focus first on visual pacing, clean cuts, and narrative flow across your 45-60 second timeline—voice-over and music will be layered in Challenges 5 and 6.
- Add your character's title card and stinger text at the end using either Challenge 2 graphics or built-in text overlays in your video editor.

## Challenge 5: Giving It a Voice

### Notes & Guidance

Participants will use **Gemini TTS** in Agent Platform Studio to generate the voice-over tracks for their teaser. Unlike traditional text-to-speech engines that only read text in a fixed preset tone, Gemini TTS operates as an expressive generative voice model: teams can direct vocal persona, emotional delivery, and pacing using natural-language style instructions alongside their script (for example, *"Speak in a wry, streetwise tone with quick, energetic pacing, like an undercity fixer introducing a rival"*).

#### Pro Tips for the Students

- Break the voice-over into short per-scene clips rather than one monolithic audio file—it makes timing and alignment on the video editor timeline much easier.
- Review the [Prompting tips for Gemini Text to Speech](https://docs.cloud.google.com/text-to-speech/docs/gemini-tts#prompting_tips) to control tone, emphasis, and pacing.
- Layer the generated audio tracks onto your timeline in Google Vids (or your chosen editor) so they land cleanly on the right visual beats without clashing with any on-screen dialogue from Challenge 3.

## Challenge 6: The Soundtrack

### Notes & Guidance

Participants will use **Lyria** in Agent Platform Studio to compose custom background music for their 45-60 second teaser. Because Lyria responds best to musical and instrumental terminology, coach teams to describe specific instruments, tempo, and mood rather than story plot points (for example, blending warm acoustic plucks and airy flutes for *Cymbal Green* with pulsing analog synth bass and crisp electronic percussion for *Circuit Ward*).

Remind teams to duck or lower the soundtrack volume in their video editor so the voice-over from Challenge 5 remains clear and intelligible, then export the finished teaser as an **MP4** file.
