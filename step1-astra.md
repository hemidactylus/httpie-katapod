<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-2023.svg" />
  <div class="scenario-title-section">
    <span class="scenario-title">Exploring Stargate with HTTPie</span>
    <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:kirsten.hunter@datastax.com">email</a> or <a href="https://linkedin.com/in/synedra">LinkedIn</a>.</span>
  </div>
</div>


<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"intro"}]' 
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 1 of 5</span>
 <a href='command:katapod.loadPage?[{"step":"step2-astra"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Connect to Astra DB and create a database</div>

✅ Create an application token with the *Database Administrator* role to access Astra DB. Skip this step if you already have a token.

<ul>
  <li>Sign in (or sign up) to your Astra account at <a href="https://astra.datastax.com?utm_source=awesome-astra&utm_medium=social_organic&utm_campaign=httpie-katapod&utm_term=all-plays&utm_content=register">astra.datastax.com</a></li>
  <li>Create an application token with the <i>Database Administrator</i> role by following <a href="https://awesome-astra.github.io/docs/pages/astra/create-token/" target="_blank">these instructions</a></li>
</ul>

✅ Setup Astra CLI by providing the Database Administrator application token you created <a href="https://awesome-astra.github.io/docs/pages/astra/create-token/" target="_blank">here</a>:
```
astra setup
```

✅ Create database `workshops` and keyspace `library` if they do not exist:
```
astra db create workshops -k library --if-not-exist --wait
```

This operation may take a bit longer when creating a new database or resuming an existing hibernated database.

✅ Verify that database `workshops` is `ACTIVE` and keyspace `library` exists:
```
astra db get workshops
```

If the command fails, please revisit the previous steps to make sure that the database exists and is `ACTIVE`, and retry connecting to the database again.

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back - Astra Overview
 </a>
 <a href='command:katapod.loadPage?[{"step":"step2-astra"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️ Set up workspace credentials
  </a>
</div>
