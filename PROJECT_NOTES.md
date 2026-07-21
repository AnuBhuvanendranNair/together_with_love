# Together, with love - Project Notes

## Progress So Far

- Built a single-page romantic America itinerary site.
- Updated page title and hero heading to `Together, with love`.
- Added local fonts:
  - `Photograph Signature` for hero title.
  - `Honeymoon` for date/subheader/tag-style text.
- Added countdown to August 8, 2026.
- Added meetup widget after countdown:
  - boy moves toward girl as countdown progresses.
  - progress can be tested with `?progress=0`, `?progress=0.5`, `?progress=1`.
  - final meetup swaps separate characters to couple image.
- Added sprite-based character states:
  - `idle`
  - `blink`
  - `yawn`
  - `sleep`
  - `working`
  - `evening`
  - `love`
  - `hugReady`
- Added time-based sleep:
  - boy sleeps based on Berlin time, wakes at 07:30.
  - girl sleeps based on SLC time, wakes at 06:00.
- Added character interactions:
  - single tap/click triggers normal actions: `working`, `evening`, `yawn`.
  - normal actions do not repeat consecutively.
  - normal actions can be cancelled by tapping same character again.
  - double tap triggers paired love/hug response.
- Added testing URL overrides:
  - `?boySleep=1`
  - `?girlSleep=1`
  - `?boyState=evening`
  - `?girlState=working`
  - `?love=1`
- Removed mobile tap highlight on characters.

## Current Interaction Rules

- Automatic states:
  - sleep
  - idle
  - blink
- Click/touch:
  - normal action: `working`, `evening`, or `yawn`
  - `working` / `evening`: 5-7 seconds
  - `yawn`: 650ms
- Double tap:
  - paired love/hug special action
  - lasts 5-7 seconds
- Disabled/unused for now:
  - `boy-more-sprite.png`
  - random love behavior

## Next Plan

### Countdown Milestones

Add small milestone moments based on countdown progress or remaining days.

Ideas:
- 10 days left: show `10 days until us`.
- 7 days left: show travel/packing mood.
- 3 days left: show airport excitement.
- 1 day left: show special almost-there message.
- 0 days left: heart confetti and couple reveal.

Possible implementation:
- Add milestone data in JavaScript.
- Compute remaining days from countdown target.
- Show milestone banner only when matching range is active.
- Keep it subtle, not too busy.
- Use same visual style as countdown widget.

## More Ideas

- Memory jar that fills with hearts as countdown progresses.
- Berlin/SLC time pills with sun/moon icons.
- Secret tap on hero title for hidden note.
- Mini route map with city stops lighting up.
- Destination cards with hidden personal notes.
- Optional sound toggle for tiny heart chime.

## Notes

- Keep interactions cute but not noisy.
- Avoid adding too many automatic animations at once.
- Prefer click/touch-triggered surprises over constant motion.
- Keep all sprite sheets at exact `2080 x 1440`, with `520 x 720` frames.
