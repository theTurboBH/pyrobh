### *exception* pyromod.exceptions.ListenerStopped

The `ListenerStopped` exception is raised in pyrobh when a listener is explicitly stopped (
using `Client.stop_listening`) during bot execution. This
exception is used to indicate that a specific listener was intentionally terminated and will only be raised if
the `throw_exceptions` setting in the pyrobh `config` is set to `True`.

* **Usage**

```python
from pyrobh.exceptions import ListenerStopped

try:
    message = await Client.listen(...)
except ListenerStopped:
    print("Listener was stopped")
```