[HEART Framework](https://docs.google.com/presentation/d/1nb7YB5qWDqtQdc7LXKEaZ4tsiRrVaHIRAEXRipWcFGs/edit?usp=sharing)

- **Metric 1: Low Churn Rate** 
  - Track Inactivity: In Firebase User Collection, add a last_active (timestamp) field. Update this field using an action on app's home page
  - Log Custom Churn Events: Identify actions that indicate churn (e.g., clicking "Delete Account" or canceling a subscription). Use the "Log Event" action in FlutterFlow to send a user_churned event to Firebase Analytics.

