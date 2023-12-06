## Initializing pyromod

To initialize pyrobh, on the file that creates the client instance, simply import the Client class from pyrobh instead
of pyrogram:

```python
from pyrobh import Client
```

And that's all! You can still use the `Client` class as you would normally do with Pyrogram, but now having all the
extra features.

>You don't need to change the imports on the plugins files. Even by importing `Client` from pyrogram, the pyrobh  features will be available anyway.

>In order to monkeyatch pyrobh features successfully, it's just required that the  first `Client` class imported to your project code should be from pyrobh. Then all the other future `Client` instances  will be patched automatically.

>On custom plugins, you just need to import Client from pyrobh if you want your IDE to recognize and suggest
the extra features based on `pyrobh.Client` type.
