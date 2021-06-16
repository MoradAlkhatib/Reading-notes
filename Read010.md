# Code Debugging
Programming code might contain syntax errors, or logical errors.

Many of these errors are difficult to diagnose.

Often, when programming code contains errors, nothing will happen. There are no error messages, and you will get no indications where to search for errors.

Searching for (and fixing) errors in programming code is called code debugging.

# JavaScript Debuggers
Debugging is not easy. But fortunately, all modern browsers have a built-in JavaScript debugger.

Built-in debuggers can be turned on and off, forcing errors to be reported to the user.

With a debugger, you can also set breakpoints (places where code execution can be stopped), and examine variables while the code is executing.

Normally, otherwise follow the steps at the bottom of this page, you activate debugging in your browser with the F12 key, and select "Console" in the debugger menu.

## The console.log() Method
If your browser supports debugging, you can use console.log() to display JavaScript values in the debugger window

# Setting Breakpoints
In the debugger window, you can set breakpoints in the JavaScript code.

At each breakpoint, JavaScript will stop executing, and let you examine JavaScript values.

After examining values, you can resume the execution of code (typically with a play button).

# The debugger Keyword
The debugger keyword stops the execution of JavaScript, and calls (if available) the debugging function.

This has the same function as setting a breakpoint in the debugger.

If no debugging is available, the debugger statement has no effect.

# Major Browsers' Debugging Tools
Normally, you activate debugging in your browser with F12, and select "Console" in the debugger menu.

Otherwise follow these steps:

## Chrome
- Open the browser.
- From the menu, select "More tools".
- From tools, choose "Developer tools".
- Finally, select Console.
## Firefox
- Open the browser.
- From the menu, select "Web Developer".
- Finally, select "Web Console".
## Edge
- Open the browser.
- From the menu, select "Developer Tools".
- Finally, select "Console".
## Opera
- Open the browser.
- From the menu, select "Developer".
- From "Developer", select "Developer tools".
- Finally, select "Console".
## Safari
- Go to Safari, Preferences, Advanced in the main menu.
- Check "Enable Show Develop menu in menu bar".
- When the new option "Develop" appears in the menu:
- Choose "Show Error Console".
