To build a working prototype in 4 days using a simple tech stack (Next.js and Supabase/Firebase), the features are split into immediate implementation and future scope.

## 🛠️ Core Features (To Be Implemented Now)

* QR-Table Link: Simple links like /table/[id] open the menu and assign the table number instantly without a login.
* Shared Table Cart: One shared digital cart for the entire table so individual orders stay grouped together.
* "Review & Fire" Button: A final button to submit the entire table's order to the kitchen at one time.
* Kitchen Kanban Board: A real-time screen for cooks that displays new orders instantly as columns.
* One-Tap Status Updates: Kitchen staff tap a single button to change order tags from Pending ➔ Preparing ➔ Ready.
* Live Guest Tracker: A simple, self-updating screen for diners showing the current state of their food.
* Red Allergy Text: Custom order notes render in bold red font on the kitchen screen so they are never missed.
* Screen Flash & Sounds: The diner's screen flashes green when food is ready, and the kitchen tablet pings when new orders arrive.
* Quick Item Hide (86ing): A fast button for the chef to mark a dish out-of-stock and grey it out on the guest menu.

## 🚀 Future Scope (Post-MVP)

* Wait Time Guesses: Showing an estimated cooking time based on how busy the kitchen screen is.
* Call Server Button: A digital buzzer for guests to summon a waiter to their table.
* In-App Payments: Adding Stripe or Apple Pay tools so guests can pay directly from the web app.
* Smart Course Splitting: Automated code to separate and time appetizers from main courses on the kitchen screen.
* Profiles & Accounts: Saving user accounts, login history, and favorite food items for repeat diners.

--------------

## Innovative space

This solution brings three core innovations to the restaurant tech space:

## 1. The "Anti-Chaos" Unified Cart

* The Innovation: Instead of treating every individual smartphone scan as an independent customer, your system creates a single, live-syncing room bucket for the entire table.
* The Impact: It acts as a digital gatekeeper. It stops the kitchen from getting flooded with 8 separate tickets for one table, protecting course timing without requiring a server to manually combine orders.

## 2. Guardrailed Allergy Alerts

* The Innovation: Custom modifications and dietary notes bypass standard small-text logs. They are formatted automatically to display in bold, high-contrast red directly on the main KDS ticket line.
* The Impact: It removes human error caused by bad handwriting or forgotten verbal warnings. Chefs instantly see safety risks without stopping the cooking line.

## 3. Two-Way Micro-Status Communication

* The Innovation: Your KDS transitions away from a static "Done/Not Done" checkbox. It broadcasts exact preparation milestones (Pending ➔ Preparing ➔ Ready) across WebSockets back to the guest's mobile browser and the waitstaff's devices.
* The Impact: It bridges the communication gap between the floor and the kitchen. Guests lose their waiting anxiety, and servers never have to run back to the kitchen window to check on an order.




