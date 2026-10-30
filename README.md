# Pioneer Institute Website

Responsive single-page Pioneer Institute prototype with a scroll-driven cinematic hero, narrative beats, interactive course rail, institute information, and admission enquiry form.

## Run locally
From this folder run:

```bash
python -m http.server 8000
```

Open http://localhost:8000.

## Contact details supplied
- CEO: V. Prabhakaran
- Cell: +91 9585347191
- Address: LCCT CO WORKING SPACE, NEXT BUILDING TO PROVIDANCE MALL, CUDDALORE MAIN ROAD, PONDICHERRY.

The footer phone link and floating WhatsApp action use the supplied mobile number.

## Timeline map and checkpoint review
The cinematic section is 440vh on desktop. Progress is calculated from the section's own scroll travel and clamped to 0–1. The animation is reversible because every visual property is derived directly from normalized progress.

| Progress | Expected stage state | Implementation check |
|---:|---|---|
| 0.00 | Complete hero | Hero copy visible; opening scene at initial scale |
| 0.18 | Opening copy has exited | Hero fade/translation is almost complete |
| 0.27 | First narrative panel | Beat A is fully readable |
| 0.44 | Clean panorama | Beat A has exited; scene remains composed |
| 0.58 | Second narrative panel | Beat B is fully readable |
| 0.74 | World returns to focus | Beat B has exited |
| 0.90 | Catalog enters | Course rail is fully visible and interactive |
| 1.00 | Final interactive state | Course rail remains visible; previous/next and swipe work |

### Verification note
The progress mapping and state transitions were reviewed against the requested checkpoints in the source. A live browser screenshot/visual regression pass has not been performed in this environment; verify the listed checkpoints in desktop and mobile browsers before production release.

## Production work still required
- Replace the prototype student image with a final high-resolution, properly licensed 3D student render.
- Replace sample course copy with the institute's confirmed course offerings.
- Add verified institute results, testimonials, and photographs if available.
- Connect the admission form to a secure backend, CRM, or email service. It currently validates in the browser but does not transmit or store submissions.
- Confirm spelling and formatting of the supplied address before publishing.
- Add the official institute logo and social links if available.

## Asset manifest
- `assets/student-hero.jpg` — prototype student visual crop; 350×331 px; right-side hero background. Replace with a production transparent 3D render for best results.
