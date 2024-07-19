# Litlyx Nuxt 3 Example

This project demonstrates the integration of Litlyx with a Nuxt 3 application. Follow the steps below to get started.

## Setup Instructions

1. **Sign Up on Litlyx Cloud**
   - Visit the [Litlyx Dashboard](https://dashboard.litlyx.com) and sign up for an account.

2. **Create a New Project**
   - After signing in, create a new project in the Litlyx Dashboard.

3. **Copy Your Project ID**
   - Once your project is created, copy the `project_id` from the dashboard.

4. **Initialize Litlyx in Your Nuxt Project**
   - Replace `PROJECT_ID` in the `Lit.init("PROJECT_ID")` function with your actual `project_id`.

   ```typescript
   <script lang="ts" setup>
   import { Lit } from 'litlyx-js';

   Lit.init("YOUR_PROJECT_ID");

   function onButtonClick() {
     Lit.event('NuxtExampleButtonClick', {
       metadata: {
         title: 'Nuxt is awesome',
         subtitle: 'Litlyx too!'
       }
     })
   }
   </script>
   ```

5. **Reload the Page**
   - Reload your Nuxt application to trigger your first visit event.

6. **(Optional) Test a Custom Event**
   - Click the "Test your event" button to trigger a custom event defined in the `onButtonClick` function.

## Testing

- After setting up and initializing your project with Litlyx, reload your application.
- Click the "Test your event" button to ensure the custom event is triggered correctly.

Enjoy using Litlyx with your Nuxt 3 project!

## Links

- [Website](https://litlyx.com)
- [Discord](https://discord.gg/9cQykjsmWX)
- [Docs](https://docs.litlyx.com)
