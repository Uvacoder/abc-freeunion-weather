# Weather <!-- omit in toc -->

A weather app using Next.js, Mantine, Edge API Routes, and the OpenWeatherMap and Google Maps API's.

⛈ View your local weather forecast: <https://localwx.vercel.app/>

---

## Table of Contents <!-- omit in toc -->

- [Development Setup](#development-setup)
  - [Generate API Keys](#generate-api-keys)
    - [OpenWeatherMap API](#openweathermap-api)
    - [Google Maps API](#google-maps-api)
  - [Install](#install)
    - [Setup Next.js](#setup-nextjs)
    - [Set ENV Variables](#set-env-variables)
  - [Working with Next.js](#working-with-nextjs)
    - [Folder Structure](#folder-structure)
    - [NPM Scripts](#npm-scripts)
- [Credits](#credits)
- [Contributing](#contributing)

---

## Development Setup

### Generate API Keys

#### OpenWeatherMap API

First, you'll need an [OpenWeatherMap API Key](https://home.openweathermap.org/users/sign_up). If you don't have an account, you can create one for free.

#### Google Maps API

Next, you'll need to generate a [Google Maps API Key](https://developers.google.com/maps/documentation/geocoding/get-api-key).

After you've generated a key, visit the [Credentials page](https://console.cloud.google.com/projectselector2/google/maps-apis/credentials) and follow the instructions below:

1. Set application restrictions to "None"
2. Select "Restrict key"
3. Choose "Geocoding" and "Places" from the dropdown
4. Save

![screenshot of google api settings](https://dl.dropbox.com/s/2vj1qa2l1602prc/Screen%20Shot%202022-02-12%20at%2008.38.25.png?dl=0)

---

### Install

#### Setup Next.js

Use [create-next-app](https://www.npmjs.com/package/create-next-app) to get up and running quickly:

```bash
npx create-next-app local-weather --example https://github.com/gregrickaby/local-weather
```

#### Set ENV Variables

Rename `.env.sample` to `.env` in the root of the project. Add the API keys you generated earlier to the following ENV Vars:

```text
// .env
GOOGLE_MAPS_API_KEY="YOUR-KEY"
OPENWEATHER_API_KEY="YOUR-KEY"
```

---

### Working with Next.js

#### Folder Structure

```text
├── components
|  ├── Alerts.tsx
|  ├── Footer.tsx
|  ├── Forecast.tsx
|  ├── etc...
├── lib
|  ├── helpers.ts
|  ├── hooks.ts
|  ├── types.d.ts
|  ├── etc...
├── pages
|  ├── api
|  |  ├── places.ts
|  |  └── weather.ts
|  ├── _app.tsx
|  ├── _document.tsx
|  └── index.tsx
├── public
|  ├── icons/
|  ├── favicon.ico
├── .env.sample
├── .gitignore
├── package.json
├── next.config.js
├── etc...
```

**Components** - This folder contains React components.

**Lib** - This folder contains internal hooks and function files.

**Pages** - This folder contains standard Next.js pages and `/api` middleware routes.

**Public** - This folder contains all of the static assets.

---

#### NPM Scripts

Start local dev server:

```bash
npm run dev
```

Lint code:

```bash
npm run lint
```

Test a build prior to deployment:

```bash
npm run build && npm start
```

---

## Credits

- React components by [Mantine](https://mantine.dev/)
- Weather icons by [@basmilius](https://github.com/basmilius/weather-icons)
- Weather data from [OpenWeatherMap API](https://openweathermap.org/api)
- Geocoding data from [Google Maps](https://developers.google.com/maps/documentation/geocoding/overview)

---

## Contributing

Please see [CONTRIBUTING](./CONTRIBUTING.md) for more information.

---
