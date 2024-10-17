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
<span class="step-count"> Step 1 of 3</span>
</div>

<!-- CONTENT -->

<div class="step-title">Create a <i>keyspace</i> and <i>table</i></div>

Cassandra should be installed in `/workspace/ds201-lab06/apache-cassandra-4.1.0/`.


✅ Change to the `./bin` directory:
```
cd /workspace/ds201-lab06/apache-cassandra-4.1.0/bin
```
✅ Look for *nodetool* in the directory:
```
ls -l
```
✅ Run *nodetool* with the help command and take your time to learn about various available commands:
```
./nodetool help
```
Some commands display information about the entire cluster and its nodes. Others may be specific to a node you connect to.

---
**Note:** The following commands have to connect to a running Cassandra node to get information about the cluster. You may have to run them more than once if your node(s) are not yet up.

---

✅ Run nodetool with the  `describecluster` command to display high-level information about the cluster:
```
./nodetool describecluster
```

✅ Run nodetool with the `status` command to display information about all nodes in the cluster:
```
./nodetool status
```

For each node, you should be able to see its state, IP address, load, and so forth. 

✅ Run nodetool with the `info` command to display information about this node:
```
./nodetool info
```
Take your time to read through all the information pieces.

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
   <a href='command:katapod.loadPage?[{"step":"step2"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>
