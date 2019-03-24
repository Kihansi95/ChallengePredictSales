* **Cannot import get_installed_distributions**: Replace in __ingestion_program/data_io.py__ at line 37
```python
from pip import get_installed_distributions
```
by
```python
try:
    from pip._internal.utils.misc import get_installed_distributions
except ImportError:  # pip<10
    from pip import get_installed_distributions
```

* **No module named 'psutil'**: 
