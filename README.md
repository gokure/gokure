<h3>
    
```python
from __future__ import annotations

import json
from dataclasses import asdict, dataclass


@dataclass
class Skill:
    languages : tuple[str, ...] = ("PHP", "Python", "Ruby", "Node.js", "Go", "Java")
    databases : tuple[str, ...] = ("MySQL", "MongoDB", "Redis", "Elasticsearch")
    frameworks: tuple[str, ...] = ("Laravel", "Hyperf", "Flask", "Django", "Vue.js")
    misc      : tuple[str, ...] = ("Linux", "Nginx", "Docker", "CI/CD", "RESTful", "GraphQL")
    ongoing   : tuple[str, ...] = ("Gin", "Coroutine")

    def jsonify(self) -> str:
        return json.dumps(asdict(self), indent=4)


skill = Skill()
print(skill.jsonify())
```
</h3>
