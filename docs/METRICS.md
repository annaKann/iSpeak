[HEART Framework](https://docs.google.com/presentation/d/1nb7YB5qWDqtQdc7LXKEaZ4tsiRrVaHIRAEXRipWcFGs/edit?usp=sharing)

- **Metric 1: Low Churn Rate** 
  - Track Inactivity: In Firebase User Collection, add a last_active (timestamp) field. Update this field using an action on app's home page
  - Log Custom Churn Events: Identify actions that indicate churn (e.g., clicking "Delete Account" or canceling a subscription). Use the "Log Event" action in FlutterFlow to send a user_churned event to Firebase Analytics.

- **Metric 2: Number of Registered Users**
  - Track User Login time: In Firebase user collection, we are able to see the time that a user logs into the app itself.
  - Track new Users weekly: For a set amount of weeks, identify how many new users on average register for the app based off of features we've tested on (rating the app, etc)
