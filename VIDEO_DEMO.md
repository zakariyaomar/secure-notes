# Video Demonstration Guide

Target length: 2 to 3 minutes.

## Preparation

1. Start the API from `server` with `npm run dev`.
2. Start the client from `client` with `npm run dev`.
3. Open the client URL in a browser.
4. Use two distinct email addresses: User A and User B.

## Recording Script

### 0:00 - 0:20: Register User A

1. Open **Create one**.
2. Register User A with a name, email, and password.
3. Point out that registration signs the user in and opens **My Notes**.

### 0:20 - 1:05: Create and edit a note

1. Select **New Note**.
2. Create a note titled `Project plan`, with a short description and the `Work` category.
3. Select **Create** and show the note in the dashboard.
4. Select **Edit**, change the title or content, and select **Update**.
5. Select the note's **Pin** control to move it to the top of the list.

### 1:05 - 1:30: Search, filter, and delete

1. Enter `Project` in the search field and show the matching note.
2. Clear the search, select the `Work` category, and show the category filter result.
3. Clear the category filter.
4. Optionally create a temporary note and select **Delete** to demonstrate deletion without removing the main example note.

### 1:30 - 2:20: Prove notes are private

1. Log out from User A.
2. Select **Create one** and register User B.
3. Show that User B's dashboard is empty and does not show User A's `Project plan` note.
4. Create a note for User B, such as `User B private note`.
5. Log out, sign back in as User A, and show that User A sees only `Project plan`, not User B's note.

### 2:20 - 2:35: Close

1. Briefly show the pinned note, search box, and category filter.
2. State that each note is linked to the authenticated user and is only returned for that user.

## Privacy Explanation

The API assigns `userId` from the verified JWT token when a note is created. Every notes query filters by that same authenticated `userId`, and note reads, edits, pins, and deletes verify ownership before continuing.