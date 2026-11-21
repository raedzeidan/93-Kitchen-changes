# 93 Kitchen — Hi-Fi visual parity correction bundle

Source design: https://www.figma.com/design/1lyrLGHubD9KHHevKfPW4g/93Kitchen-new?node-id=89-309

Main project: https://github.com/raedzeidan/93Kitchen-new

Applied main branch commit: 863a2215b1feb09c4825ecd286bb68cba3801749

## Why the implementation differed

- Styling used generic section spacing and card geometry rather than the 1440 × 4013 Figma desktop frame.
- Only two dish photos were used in the code; some dishes displayed icons/placeholders while the actual design had distinct food imagery.
- Typeface family was Cairo in both, but the weight, scale and wrapping were not consistent with Figma.
- The hero, plan cards, delivery block, split About panel, review portraits, FAQ rows and footer layout did not honor original section dimensions.

## Files to apply

Copy `src/site/app.ts` and `src/site/styles.css` to the same paths in the main repository.
Copy every file in `assets/` into `public/assets/` in the main repository.

Do not overwrite the existing Figma Make build configuration, `package.json`, lockfiles, `index.html`, or other unmodified assets.

## Visual mapping

Homepage: navigation 86px, hero 597px, menu 625px, subscriptions 530px, delivery 271px, About 652px, reviews 492px, FAQs 515px, footer 245px at 1440px desktop width.

Menu: Figma 3 columns, photo 382 × 190, full card 382 × 408. The original `menu-atlas.jpg` contains a 3×3 layout of photographed dishes and is cropped with the `atlas-x*` / `atlas-y*` classes; don't replace it with stock photos. Home-specific real food photographs and review portraits are supplied separately.

## QA and publishing

The code and eight image files were committed to `93Kitchen-new`, and paths were verified on GitHub. Live browser screenshot verification of https://93kitchen2.figma.site was unavailable. GitHub updates may require **sync/reimport and Publish** inside the correct Figma Make project before the public site changes.
