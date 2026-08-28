# Yumble — Design Document

**Yumble** — watch it all tumble together. A playful, visual food-ordering experience where users build a meal ingredient-by-ingredient and watch their choices become the final dish.

_Working concept name: "Build Your Bowl."_

Status: `Discover + Define` complete → moving into wireframes.

---

## 1. Problem Statement

Highly customizable food ordering feels like filling out a form: select an option, scroll, choose another, repeat. Users can't picture the final dish until it arrives, and long ingredient lists create decision fatigue.

**Primary design question:**
How might we make customizable food ordering feel more tangible and understandable, while preserving the speed and clarity of a normal ordering flow?

**Key tension:** Delight ↔ Efficiency. The build experience should reward users who want to explore, without punishing users who just want to reorder a familiar meal.

## 2. Target Users

| User | Need | Primary friction |
|---|---|---|
| **Visual / first-time orderer** *(primary)* | Wants to see the dish, not just read ingredient names | Text-only selections are abstract |
| Explorer / influencer | Wants an appealing, photo-worthy result | Too many choices, no preview to judge the outcome |
| Quick reorderer | Wants speed | Animation and multi-step flows slow repeat orders |

MVP is designed primarily for the **visual/first-time orderer** — the other two are served by the same live-preview mechanic rather than separate flows.

## 3. Scope

**In scope (MVP)**
- One meal format (bowl)
- ~15 ingredients across rice, beans, protein, salsa, toppings
- A single guided build flow with a live visual preview of the dish
- One AI-assisted "what are you feeling" recommendation flow
- Responsive layout, keyboard access, reduced-motion support
- A Figma prototype covering the full flow

**Out of scope (MVP)**
- Multiple meal formats (wrap, salad)
- Image-to-meal AI, preference learning across sessions
- Accounts, payments, delivery tracking
- Quick Order mode (candidate for v2)

## 4. Core Flow

```
Home → Start Order → Choose Meal → Build → Review → Checkout
```

Build sub-flow: `Rice → Beans → Protein → Salsa → Toppings → Review`

Every selection has a visible consequence — the chosen ingredient appears in the live dish preview; removing one reverses that state. Reduced motion preserves the same information without relying on animation.

## 5. Definition of Done (MVP)

- A user can complete a bowl start to finish and edit any prior step
- The dish visibly builds as choices are made, on desktop and mobile
- Price updates correctly as ingredients are added or removed
- The AI flow returns a valid, editable suggestion from real menu data
- Core controls are keyboard-accessible; reduced motion preserves parity
- A Figma prototype demonstrates the full flow end to end

## 6. Tech Stack

| Layer | Tool |
|---|---|
| Design | Figma |
| Frontend | Next.js + React + TypeScript |
| Styling | Tailwind CSS |
| Motion | Framer Motion |
| AI | Structured mock for MVP |
| Data | Static JSON |
| Deployment | Vercel |

## 7. License

See [LICENSE](./LICENSE).
