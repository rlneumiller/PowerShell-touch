Here is the markdown formatted text:

# PowerShell-touch
This PowerShell function creates an alias that functions like a rudimentary GNU coreutils touch. The function will create the file specified if it doesn't exist (and you have permission) or it will modify last modified time if the file already exists.

## Example usage:
```powershell
touch c:\temp\hello.txt
```

## How to create your PowerShell profile (similar to .bashrc etc.):
1. Create your profile directory and file:
```powershell
New-Item -ItemType Directory -Path (Split-Path $PROFILE)
New-Item -ItemType File -Path $PROFILE
```
2. Open your profile for editing:
```powershell
notepad $PROFILE
```
3. Edit your profile (such as adding the touch-file function and alias).
4. Save your profile file.
5. Reload your profile:
```powershell
. $PROFILE
```

### Find the location of your $PROFILE:
```powershell
$PROFILE.CurrentUserCurrentHost
```

