# cosmo-quiz

Interactive astrology + MBTI quiz with personalized results. Standalone quiz module that integrates with the cosmo-funnel conversion flow.

## What It Does

- Collects user birthday and MBTI type via multi-step quiz UI
- Generates a personalized cosmic personality profile
- Displays 3 free result reveals to hook the user
- Gates the full reading behind the $9 OTO paywall in cosmo-funnel

## Integration with cosmo-funnel

This quiz feeds into [uerzer/cosmo-funnel](https://github.com/uerzer/cosmo-funnel):

```
cosmo-funnel/index.html  -->  cosmo-quiz  -->  cosmo-funnel/results.html ($9 OTO)
```

The quiz collects lead data (birthday, MBTI) and passes it to the results page where the paywall lives.

## Tech Stack

- Pure HTML5, CSS3, vanilla JavaScript
- No frameworks, no build step
- Works standalone or embedded in funnel

## Deploy

```bash
# Clone and serve locally
git clone https://github.com/uerzer/cosmo-quiz
cd cosmo-quiz
python3 -m http.server 8000
open http://localhost:8000

# Deploy to GitHub Pages
# Go to repo Settings > Pages > select main branch > Save
# Live at: https://uerzer.github.io/cosmo-quiz

# Or deploy to Netlify by dragging the folder to netlify.com
```

## File Structure

```
cosmo-quiz/
├── index.html    # Quiz entry point
├── style.css     # Quiz styling
└── script.js     # Quiz logic and result generation
```

## Status

- [x] Quiz UI built
- [x] Personalized result generation
- [ ] GitHub Pages enabled
- [ ] Wired to cosmo-funnel payment flow
