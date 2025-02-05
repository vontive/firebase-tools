# Integrate React

Using the Firebase CLI, you can deploy your React static web apps to Firebase 
and serve them with Firebase Hosting.

Note: Framework-aware Hosting is an early public preview. This means
that the functionality might change in backward-incompatible ways. A preview
release is not subject to any SLA or deprecation policy and may receive limited
or no support.

## Before you begin

Before you get started deploying your app to Firebase,
review the following requirements and options:

- Firebase CLI version 12.1.0 or later. Make sure to
  [install the CLI](/docs/cli#install_the_firebase_cli) using your preferred 
	method.
- Optional: An existing React project using Vite. You can create one with 
	`npm create vite@latest -- --template react` or let the Firebase CLI
	 [initialize a new project](#initialize-a-new-project) for you.


## Initialize Firebase

To get started, initialize Firebase for your framework project.
Use the Firebase CLI for a new project, or modify `firebase.json` for an
existing project.

### Initialize a new project

1. In the Firebase CLI, enable the web frameworks preview:
   <pre class="devsite-terminal">firebase experiments:enable webframeworks</pre>
1. Run the initialization command from the CLI and then follow the prompts:
   <pre class="devsite-terminal">firebase init hosting</pre>
1.  Answer yes to "Do you want to use a web framework? (experimental)"
1.  Choose your hosting source directory.  If there is an existing React 
    codebase (with Vite), the CLI detects it and the process completes.

## Serve static content

After initializing Firebase, you can serve static content with the standard
deployment command:

```shell
firebase deploy
```

You can [view your deployed app](/docs/hosting/test-preview-deploy#view-changes)
on its live site.
