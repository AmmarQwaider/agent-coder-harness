# PowerShell Support

The hooks and automation scripts included in this harness (such as `verify-loop.sh` and `protected-branch-guard.sh`) are written in **Bash** by default to ensure universal compatibility across macOS, Linux, and WSL environments.

If you are running on a Windows environment and prefer to execute these hooks via PowerShell, you will need to:
1. Re-implement the `.sh` scripts as `.ps1` files in this directory.
2. Update the command paths in `.agent/hooks.json` to point to the new `.ps1` files.
3. Ensure your LLM agent is instructed to use `pwsh` or `powershell` when invoking commands.

Alternatively, you can run the Bash scripts seamlessly on Windows by using Git Bash or Windows Subsystem for Linux (WSL).
