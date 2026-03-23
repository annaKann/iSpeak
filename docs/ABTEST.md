# A/B Tests

---

## Test 1: SignUp/Login Screen on One Tab or Two Different Tabs
**Contributor:** Mustaan
**User Story:** US1

**Metrics:**
Number of users who sign up/login from one screen or from two different screens.

**Hypothesis:**
You are a user about to sign-up/log into the app, but would find it more feasible to have signing up and logging in on two different screens or having one screen for both signing up and logging in. The issue that this A/B test would be solving is whether or not the user would find it more feasible to sign-up/login from one screen or switch from one screen that details signing up to another screen that details logging in. I hypothesize that users would prefer to just have signing up and logging in on one screen rather than two different screens.

**Experiment:**
We would set up a true/false "check box" that will show the two different signing up/logging in methods that were previously discussed in the hypothesis, and then track the number of users that sign up or log in from each method in Firebase via the amount of new users that register for the app.

**Variations:**
Aside from the things discussed above, there would be no other variations needed to be tested for this A/B test.

---

## Test 2: Profile Onboarding on Guided Setup or Quick Start Option
**Contributor:** Korinne
**User Story:** US3

**Metrics:**
Profile completion rate, users who complete profile within first session, 7-day return rate.

**Hypothesis:**
You are a new user who just signed up for the app but would find it more feasible to either complete a guided profile setup before using the app or skip the setup and start working out immediately. The A/B test would be solving whether or not the user would prefer to complete their profile first or jump straight into the app with the "Quick Start" option.

**Experiment:**
We would set up Firebase A/B testing to randomly split new users into two groups that will show the two different onboarding methods that were previously discussed in the hypothesis, and then track the number of users that complete their profile or skip it in Firebase via the profile completion rate and 7-day return rate.

---

## Test 3: Workout Reminder Notifications
**Contributor:** Anna
**User Story:** Calendar-Based Workout Opportunity Notifications

**Metrics:**
Amount of sessions per new user, amount of sessions per returning user on average.

**Hypothesis:**
If a user who feels that they lack time to exercise are given reminders to workout in a known free block of time, they will be more likely to log workout sessions using the app.

**Experiment:**
Randomly select two subsets of users — one will set up calendar tracking and will receive notifications reminding them to workout. The other subset will not receive these notifications and will not set up calendar tracking.

---

## Test 4: Workout Streak Visibility: Visible vs Hidden
**User Story:** US6 – Build workout log and streak

**Metrics:**
- Engagement: Workouts started per user
- Retention: Return rate within 7 days

**Hypothesis:**
If users can clearly see their workout streak on their profile and home screen, then they will be more likely to continue using the app and start more workouts because streaks create a sense of progress and accountability.

**What problem are we trying to solve? Its impact?**
Currently, the workout streak is only minimally visible and easy to overlook. Users may not feel a strong sense of progress or motivation to return to the app. This is a problem because the app relies heavily on habit-building and consistency. If users don't feel motivated to maintain a streak, they are more likely to stop using the app after a short period. The bottleneck occurs after initial app usage — users are not returning consistently. We believe this is due to a lack of visible progress indicators that reinforce continued use.

**Experiment:**
We will use Firebase Remote Config to split users into two groups:
- Group A (Control): Workout streak is minimally displayed (log only)
- Group B (Variant): Workout streak is prominently displayed on both the home screen and profile

50% of users will be assigned to each group.

Firebase Analytics events: `workout_started`, `app_open`, `workout_completed`, `session_duration`

We will include all users to maximize data collection and run the test until at least 100 users per group are reached.

**Variations:**

Version A (Control):
- Streak is only visible on the profile page
- No visual emphasis

Version B (Variant):
- Streak is displayed prominently on the home screen
- Includes visual emphasis (e.g., bold text, flame icon)
