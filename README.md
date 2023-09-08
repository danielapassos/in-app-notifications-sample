# Knock — In-app notifications in React


## How this example works

Given that a notification feed is stateful, when a new session is opened we automatically `identify` a new user in Knock and persist the `userId` generated into local storage. We then use this `userId` to route notification messages to on the in-app feed.

You can see how we identify users and send notify calls to Knock in the `pages/api` directory. These functions are executed on the server-side by Next.

For our in-app toasts, we listen to all real-time messages coming in that have the `showToast` property not set to `false`. We'll then display a toast prompt using our custom `Toast` component.
