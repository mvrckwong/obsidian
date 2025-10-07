# 🚀 Data Engineering Hub

> **Visual Navigation**: Open [[Data Engineering Canvas.canvas|Data Engineering Canvas]] for visual exploration

## 📊 Quick Stats

```dataview
TABLE WITHOUT ID
	"📄 " + file.link as "Resource",
	topic as "Topic",
	date_added as "Added"
FROM "30 Resources/Data Engineering"
WHERE type = "resource"
SORT date_added DESC
LIMIT 10
```

---

## 🎯 By Category

### Maturity & Impact
```dataview
LIST
FROM "30 Resources/Data Engineering"
WHERE contains(tags, "kpis") OR contains(tags, "maturity") OR contains(tags, "impact")
SORT file.name
```

### Architecture & Tools
```dataview
LIST
FROM "30 Resources/Data Engineering"
WHERE contains(tags, "architecture") OR contains(tags, "tools") OR contains(tags, "stack")
SORT file.name
```

### Skills & Learning
```dataview
LIST
FROM "30 Resources/Data Engineering"
WHERE contains(tags, "skills") OR contains(tags, "learning") OR contains(tags, "career")
SORT file.name
```

---

## 🏷️ Browse by Tag

```dataview
TABLE WITHOUT ID
	rows.file.link as "Resources"
FROM "30 Resources/Data Engineering"
WHERE type = "resource"
FLATTEN tags as tag
GROUP BY tag
SORT tag
```

---

## 🔗 Recently Modified

```dataview
TABLE WITHOUT ID
	file.link as "Resource",
	file.mtime as "Last Modified"
FROM "30 Resources/Data Engineering"
WHERE type = "resource"
SORT file.mtime DESC
LIMIT 5
```

---

## 📚 Traditional Index
For a structured outline view, see: [[DE - Index]]

---

> 💡 **Tip**: Use the graph view to discover unexpected connections between concepts!
