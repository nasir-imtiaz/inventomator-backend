# Data Model Notes

### This document lists important notes related to the data-model of inventomator-backend.

> Last Updated: 20-06-2017
> Update author: inam@dexdevs.com


___
#### Foreign Key Naming Convention
```sql
fk_[referencing table name]_[referenced table name]_[referencing field name]
```

_**Example** with following tables:_
> task (id, user_id, title)
> note (id, task_id, user_id, note);
> user (id, name)

* FK for `task` will be: `fk_task_user_user_id`
* 1st FK for `note` will be: `fk_note_task_task_id`
* 2nd FK for `note` will be: `fk_note_user_user_id`
___
