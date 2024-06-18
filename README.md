# Mutlipackage

Make sure that you have defined your packages in `pyproject.toml`
In this case:
```toml
[tool.poetry]

packages = [
    {include = "spanish", from="src"},
    {include = "german", from="src"},
    {include = "english", from="src"},
]
```

Install your package
```bash 
poetry install
```

Open a console
```bash
poetry shell
python 
```

Access the values from different packages:
```python
from german.base import GREETING as GERMAN
from english.base import GREETING as ENGLISH
from spanish.base import GREETING as SPANISH

print(GERMAN, ENGLISH, SPANISH)
```

