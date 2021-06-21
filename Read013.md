# Window localStorage Property
## Definition and Usage
The localStorage and sessionStorage properties allow to save key/value pairs in a web browser.

The localStorage object stores data with no expiration date. The data will not be deleted when the browser is closed, and will be available the next day, week, or year.

The localStorage property is read-only.

## Syntax
window.localStorage
Syntax for SAVING data to localStorage:

localStorage.setItem("key", "value");
Syntax for READING data from localStorage:

var lastname = localStorage.getItem("key");
Syntax for REMOVING data from localStorage:

localStorage.removeItem("key");
Technical Details
Return Value:	A Storage object
## Example
The following example counts the number of times a user has clicked a button:

if (localStorage.clickcount) {
  localStorage.clickcount = Number(localStorage.clickcount) + 1;
} else {
  localStorage.clickcount = 1;
}
document.getElementById("result").innerHTML = "You have clicked the button " +
localStorage.clickcount + " time(s).";
## What is localStorage and how does it work?
LocalStorage is a way of storing data permanently in the browser. Unlike setting a normal variable, it does not reset when you reload the page, and you can access the same localStorage data from any page on your website.

LocalStorage is a key-value store, meaning that you store data with a key. A key is a ‘label’ for the data that you can use to retrieve it, kind of like a variable name. For example, you could save the user’s high score in a game using a key of highScore.

All localStorage data gets converted to a string before saving, even if it’s not a string to begin with.

## Inspecting localStorage
Google Chrome has a built-in tool to help you view the data that you have stored in localStorage. Many other browsers also have similar tools. To open the localStorage inspector in Google Chrome, start by right-clicking on your page, then clicking “Inspect Element”. From here, go to the “Application” tab.
You may need to click the little arrow in the inspector tab bar to find it:

![Image](https://cdn.statically.io/img/codetheweb.blog/assets/img/posts/javascript-localstorage/inspector-application-tab-button.png?f=webp&w=720)
![Image](https://cdn.statically.io/img/codetheweb.blog/assets/img/posts/javascript-localstorage/inspector-application-localstorage-table.png?f=webp&w=720)
Great! This is where our data will show up once we start setting stuff in localStorage.

Note that if you’re using an HTML file that you’ve opened up in your browser, you may already see some data in there. This is because all page URLs starting with file:// use the same localStorage area. Normally, each domain name has its own localStorage area. So example.com, google.com and blog.example.com would all have different localStorage areas. Setting an item in localStorage for one of them would not set it for the others.

Adding and updating data with localStorage.setItem
Let’s get started by adding some data to localStorage!

We can use the localStorage.setItem function to do this. It takes two parameters — the key to store the data under, and the value that you want to store. For example, this code sets the key fullName to Jenny Smith in localStorage:
![Image](https://cdn.statically.io/img/codetheweb.blog/assets/img/posts/javascript-localstorage/full-name-jenny-smith.png?f=webp&w=720)
