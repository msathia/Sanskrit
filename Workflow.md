# Sanskrit Study Workflow

## Terminal Rendering

Current local checks:

```text
locale: UTF-8
tmux: 3.6b
TERM inside tmux: tmux-256color
```

This is a good base. For Sanskrit, the main rendering issue is usually the terminal emulator and font, not tmux itself.

Recommended setup:

- Use a terminal with good Unicode shaping and font fallback.
- Use a coding font for Latin text and a proper Devanagari fallback font for Sanskrit.
- Good Devanagari fallback choices: `Noto Sans Devanagari`, `Noto Serif Devanagari`, `Shobhika`, or `Sanskrit 2003`.
- If a terminal has a separate non-ASCII font setting, set that to a Devanagari-capable font.

Rendering test:

```text
अच्सन्धिः अच्-सन्धिः गुणसन्धिः वृद्धिसन्धिः यण्सन्धिः
कर्मणिप्रयोगः भावेप्रयोगः महेश्वरः स्वागतम्
क् + त = क्त, त् + य = त्य, द् + य = द्य
```

If these look broken, the fix is usually terminal/font configuration. If these look correct but an editor cursor moves oddly, the issue is usually terminal-editor handling of combining marks.

## Notes Workflow

- Prefer pasting Sanskrit text directly into chat when possible.
- Use screenshots only for rendering problems, PDF snippets, handwritten notes, or layout questions.
- Keep course materials and screenshots out of Git.
- Summaries in this repo should be original notes, not copied course text.

## Screenshot Workflow

When uploading a screenshot:

1. Crop to the smallest useful region.
2. Include one sentence saying what to inspect.
3. Paste the underlying text too, if available.
4. If saving locally, use `screenshots/`; this folder is ignored by Git.

Good prompt format:

```text
Here is a screenshot from tmux. Please check whether the Devanagari rendering of "गुर्वाज्ञा" looks right.
Raw text: गुरु + आज्ञा -> गुर्वाज्ञा
```
