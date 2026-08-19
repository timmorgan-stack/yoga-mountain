# Yoga Mountain — design concept

An independent redesign proposal for [yogamountain.ie](https://yogamountain.ie), the yoga practice of
Hannah Dunford in Enniskerry, Shankill and Bray, Co. Wicklow.

**Live preview:** https://timmorgan-stack.github.io/yoga-mountain/

This is a concept, not the live site — it is served `noindex, nofollow` so it can't surface in search.
All copy, class details, logo and photography belong to Yoga Mountain; photography by
[The Visible Business](https://www.thevisiblebusiness.ie). Everything here is their own content, rearranged.

## What it is

A single static page (`index.html` + `assets/`), no build step, no dependencies, no external requests.
Open `index.html` directly or serve the folder.

- Hero, offer cards, weekly timetable, retreat itinerary + pricing, about, testimonials, gift vouchers, enquiry form
- Logo is the live site's own mark, keyed off its white JPEG background to transparent PNG, with a
  lightened variant (`assets/logo-dark.png`) swapped in by CSS for dark theme
- Light and dark themes via CSS custom properties, plus a manual toggle
- Mobile-first, system font stacks, `prefers-reduced-motion` respected
- Scroll reveals use IntersectionObserver with a scroll + timeout fallback (embedded browser panes don't always fire IO)
- The enquiry form is UI only — nothing is sent
