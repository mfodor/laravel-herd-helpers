# PHP Debug switcher for Mac

## Installation

### ARM (Mx chips)

Make sure the file is executable, copy the file to a directory in your shell PATH and there you go!

```bash
chmod +x arm/phpdebug
sudo cp arm/phpdebug /usr/local/bin/phpdebug
```

### Intel

Copy the executable to a directory in your shell PATH and there you go!

```bash
chmod +x intel/phpdebug
sudo cp intel/phpdebug /usr/local/bin/phpdebug
```

## Usage

```
PHP xdebug toggler for Herd Free
Usage:
➜ phpdebug <action: on|off|add|remove> [<version=82 (74|80|81|82|83)>]
```

*All actions will restart Herd to apply the changes.*

### Example

Running the following command will turn the debugger on for PHP v8.3

```
phpdebug on 83
```

### ‼️

If you never turned on the debugger before, you must use `add` action instead of `on`.

### Actions

#### Add

It will add the needed configurations to the php.ini of the selected version.

#### Remove

It will remove the debug configurations from the php.ini of the selected version.

‼️ If you use `remove`, you have to use `add` the next time you want to use debug.

#### On

Once added, you can uncomment the debug configs with the `on` action.

#### Off

Once added, you can comment the debug configs with the `off` action.
