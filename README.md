
## What this is
This is a React front-end clone of a Starbucks-style storefront and landing experience, focused on browsing drinks, food, rewards, and store flows. It is built as a single-page app with route-based pages and a fixed header/footer shell rather than a backend-powered commerce app.

### Stack
- **Language(s):** JavaScript, HTML, CSS
- **Framework / runtime:** React 18 with Create React App / `react-scripts`
- **Notable libraries:** `react-router-dom`, `swiper`, `react-icons`, `tailwindcss`

## How it's organized
```text
public/             static HTML shell and favicon/manifest assets
src/
  App.js            app router and page composition
  index.js          bootstraps React app
  index.css         global styling
  data/
    index.js        product catalog and promo content
  components/
    Header.js       site navigation and top menu
    Footer.js       footer links and page footer
  pages/
    Home.js         Starbucks-style landing page
    Gift.js         gift cards page
    Order.js        ordering entry page
    Pay.js          payment page
    Profile.js       profile stub
    Rewards.js       rewards stub
    Search.js        search stub
    Store.js         store locator page
  assests/          images used throughout the UI
Dockerfile          containerizes the app for Node
Jenkinsfile         CI/CD pipeline for install/build/push Docker image
package.json        React app scripts and dependencies
tailwind.config.js Tailwind setup
```

**How it fits together:** `App.js` sets up routes like `/dashboard`, `/giftcards`, `/ordering`, and `/pay`, with `Header` and `Footer` wrapping the page content. The main experience is in `src/pages/Home.js`, while `src/data/index.js` provides structured product and promotion data that drives cards and banners. The app is front-end only: no API or database layer is evident in the repo.

## How to run it
From a fresh clone:

```bash
npm install
npm start
```

For a production bundle:

```bash
npm run build
```

For the Docker path defined in the repo:

```bash
docker build -t starbucks .
docker run -p 3000:3000 starbucks
```

## Try asking
- "Where are the product cards and banners defined in this app?"
- "Can you walk me through the main routing flow between Home, Store, and Pay?"
- "Is this repo meant to be a static mockup or do you want me to add real data/API integration next?"