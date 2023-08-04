# GetThru / Skynet Take-Home Exercise
![image](https://user-images.githubusercontent.com/83227995/139120549-61b184e3-5568-45b2-a085-652f52195d8c.png)

Hello and thanks for taking the time to do GetThru's Elixir take-home coding exercise! We've prepared a fun exercise that will help us gauge your skill level with Elixir.

## Directions

1. Clone this repo to your machine.
2. Create a new _private_ repository under your account on GitHub (or similar service) and push the cloned project there. Don't just fork it because then other people can see your solution. You'll probably have to remove the existing git remotes in `.git/config` before doing this.
3. Create a branch other than main that will contain your work.
4. Do the work described in "The Exercise" section.
5. Make a pull request of your working branch to main. Write a description of your design choices, thoughts, setbacks, etc. in the PR description (template provided).
6. Add `@crertel-getthru` to your PR. Once notified, he'll review your PR and if it looks good setup the interview.

### Regarding Time

This is supposed to test your skills, not take up all of your free time. If you find yourself spending more than 3-4 hours on it and try to get it done and sent back within 3 days, use your best judgement to find a stopping point and write a short description of what the challenges were.

Prioritize the server part of the exercise if you're short on time. Contact your recruiter or tech@getthru.io if you have any questions.

### Regarding LLM assistance

There are a wave of new tools like ChatGPT and copilot that can be very helpful, but they can also hallucinate and mislead.

For the purposes of this exercise **do not use any code generated or derived from an LLM or chatbot**. If you need to use one to help explore a subject as you would Wikipedia or whatever, that's fine--but in order to get the best assessment of your skills and capabilities, we need you to solve this assignment on your own.

## The Exercise

### The Server

The exercise is to model Skynet and Terminators using Elixir. A user can spawn Terminators and then those Terminators go on living their metallic, human-killing lives. Each Terminator has a chance to reproduce and be killed by Sarah Connor at specific intervals.

- Take advantage of Elixir's OTP features.
- When the app starts there should be no Terminators.
- There should be a function that when called spawns a Terminator.
  - While this terminator is alive, it has a chance to reproduce and be killed by Sarah Connor.
  - Every 5 seconds, each terminator has a 20% chance of reproducing, creating 1 new terminator.
    - Terminators can reproduce more than once. They're trying to take over the world, after all.
  - Every 10 seconds, each terminator has a 25% chance to be killed by Sarah Connor.
- Each terminator should have a unique ID.
- There should be a function to manually kill a Terminator given its ID.
- There should be a function to get a list of all living Terminators.
- You don't need to keep track of ancestry / hierarchy.
- Expect this part to be run and manually tested in `iex`.

### The API

Create API endpoints for the following actions. You can pick what API protocol to use, if any.

- Spawn a terminator
- Manually kill a terminator
- List all living terminators

### Bonus points

We know that time is limited, but if you wanted to take a crack at any of the following it'd be great!

* Automated testing (show us how to exercise the API during tests)
* Elevator pitch for deploying this to production
* Clustering (can you get this to generate Terminators on multiple nodes?)
* Metrics/monitoring via Telemetry
