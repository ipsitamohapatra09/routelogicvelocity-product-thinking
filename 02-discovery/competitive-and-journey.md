# Persona & Future-State Journey, Module 2

- **Scenario:** RouteLogic Velocity (B2B)

## Persona
- **Role:** RouteLogic Velocity’s frontline coordinators. In the research these are mainly delivery drivers running multi-stop routes, working with dispatchers (composite persona “Dana”, built from UXR-01, 03, 06, 07, 11 and 12).
- **Goal:** Finish every stop on the route without calling anyone or reaching for a backup, so the shift ends on time.
- **Friction:** The app is slowest and least reliable at the exact moments she depends on it: at the doorstep (3 taps across 3 screens to mark delivered), when the route changes (8–15 minutes to arrive, no alert), and when signal drops (blank route offline).

## Current workaround (the status quo to beat)
- **External tools:** Paper manifests, phone screenshots of the route, text messages to the dispatcher, a WhatsApp group, phone calls to the office.
- **The process:** Before the shift, write or print a manifest and screenshot the route. During the shift, text completions instead of using the 3-screen flow, watch WhatsApp for route changes, retake proof-of-delivery photos when unsure an upload worked, and override route optimization by hand. After a crash, call the office and have someone read the remaining stops aloud.
- **Core frustration:** “I can’t trust the app, so I run a second system alongside it.”
- **The evidence:**
  - 5 of 7 drivers in the focus group keep a paper manifest “just in case the app dies” (UXR-12).
  - A dispatcher’s team uses a WhatsApp group as “the real system” (UXR-02); route reassignments take 8–15 minutes to reach drivers (BUG-2044, Critical).
  - A driver texts the dispatcher instead of marking stops delivered (UXR-01); the 3-tap flow is the top frontline complaint (BUG-2055, High).
  - A driver lost 20 minutes calling the office after a mid-route crash (UXR-03); separately, the app crashes on Android 12/13 above ~40 stops (BUG-2031, Critical).
  - A rural driver screenshots her route every morning because offline mode shows a blank route (UXR-06, BUG-2050).
  - Proof-of-delivery uploads fail silently ~35% of the time on weak signal (BUG-2061); a warehouse lead reports drivers retaking photos three times (UXR-07).
  - Business impact: an enterprise account is evaluating a leaner competitor (UXR-04), and a regional manager says the driver experience has put renewal at risk (UXR-10).

## Future-state journey map
1. **Start the shift:** Dana taps Start route from the home screen and the full route downloads and stays on her phone → her route is available all day, with or without signal, so the paper manifest and morning screenshots are no longer needed.
2. **On the road:** A route change arrives as a push alert and updates her stops instantly, while her status updates the dispatcher’s board live → nobody drives the wrong way and both screens show the same truth, replacing the WhatsApp group and check-in texts.
3. **At the doorstep:** One tap marks the stop delivered, and the photo saves on the phone, uploads in the background and confirms when done → each stop is finished in seconds with one hand, with no texting completions and no retaken photos.
4. **When something breaks:** If the app restarts, the route resumes where she left off, and Report failed delivery is one tap from the stop → a failure costs seconds instead of a 20-minute call to the office.

_Not yet eliminated: daily manual routing overrides. Saved local overrides (BUG-2068) are deferred to next quarter._

## Competitive advantages
1. **One trusted system of record.** Every delivery, route change and photo is captured in the product instead of WhatsApp, texts or paper. That makes the admin reporting buyers paid for accurate again, which neither the workarounds nor a leaner routing-only tool can provide.
2. **Built for the field, not the office.** Offline-first, crash-resilient and usable with one hand at the doorstep. The status quo fails at exactly the moments drivers rely on it.
3. **A real-time dispatch loop.** Drivers and dispatchers see changes within seconds, compared with 8–15 minutes for route changes and 20–60 minutes for dashboard status today. Coordination stays inside the product.

_Caveat: the advantage over the leaner competitor is a claim to validate. Its offline and real-time sync capabilities are not yet known._
