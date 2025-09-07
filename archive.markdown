---
layout: page
title: ארכיון מאמרים
permalink: /archive/
---

# ארכיון מאמרים וטיפים

כאן תוכלו למצוא את כל המאמרים והטיפים שפורסמו באתר, מאורגנים לפי קטגוריות ותאריכים.

## לפי קטגוריות

### 📋 **טיפים וניהול**
{% for post in site.categories["טיפים ניהול"] %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%d/%m/%Y" }}
{% endfor %}

### 🛠️ **כלים וסקירות**
{% for post in site.categories["כלים סקירות"] %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%d/%m/%Y" }}
{% endfor %}

### 📢 **הודעות כלליות**
{% for post in site.categories["הודעות כלליות"] %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%d/%m/%Y" }}
{% endfor %}

### 🎯 **מעורבות קהילה**
{% for post in site.categories["מעורבות קהילה"] %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%d/%m/%Y" }}
{% endfor %}

### 💼 **קריירה ופיתוח מקצועי**
{% for post in site.categories["קריירה פיתוח"] %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%d/%m/%Y" }}
{% endfor %}

---

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

---

*לא מוצאים מה שחיפשתם? [צרו קשר]({{ site.baseurl }}/contact/) ואנחנו נעזור לכם למצוא את המידע הדרוש.*
