
| Skill | Level |
| ---- | ---- |
{% assign skills = site.data.skills.language | sort: "title" -%}
{% for skill in skills -%}
| {{skill.title}} | {{skill.level}} |
{% endfor %}