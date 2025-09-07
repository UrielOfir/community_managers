---
layout: page
title: ארכיון מאמרים
permalink: /archive/
---

# ארכיון מאמרים וטיפים

כאן תוכלו למצוא את כל המאמרים והטיפים שפורסמו באתר, מאורגנים לפי קטגוריות ותאריכים.

## כל המאמרים לפי תאריך

{% for post in site.posts %}
### [{{ post.title }}]({{ post.url }})
**תאריך:** {{ post.date | date: "%d/%m/%Y" }}  
**קטגוריה:** {{ post.categories | join: ", " }}  
**מחבר:** {{ post.author | default: "צוות האתר" }}  

{{ post.excerpt | strip_html | truncatewords: 30 }}

[קרא עוד...]({{ post.url }})

---
{% endfor %}
