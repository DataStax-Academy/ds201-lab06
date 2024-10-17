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
 <a href='command:katapod.loadPage?[{"step":"step1"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
  <a href='command:katapod.loadPage?[{"step":"step3"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
<span class="step-count"> Step 2 of 3</span>
</div>

<!-- CONTENT -->

<div class="step-title">Create the <i>killrvideo</i> keyspace and the <i>videos</i> table</div>


✅ Start *cqlsh*
```
./cqlsh
```
✅ Create the *killrvideo* keyspace:
```
CREATE KEYSPACE IF NOT EXISTS killrvideo
WITH replication = {
  'class':'SimpleStrategy', 
  'replication_factor': 1
};
```
✅ Use the keyspace:
```
use killrvideo;
```
✅ Create the *videos* table:
```
CREATE TABLE IF NOT EXISTS videos (
  video_id TIMEUUID,
  added_date TIMESTAMP,
  title TEXT,
  PRIMARY KEY (video_id)
);
```
✅ Populate the *videos* table:
```
COPY videos(video_id, added_date, title)
FROM '/workspace/ds201-lab06/data-files/videos.csv'
WITH HEADER=TRUE;
```
✅ Verify that the data was loaded:
```
SELECT * from videos;
```
You should see that six rows have been added to the table.

✅ Exit *cqlsh*:
```
exit
```
<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
  <a href='command:katapod.loadPage?[{"step":"step1"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
  <a href='command:katapod.loadPage?[{"step":"step3"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>
