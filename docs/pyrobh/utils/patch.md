### *function* pyrobh.utils.patch_into(target_class)

The `pyrobh.utils.patch_into` decorator is a function used to facilitate monkeypatching of pyrogram classes with custom
methods from pyrobh.

### *Parameters:*

- **target_class** (*Type*) - The target class or Pyrogram class to which you want to apply the patch.

### *Returns:*

A decorated class containing the patched methods. Each replaced method is now available prefixed with `old` in the
decorated class (e.g. `__init__` becomes `old__init__`).

### *function* pyrobh.utils.should_patch(func)

The pyrobh.utils.should_patch` decorator is a function used to specify that a method should be patched into a target class.
It marks a method as patchable, indicating that it should be considered for monkeypatching by `pyrobh.utils.patch_into`. This
decorator is used in conjunction with the `pyrobh.utils.patch_into` decorator.

### *Parameters:*

- **func** (*Type*) - The method to be marked as patchable.

### *Returns:*

The same method with the `should_patch` attribute set to `True`.
