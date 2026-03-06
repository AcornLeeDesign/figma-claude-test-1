# CLAUDE.md

> Read this before every session.
> Only add to "Never Change" when you've made a hard call worth protecting.

---

## Project

**Product:** CRM for Feminists Center for Creative Work  
**Platform:** Desktop  
**Typeface:** Inter - Google Fonts  
**Brand colors:**   
- #7C3AED  
- Gray: #6B7280
- Error: #DC2626

**Repo:** [https://github.com/AcornLeeDesign/figma-claude-test-1](https://github.com/AcornLeeDesign/figma-claude-test-1)
**Token file:** `/tokens/tokens.json`
**Figma file:** [name or URL]

---

## What Lives in tokens.json

Colors and radius only. Spacing and typography are rules below —
not tracked as variables, not in the token file.

---

## Color Token Rules

- Three layers always: primitive → semantic → component. Never skip.
- Primitives: `[name]-[shade]` e.g. `violet-600`
- Semantic: `color-[role]` e.g. `color-bg-default`, `color-interactive-primary`
- Component: `color-[component]-[role]` e.g. `color-button-bg-hover`
- Global semantic token only if pattern appears in 3+ components
- Never reference a primitive directly from a component token
- kebab-case, lowercase, no abbreviations

---

## Spacing Rules

> Apply these when generating UI. Do not create spacing tokens or variables.

4px base unit. Non-linear — tighter at small sizes, bigger jumps at large.
Always use a value from this scale. No arbitrary values.


| Value | Use                                  |
| ----- | ------------------------------------ |
| 4px   | icon padding, indicator dots         |
| 8px   | tight inline, badge padding          |
| 12px  | compact stacks, dense lists          |
| 16px  | default component padding            |
| 20px  | relaxed component padding            |
| 24px  | card padding, section breathing room |
| 32px  | between grouped components           |
| 40px  | between sections                     |
| 48px  | generous section separation          |
| 64px  | page-level padding, major breaks     |
| 80px  | large breakpoint breathing room      |
| 96px  | maximum layout spacing               |


---

## Typography Rules

> Apply these when generating UI. Do not create typography tokens or variables.

- Scale: 12 / 14 / 16 / 18 / 20 / 24 / 30 / 36 / 48px (major third 1.25, base 16px, even sizes only — no 13px or other odd values)
- Line height: 1.2 headings · 1.5 body · 1.0 labels
- Letter spacing: 0 body · +0.05em labels/caps
- Max 3 font sizes in any single component
- Only use weights that exist in the loaded typeface
- Weight usage: regular (400) body · medium (500) UI labels · semibold (600) headings · bold (700) display only

---

## Accessibility (always enforce)

- Body text: 4.5:1 contrast minimum
- Large text 18px+: 3:1 minimum
- UI components + focus indicators: 3:1 minimum
- Never color alone for meaning — pair with icon or label
- Focus states always visible — never just `outline: none`
- Error states require a label or icon, not just a color change
- **Desktop:** 24×24px min hit area · 8px min gap between targets
- **Mobile:** 44×44px min touch target · 8px min gap between targets
- **Responsive:** desktop rules at desktop breakpoints, mobile rules at mobile

---

## States

Flag any missing before marking a component done:
`default` · `hover` · `active` · `focused` · `disabled` · `error` · `loading`

---

## Never Change

> Hard calls only. Start sessions by reading this.

- [add locked decisions here]

---

## Commit Format

`feat:` new color token or component ·
`fix:` value correction ·
`refactor:` rename without value change