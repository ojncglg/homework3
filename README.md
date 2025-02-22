[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Fc9pM79D)
# Assignment 1

## Objective

For Assignment 1 (A1) we are going to be building four different timer components that we will use in future assignments.

## What are we building?

In the fitness world, there are lots of different ways a workout can be timed. For example, we can use a traditional stopwatch, a count-down timer, an interval timer, etc. To support our athletes, we’ll be building 4 different types of timers:

| Timer type | Description                                                                                                                                                                                                                                                                               |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Stopwatch  | A timer that counts up to X amount of time (e.g. count up to 2 minutes and 30 seconds, starting at 0)                                                                                                                                                                                     |
| Countdown  | A timer that counts down from X amount of time (e.g. count down to 0, starting at 2 minutes and 30)                                                                                                                                                                                       |
| XY         | A timer that counts down from X time per round, for Y number of rounds (e.g. 1 minute for 10 minutes would count down from 1 minute to 0, then start another countdown, etc, 10 times )                                                                                                   |
| TABATA     | An interval timer with work/rest periods. Example: 20s/10s, 8 rounds, would count down from 20 seconds to 0, then count down from 10 seconds to 0, then from 20, then from 10, etc, for 8 rounds. A full round includes both the work and rest. In this case, 20+10=30 seconds per round. |

Our larger components are going to be `Stopwatch`, `Countdown`, `XY`, and `Tabata` (all of them are located in `src/components/timers`), but you can imagine that they have common functionality. An example is a start button. All timers are going to have to have a way to start. Our goal is to take these large components and extract common functionality into smaller components. We might have a `Button` component that is shared by all of our timers and it might have a prop that we pass in that changes the background color in order to create a start `Button` and a stop `Button`.

## Deliverable

1. Get all 4 types of timers to work. The timers should have a pause/resume button, a reset button, and a "fast forward" button (ends the timer). All timers should render at `localhost:3000`.
2. You should try to DRY up your code by creating generic components that are going to be used by your timers. The most basic ones, but not limited to, are going to be a `Button`, `Input`, `DisplayTime`, `DisplayRounds`, and `Panel` (that handles layout of your timer).
3. For now you are going to want to store all state in the timers themselves.
4. Style your components in a way that they are consistent and look presentable. Do not use an existing UI design library (e.g. MUI or Antd), instead try to come up with your own. **You are welcome to search the internet for design inspiration, but make sure to cite all resources you have used.**
5. Deploy your application to Github pages.

## Grading rubric

- All 4 timers are working correctly. Timers should have pause/resume button, a reset button, and a button that ends the timer (puts the timer in completed state).
- UI is consistent and effort has been put into making it look nice. Cite any resources you used.
- Keep your code as DRY (Don't repeat yourself) as possible
- The console should be free of JS erros, TS errors, and warnings

## Bonus (5pt)

- Document all of your generic components. A template for this documentation can be found at `/docs`.

## Install and Run Project

Install project

```
npm i
```

Run project

```
npm run dev
```

Timers: `localhost:5173`. Documentation: `localhost:5173/docs`

## Deploy to GH-Pages

**It is important that you follow these steps in the correct order:**

1. Open `package.json` and update the `"homepage"` key with your repo information. It should change from:


//CHANGED FROM assignment-1 to assignment-2//
`"homepage": "https://hes-e39.github.io/assignment-2/"`

to

`"homepage": "https://hes-e39.github.io/<your repo>/"`

If you created this repo in github classrooms, the repo name should have your username at the end of it. Make sure to copy the whole thing. Also make sure the trailing `/` follows after your repo name.

2. Push changes to GH
3. Wait until actions finish, this will create a new branch `gh-pages` and run the deployment
4. In your GH repo: Settings -> Pages -> Build and deployment -> Branch -> gh-pages

You might have to hard refresh the browser page when pushing multiple updates to GH in order to reflect the most recent changes.

This is to update the new SRC folder.