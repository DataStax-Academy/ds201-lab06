<!-- TOP -->
<div class="top">
  <img class="scenario-academy-logo" src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-2023.svg" />
  <div class="scenario-title-section">
    <span class="scenario-title">Nodetool</span>
    <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:academy@datastax.com">email</a>.</span>
  </div>
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
   <a href='command:katapod.loadPage?[{"step":"step2"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
<span class="step-count"> Step 1 of 4</span>
</div>

<!-- CONTENT -->

<div class="step-title">Create a *keyspace* and *table*</div>

Cassandra should be installed in `/workspace/ds201-lab06/apache-cassandra-4.1.0/`.


✅ Change to the `./bin` directory:
```
cd /workspace/ds201-lab06/apache-cassandra-4.1.0/bin
```
✅ Look for *nodetool* in the directory:
```
ls
```
✅ Run *nodetool* with the help command and take your time to learn about various available commands:
```
nodetool help
```

In the file find:

`# initial_token:`

Un-comment and change `initial_token` value setting it to `-9223372036854775808`. This will allow *node2* to manage half of the token range – all of the positive tokens and one negative token of `-9223372036854775808`

The new entry should look like:

`initial_token: -9223372036854775808`

Save and exit the editor.

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
   <a href='command:katapod.loadPage?[{"step":"step2"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>
