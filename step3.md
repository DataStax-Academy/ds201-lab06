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
 <a href='command:katapod.loadPage?[{"step":"step2"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
<span class="step-count"> Step 3 of 3</span>
</div>

<!-- CONTENT -->

<div class="step-title">Explore the table using *nodetool*</div>

In this step you will explore the *killrvideo* keyspace

✅ Run *nodetool* to get information on the keyspace:
```
./nodetool tablestats killrvideo
```
Take your time to read through all the information pieces. Note that the value for the *SSTable count* metric is 0 for each table since our data currently only resides in the Commitlog and Memtables.

✅ Run *nodetool* with the `flush` command to flush in-memory Memtables to on-disk SSTables:
```
./nodetool flush
```
✅ Run *nodetool* with `tablestats` again to get information on the keyspace:
```
./nodetool tablestats killrvideo
```
The *SSTable count* should now be 1.

✅ You may wish to explore some other *nodetool* commands on your own like:

`./nodetool help tpstats`

`./nodetool help netstats`

`./nodetool help repair`

`./nodetool tpstats`

`./nodetool netstats` 



<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
  <a href='command:katapod.loadPage?[{"step":"step2"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
   <a href='command:katapod.loadPage?[{"step":"step4"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>
