---
title: "Markdown cheatsheet (draft — not published)"
date: 2026-10-05
tags: ["meta"]
draft: true
---

This post is a **draft**, so it only shows up when you run `hugo server -D` locally.
Use it as a reference for what the site can render, then delete it whenever you like.

## Headings

Use `##` for sections and `###` for sub-sections.

### Links and emphasis

Here's a [link](https://gohugo.io), some *italic*, some **bold**, and some `inline code`.

## Lists

1. First
2. Second
3. Third

- A bullet
- Another bullet

## Quote

> Rest days are training days.

## Code

```go
package main

import "fmt"

func main() {
	fmt.Println("hello, world")
}
```

## Images

Put images in `static/images/` and reference them like this:

```markdown
![Alt text describing the photo](/images/your-photo.jpg)
```

---

That's it.
