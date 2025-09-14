
| Skill | Level |
| ---- | ---- |
{% assign skills = site.data.skills.soft_skills | sort: "title" -%}
{% for skill in skills -%}
| {{skill.name}} | {{skill.level}} |
{% endfor %}