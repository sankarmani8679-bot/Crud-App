# Crud-App
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Event-focused CRUD To-Do App (Demo)</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header>
    <h1>Event-focused CRUD To‑Do App</h1>
    <div id="auth-area">
      <span id="welcome" class="hidden"></span>
      <button id="btn-show-signin">Sign In</button>
      <button id="btn-show-signup">Sign Up</button>
      <button id="btn-signout" class="hidden">Sign Out</button>
    </div>
  </header>

  <main>
    <section id="auth-forms" aria-live="polite">
      <!-- Sign In / Sign Up forms are toggled by buttons -->
      <form id="signin-form" class="auth-form hidden" autocomplete="on">
        <h2>Sign In</h2>
        <label>
          Email
          <input id="signin-email" name="email" type="email" required placeholder="you@example.com" />
        </label>
        <label>
          Password
          <input id="signin-password" name="password" type="password" required minlength="6" />
        </label>
        <div class="form-actions">
          <button type="submit">Sign In</button>
          <button type="button" id="signin-cancel">Cancel</button>
        </div>
      </form>

      <form id="signup-form" class="auth-form hidden" autocomplete="on">
        <h2>Create Account</h2>
        <label>
          Name
          <input id="signup-name" name="name" type="text" required placeholder="Your name" />
        </label>
        <label>
          Email
          <input id="signup-email" name="email" type="email" required placeholder="you@example.com" />
        </label>
        <label>
          Password
          <input id="signup-password" name="password" type="password" required minlength="6" />
        </label>
        <label>
          Confirm Password
          <input id="signup-password2" name="password2" type="password" required minlength="6" />
        </label>
        <div class="form-actions">
          <button type="submit">Sign Up</button>
          <button type="button" id="signup-cancel">Cancel</button>
        </div>
      </form>
    </section>

    <section id="todo-app" class="hidden" aria-live="polite">
      <h2>My To-Do / Events</h2>

      <form id="todo-form">
        <input id="todo-input" type="text" placeholder="Add an event or todo and press Enter" required />
        <select id="todo-priority" name="priority" title="Set priority">
          <option value="low">Low</option>
          <option value="medium" selected>Medium</option>
          <option value="high">High</option>
        </select>
        <button type="submit">Add</button>
      </form>

      <div id="todo-controls">
        <label>
          Filter
          <select id="filter">
            <option value="all">All</option>
            <option value="active">Active</option>
            <option value="done">Done</option>
          </select>
        </label>
        <button id="clear-done">Clear Done</button>
      </div>

      <ul id="todo-list" aria-label="Todo list"></ul>
    </section>

    <aside id="event-panel">
      <h3>Event Log</h3>
      <div id="events"></div>
      <button id="clear-events">Clear Log</button>
    </aside>
  </main>

  <footer>
    <small>Demo app — not production ready. Passwords stored in localStorage for demo only.</small>
  </footer>

  <script src="app.js"></script>
</body>
</html>
