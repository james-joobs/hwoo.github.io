---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---


## 👋 Welcome to Hwoo's Blog!

I'm **Hyunwoo Joo**, a Machine Learning Engineer with a Ph.D. in Artificial Intelligence. I specialize in **3D Computer Vision**, **Embodied AI**, and **MLOps**. 

🔗 **[View My Portfolio](/portfolio/)** | 🛠️ **[See My Projects](/projects/)** | 📧 **[Contact Me](mailto:stevepaulljobs@gmail.com)**

---

## Latest Reviews
{% assign reviews = site.reviews | sort: 'date' | reverse %}
{% for review in reviews limit:3 %}
  - [{{ review.title }}]({{ review.url | relative_url }}) - {{ review.date | date: "%B %d, %Y" }}
{% endfor %}

## Recent News
{% assign news = site.news | sort: 'date' | reverse %}
{% for item in news limit:3 %}
  - [{{ item.title }}]({{ item.url | relative_url }}) - {{ item.date | date: "%B %d, %Y" }}
{% endfor %}

## Recent Thoughts
{% assign thoughts = site.thoughts | sort: 'date' | reverse %}
{% for thought in thoughts limit:3 %}
  - [{{ thought.title }}]({{ thought.url | relative_url }}) - {{ thought.date | date: "%B %d, %Y" }}
{% endfor %}

