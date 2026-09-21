## 🎯 The MVP Value Proposition

For busy, fast-casual restaurants overwhelmed by disjointed QR orders, our platform is a lightweight web workflow that unifies table orders before they hit the kitchen and synchronizes prep milestones in real time. Unlike Toast or Square, we protect kitchen pacing and keep diners informed without complex hardware or app downloads.

----

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

----

## PM Brainstorming: Breaking Down the Core Innovations
To make this MVP truly impactful, we need to design the Must-Have features with a highly specific product logic:

## 1. The "Anti-Chaos" Unified Cart

* The Product Logic: Instead of treating every individual smartphone scan as an independent customer session, our backend needs to create a single, live-syncing "room bucket" tied strictly to the table_id.
* The UX Flow: When User A adds a burger and User B adds tacos at Table 4, they both see the items appearing in real time on their respective screens. The order cannot be fired until someone clicks the collective "Review & Fire" button.
* Why this wins: It completely eliminates the "Ghost Order" problem. The kitchen gets one clean ticket for the table, allowing the chef to pace the execution correctly.

## 2. Guardrailed Allergy Alerts

* The Product Logic: We are ditching the traditional text box buried at the bottom of the checkout screen.
* The UX Flow: When a user selects a modification or types an allergy note, our system flags it with a high-priority data attribute. On the KDS dashboard, this text automatically scales up and renders in bold, flashing, or high-contrast red font.
* Why this wins: It forces the kitchen line's eyes right to the restriction. No more dropped tickets or chefs walking out to the floor to read bad handwriting.

## 3. Two-Way Micro-Status Communication

* The Product Logic: The KDS isn't just a static "Done" checklist. It is a live state-machine.
* The UX Flow: When a line cook moves a ticket from Pending → Preparing, a WebSocket event fires immediately. The diner’s phone screen shifts from a grey "Received" state to an amber "Cooking" state. When bumped to Ready, it flashes vibrant green.
* Why this wins: It bridges the information asymmetry. Diners stop harassing busy waitstaff with "Where is my food?" because their phone tells them exactly what stage it's in.

------------------------------

## What we are actively ignoring
To hit our 4-day deadline,

* No Payments: Diners will pay the waiter at the end via the house traditional POS. We are managing operations, not transactions right now.
* No Authentication: No "Sign up with Google" or phone number verification. If they are sitting at Table 5, their physical location is their authorization token.

----------------------


