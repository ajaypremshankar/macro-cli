
# macro-cli

**macro-cli** is a command-line tool designed to help users record and run macros directly from the terminal. This tool allows you to capture a sequence of commands, store them under a specific name, and then replay those commands as needed. It's particularly useful for automating repetitive tasks.

### Features

- **Record Macros**: Capture a series of commands under a specific name.
- **Run Macros**: Replay the commands in a recorded macro with a single command.
- **Simple CLI Interface**: Easily start, abort, finish, and run macros with straightforward commands.

### Requirements

- Python 3.6+
- `click` package (handled automatically during installation)

### Installation

To install **macro-cli** using `pip`:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/macro-cli.git
   cd macro-cli
   ```

2. Install with `pip`:
   ```bash
   pip install .
   ```

Or you can install it directly from [Homebrew](https://brew.sh/) if it's published:

```bash
brew install yourusername/tap/macro-cli
```

### Usage

Once installed, the `macro` command will be available in your terminal. Here’s how to use it:

#### 1. Start Recording a Macro

To start recording a macro, use:

```bash
macro record start <name>
```

Replace `<name>` with the name you’d like to give to this macro.

Example:
```bash
macro record start my_macro
```

#### 2. Abort Recording

If you want to stop recording without saving, use:

```bash
macro record abort
```

This will discard all commands recorded since the last `record start`.

#### 3. Finish Recording

To stop recording and save the commands to the macro, use:

```bash
macro record finish
```

The commands recorded between `record start` and `record finish` will be saved.

#### 4. Run a Macro

To replay the commands stored in a macro, use:

```bash
macro run <name>
```

Replace `<name>` with the name of the macro you want to run.

Example:
```bash
macro run my_macro
```

### Example Workflow

1. Start recording a macro named `backup`:
   ```bash
   macro record start backup
   ```

2. Run the commands you want to record, for example:
   ```bash
   cp ~/Documents/important-file.txt ~/Backups/
   echo "Backup completed"
   ```

3. Finish recording the macro:
   ```bash
   macro record finish
   ```

4. Now, whenever you want to execute the `backup` macro, simply run:
   ```bash
   macro run backup
   ```

### Uninstalling

To uninstall **macro-cli**, you can use `pip`:

```bash
pip uninstall macro-cli
```

Or if installed via Homebrew:

```bash
brew uninstall macro-cli
```

### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
