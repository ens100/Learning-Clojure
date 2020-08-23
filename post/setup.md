# Set Up

So, I was under the impression that the first step to get any program running is to install something, sounds easy right, how wrong I was.  I have a tiny (maybe minuscule is better) bit of experience in Phyton so had a little bit of an idea of what to expect but I was not prepared mentally for what was coming up - things are a little trickier here.

From having to sign up to GitHub and learn about what it is (optional) and then having to find and download different JDK / J SE files,  to doing something with Leiningen followed by some chocolate (mmmm chocolate) - I was all over the place and feeling a little overwhelmed with information overload. 

Anyway, what I did was throw my computer out of the window....no, seriously, I closed all of my Chrome tabs and started one step at a time. 

Here are the steps I carried out:

1. Download and install "Java SE Runtime Environment 8u251" from (https://oraclemirror.np.gy/jre8/)
2. Download IntelliJ from https://www.jetbrains.com/idea/download/#section=windows
3. Run PowerShell and type "java -version" to see that it has installed and you have the latest versions - **maybe this should have been step 1 - oh well, I like living on the edge**
4. Install from Chocolatey (Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1')))
5. Run the Leiningen installation using Chocolatey: `choco install lein`
	2. There may be a few prompts to which i selected Y or A
5. Open terminal and type: `lein repl`

and Voila! following the above I was able to get Clojure up and running. 

To celebrate, I typed "nil" and it returned `nil`. 

Great Success!


# New Project

Here are the steps I followed to get a new project up and running

1. In Powershell run "Lein new app name" (name represents the name you choose)
2. cd "name"
3. lein run
	1. Should show "hello world"

Open Intellij
1. Open Project - find Project.clj of project
2. Open as project
3. Add Configuration -> Leiningen
4. Clojure REPL - Add configuration -> Clojure REPL -> local
5. Press play and the REPL should show up on the side

Very good so far, we have Clojure installed and managed to get it up and running. High Five!
