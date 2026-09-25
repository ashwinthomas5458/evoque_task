# evoque_task

A React front-end exercise: a course-marketplace landing page (page title "Interview Task") that renders course data fetched from a remote API.

## Overview

`src/App.js` composes `Nav`, `Cover`, `Body` and `Footer`. Section components in `src/components` cover course categories, featured courses, popular courses, offers (`OfferIncluded`), a mobile-app promo (`MobileApp`) and course cards (`Card`, `Cat`).

Data is loaded by two hooks in `src/hooks`:

- `GetCourses` – POSTs to a `/api/v1/user/course/home` endpoint and reads `featured_courses`, `popular_courses` and `course_with_offers` from the response.
- `GetCategories` – GETs `/api/v1/user/course-category/get-all`.

Both endpoints are hard-coded to an AWS API Gateway (`ap-south-1`, `dev` stage) URL in the hook files. The page depends on that external service being reachable.

## Stack

React 16 (`^16.13.1`) on Create React App (`react-scripts` 3.4.3), with Testing Library packages installed.

## Scripts

```
npm start       # development server on http://localhost:3000
npm run build   # production build
npm test        # test runner
npm run eject
```

## Layout

```
public/       HTML shell and manifest
src/          App, components, hooks, styles
docs/         Committed production build output (static bundle)
```
