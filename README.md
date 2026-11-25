# Windows & Git Bash Setup

Personal configuration and setup notes for Git Bash across IDEs (VS Code and Android Studio) on Windows.

## Git Bash Aliases Setup (VS Code & Android Studio)

Shared aliases live in [`.bash_aliases`](./.bash_aliases) (kept with LF line endings via [`.gitattributes`](./.gitattributes)).

### 1. Wire up home dotfiles (one-time per machine)

Run in Git Bash to create a one-way loading chain (`~/.bash_profile` → `~/.bashrc` → repo `.bash_aliases`):

```bash
echo '[ -f ~/.bashrc ] && . ~/.bashrc' > ~/.bash_profile
echo '[ -f /c/kyle/workspace/setup/.bash_aliases ] && . /c/kyle/workspace/setup/.bash_aliases' > ~/.bashrc
```

### 2. Android Studio Terminal

In **Settings → Tools → Terminal → Shell path**, set:

```text
"C:\Program Files\Git\bin\bash.exe" --login -i
```

### 3. Verify

Restart the terminal in VS Code and Android Studio and run `alias` (or `gs`).
