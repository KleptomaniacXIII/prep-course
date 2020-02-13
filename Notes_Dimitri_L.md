## 12/02/2020 - Setting up GitHub and VS Code.

## After setting up VS Code with GitHub Desktop I wasn't able to use Terminal inside VS Code as it's shown on work-station-setup.md and README.md
 - Aparently it was due to by default Terminal used in VS Code was set to be Comand Prompt -  'C:/WINDOWS/System32/cmd.exe' 
 The line begun with Project path the way Windows Comand Prompt : C:\Users\dimit>(projet path) and using the terminal I couldn't execute such commands as checking version of packages or installing a package. While I could do those commands in cmd.exe ensuring packages are installed.
 - I found Settings insde Terminal window (at the drop down menu for switching between active terminals) "Select Default Shell" - that opened a drop down list of shells at the top. Could see 3 : Command Prompt, Power Shell, GitBash. However none could be selected with aparent change to Terminal or it's function.

##  This I could resolve by visiting GitHub Desktop application: File->Options->Integrations->Applications->Shell (where same 3 Shells available to choose from)
- By switching to GitBash inside settings in GitHub Desktop my terminal command line inside VS Code chnaged to :
    - 'dimit@DESKTOP-6U24HEH MINGW64 ~/OneDrive/Documents/GitHub/prep-course (master)'

## 13/02/2020
## This allowed me to used commands as -v , --version as well as install packages. 
 - But then again running command - | ts-node -e "console.log('Hello World!')" | threw at me an error: | bash: !': event not found |
 

dimit@DESKTOP-6U24HEH MINGW64 ~/OneDrive/Documents/GitHub/prep-course (master)
$ npm install -g ts-node
C:\Users\dimit\AppData\Roaming\npm\ts-node -> C:\Users\dimit\AppData\Roaming\npm\node_modules\ts-node\dist\bin.js
C:\Users\dimit\AppData\Roaming\npm\ts-script -> C:\Users\dimit\AppData\Roaming\npm\node_modules\ts-node\dist\script.js
npm WARN ts-node@8.6.2 requires a peer of typescript@>=2.7 but none is installed. You must install peer dependencies yourself.

+ ts-node@8.6.2
added 8 packages from 40 contributors in 3.389s

dimit@DESKTOP-6U24HEH MINGW64 ~/OneDrive/Documents/GitHub/prep-course (master)
$ npm install -g typescript
C:\Users\dimit\AppData\Roaming\npm\tsserver -> C:\Users\dimit\AppData\Roaming\npm\node_modules\typescript\bin\tsserver
C:\Users\dimit\AppData\Roaming\npm\tsc -> C:\Users\dimit\AppData\Roaming\npm\node_modules\typescript\bin\tsc
+ typescript@3.7.5
updated 1 package in 9.223s

dimit@DESKTOP-6U24HEH MINGW64 ~/OneDrive/Documents/GitHub/prep-course (master)
$ node -v
v12.16.0

dimit@DESKTOP-6U24HEH MINGW64 ~/OneDrive/Documents/GitHub/prep-course (master)
$ npm -v
6.13.4

dimit@DESKTOP-6U24HEH MINGW64 ~/OneDrive/Documents/GitHub/prep-course (master)
$ ts-node -e "console.log('Hello World!')"
bash: !': event not found

## Running the same command inside cmd.exe it works:

Microsoft Windows [Version 10.0.18362.657]
(c) 2019 Microsoft Corporation. All rights reserved.

C:\Users\dimit>ts-node -e "console.log('Hello World!')"
Hello World!

C:\Users\dimit>

## Worked
- by typing firstly "ts-node"

- Then "console.log('Hello World!')"

dimit@DESKTOP-6U24HEH MINGW64 ~/OneDrive/Documents/GitHub/prep-course (Notes)
$ ts-node
> console.log('Hello, World!')
Hello, World!
undefined

But not sure if it's the right way to do. Found this approach on this website: https://riptutorial.com/typescript/example/28089/running-typescript-using-ts-node
