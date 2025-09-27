# Areas Index

Use one note per area based on `99 Templates/Area Template`.

```dataview
TABLE health, owner
FROM "20 Areas"
WHERE type = "area" OR contains(file.folder, "20 Areas")
SORT file.name ASC
```


