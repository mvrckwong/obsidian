# Brainstorms Index

Create new brainstorms from `99 Templates/Brainstorm Template` and store in this folder.

```dataview
TABLE topic, date, inspired_by
FROM "30 Resources/Brainstorms"
WHERE type = "brainstorm" OR contains(file.folder, "30 Resources/Brainstorms")
SORT date DESC
```


