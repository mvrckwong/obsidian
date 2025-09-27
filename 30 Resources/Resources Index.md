# Resources Index

Use one note per resource based on `99 Templates/Resource Template`.

```dataview
TABLE topic, source, date_added
FROM "30 Resources"
WHERE type = "resource" OR contains(file.folder, "30 Resources")
SORT date_added DESC
```


