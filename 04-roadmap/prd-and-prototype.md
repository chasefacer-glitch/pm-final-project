# A2 — Why You'll Love This Label, Simplified PRD (StreamLine)

**Author:** Me · **Status:** Draft · **Target:** High-Fidelity Prototype · **Persona:** Frustrated Viewer (Priya, UXR-01): a longtime subscriber who scrolls for 20 minutes and then puts on a DVD

## 1. The Big Picture
- **Vision:** Help users spend less time browsing and more time watching movies they're excited about.
- **Press release:** StreamLine introduces “Why You'll Love This,” a new Spotlight feature that gives users a short, relevant explanation of why a movie is worth watching.

Instead of spending 20 minutes scrolling through endless recommendations, users can quickly understand what makes each movie appealing and feel more confident in their choice.
- **Success metric:** Browse-to-play conversion rate
- **Guardrail:** Movie completion rate must not decrease.

## 2. The Details
### User stories
- As a longtime subscriber, I want to understand why a movie is recommended so that I can make a faster decision.
- As a viewer, I want to see what makes a movie worth watching without having to open every movie detail page.
### Screens to build
- 1. Home: Spotlight collection featuring movie cards with “Why You'll Love This” labels.
- 2. Movie details: Movie poster, description, recommendation label, genre, runtime and Play button.
- 3. Now playing: Confirmation screen showing the selected movie and a Back to Home button.
### Functional requirements
- Display eight movie cards within the Spotlight collection.
- Show a recommendation label on every Spotlight movie card.
- Limit each label to 20 words or fewer.
- Allow users to select any movie card to view its details.
- Display the same recommendation label on the movie detail screen.
- Allow users to select Play and reach the Now Playing screen.
- Allow users to return to the homepage.
### Smart behaviors (Situation → Outcome)
- If a user selects a movie card → open its detail screen.
- If a user selects Play → display the Now Playing screen and log a play event.
- If a user returns to the homepage → preserve their previous browsing position.
- If a recommendation label is missing → hide the label rather than display empty text.
### Technical constraints
- Use React and useState only. Use eight sample movies with prewritten recommendation labels. No external APIs, database, backend, user accounts, live AI recommendations or actual video playback.
- Scope decision: We're simulating the recommendation labels and playback for this prototype, not building the actual recommendation engine. Movie completion rate cannot be measured until real playback is implemented.

## 3. The Logistics
### Features out
- New AI recommendation engine, labels across the full catalog, user ratings and reviews, multiple language support, and actual video playback.
### Edge cases & safety guard
- If a label is missing, hide it. If a movie poster fails to load, display a fallback image. Never display misleading recommendations, inaccurate movie information or empty labels.
### Decision log
- 1. Use prewritten recommendation labels instead of building a new AI recommendation engine to reduce engineering effort.
- 2. Limit the prototype to eight Spotlight movies instead of the entire catalog to protect the three-week sprint.
### Evals
- Accuracy: 100% of labels accurately describe their movies.
- Time-on-task: At least 80% of testers select a movie and reach the Now Playing screen within two minutes.
- Safety: Zero misleading recommendations or empty labels displayed during testing.

## MoSCoW scope
- **Must:** Short, relevant explanation of why a movie is worth watching.; Labels displayed on Spotlight movie cards.; Accurate recommendations based on existing movie data.
- **Should:** Labels personalized to the user's viewing preferences.; Tracking of browse-to-play conversion and movie completion rates.; Ability to update or correct inaccurate labels.
- **Could:** Mood-based recommendation labels.; Curator attribution (e.g., “Picked by…”).; Visual enhancements such as icons or animations.
- **Won't (now):** A new AI recommendation engine.; Labels across the entire StreamLine catalog.; User ratings and reviews.; Multiple language support.

---
**Builder hook:** Build a working prototype based on this PRD. Use the User Story as the core flow, Functional Requirements as build constraints, and prioritize speed and clarity over visual complexity.

**Prototype:** https://claude.ai/artifact/K2DH9wd585vbdApY2DQ5uE
