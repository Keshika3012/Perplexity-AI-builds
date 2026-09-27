# Teardown: Google Maps

**Date:** 26 Sep 2026

## 1. The product in one line

Gets drivers where they're going without having to look at the screen.

## 2. Target user for this teardown

Long-time users who rely on voice guidance so they can keep their eyes on the road.

## 3. What I tested

- **Multi-stop trip:** the overview map doesn't label stops clearly (1, 2, 3), so it's hard to track progress through the trip
- **Arrive-by time picker:** offers past dates, which is minor
- **Transit route:** checked walking paths; it showed a walking path where there isn't one
- **Voice settings:** looked for a way to change the navigation voice and found none
- **Reviews:** scanned recent 1–2 star reviews on the App Store and Play Store

I chose the voice problem because it had the most user evidence and the highest stakes: driver safety and long-time users leaving.

## 4. Evidence

About 10 reviews across both app stores complained about the new voice, all posted on 24–25 Sep 2026. That timing suggests it reached most users at once.

- **Safety:** One Play Store reviewer said the new voice is slow and leaves out specifics like exits, ramps and lanes, so they now watch the map instead of the road and called the update a hazard.
- **Churn:** One App Store reviewer said they're switching apps after 14 years of Google Maps. Another said they deleted it for the first time in 17 years. Others named Apple Maps and MapQuest as alternatives.
- **Control:** Several reviewers asked for an option to choose the voice, since there is currently no way to change it.
- **Preference:** Three reviewers described it as an "AI voice" without prompting, and called it harsh or unfriendly.

**Context:** Google announced in March 2026 that its navigation voice would become more natural and give more context about turns, as part of a Gemini-powered navigation upgrade rolled out in stages.

**Limitation:** This is a small sample from app store reviews, which skew negative. It shows a clear pattern, not proof of scale.

## 5. The biggest problem

Google Maps' new AI navigation voice gives drivers less specific guidance, pushing them to watch the screen instead of the road. Because they can't switch back, some long-time users are leaving the app.

## 6. Why it happens (root cause)

**Hypothesis:** Google tested whether the new voice *sounds* more natural, not whether drivers still get enough usable information to navigate without looking at the screen. It then rolled the voice out to everyone with no opt-out, so drivers who struggled with it had no fallback.

## 7. Proposed solution

**Restore the specifics in the new voice, with the classic voice as a temporary fallback.**

How it works for the user:
1. The new voice calls out exits, ramps and lanes again, at a normal speaking pace.
2. On the first drive after the update, a one-time notice says: *"Maps has a new voice. Prefer the old one? You can switch anytime in settings."*
3. Settings → Navigation → Voice offers two choices: **New voice** or **Classic voice**.
4. Google retires the classic voice only once the new voice performs as well on reroute rate and mute rate.

**What I'm not building, and why:**
- **A full voice picker:** expensive across dozens of languages, and it doesn't fix the missing information.
- **Retraining the voice to sound more natural:** that's what Google already optimized for; the gap is information, not tone.
- **A feedback prompt after every drive:** it would annoy drivers. One prompt after the first few drives on the new voice is enough.

## 8. Success metrics

- **Primary:** 30-day navigation retention among drivers who received the new voice
- **Early warning:** voice mute rate (drivers muting the voice mid-drive)
- **Guardrails:**
  - **Reroute rate:** missed turns must not go up
  - **Share of drivers staying on the new voice:** if everyone switches to classic, the fix has stalled Google's AI voice plans

## 9. Risks and trade-offs

- **Cost:** maintaining two voices across every supported language
- **Strategy:** the classic fallback could slow adoption of the AI voice Google is investing in
- **Over-correction:** adding more detail could make the voice talk too much. The mute rate will show this.
- **Evidence gap:** this is based on a small review sample; I'd validate it with usage data before building
