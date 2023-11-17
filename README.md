# PowerShell-touch
Powershell function that creates an alias that functions like a rudimentary GNU coreutils touch
Rudimentary == Will create the file specified if it doesn't exist (and you have permission) or it will modify last mdoified time if the file already exists
example usage:
touch c:\temp\hello.txt

How to create your powershell profile (similar to .bashrc etc.):

Create your profile directory and file:
PS c:\>New-Item -ItemType Directory -Path (Split-Path $PROFILE)
PS c:\>New-Item -ItemType File -Path $PROFILE

Open your profile for editing:
PS c:\>notepad $PROFILE

Edit your profile (such as adding the touch-file function and alias)
Save your profile file->save

Reload your profile:
PS c:\>. $PROFILE

