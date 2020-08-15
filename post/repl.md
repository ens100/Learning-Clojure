The last few days at work have been intense so I have not been able to dedicate too much time to my Clojure learning, but thankfully it is the weekend so that I can hopefully spend some time on this. 

Managed  to find a cool video which gives a good introduction of Clojure and how to get it set up in Intellij and run different things. I can now follow the various different steps and the purpose of REPL and how to make it run so that can evaluate the script. 

Today managed to:
- Follow the video (https://www.youtube.com/watch?v=jLsddw8_bt4&t=673s) + (https://www.youtube.com/watch?v=k8wgMG5AZIE&t=338s)
- Work out the shortcut for the REPL (Alt + Shift + P)
- Work through the various different Types and get an understanding of what each of them does
- Test the mangle and demangle functions 
- Understand that you can do ```Def``` followed by ```fn``` or use the shortcut ```Defn```

Feel quite content with my progress.

Discovered a few more tweaks / tips which I think are useful to know:
- Alt-Shift-P - will evaluate the top-level form your cursor is on in the REPL
- Alt-Shift-L - will load the file you are in, into the REPL
- Alt-Shift-M - will load all modified files into your REPL
- Alt-Shift-R - will change the REPL namespace to the one of the file you are in
- File -> Settings -> Keymap and search for Send form before caret to REPL and add the keyboard shortcut Ctrl+Enter for it. That way, when your cursor (caret) is at the end of any s-expr and evaluate the s-expr into the REPL by pressing: Ctrl+Enter.
