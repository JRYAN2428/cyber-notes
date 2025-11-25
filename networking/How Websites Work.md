# How Websites Work

## **Two major components of a website**
- The **Front End** (Client side); how the browser looks at the website
- The **Back End** (Server side); server processes request > returns response

## Primary methods of website creation:**
- HTML; builds websites and structure
- CSS; presentation-side
- JavaScript; Implement complex features, user interactivity

HTML = HyperText Markup Lnaguage
- Is the language websites are written in
- Elements = tags; vice versa; > Building blocks of HTML pages > Tells browser how to display content

**HTML STRUCTURE:**
- <!DOCTYPE html> defines the page as HTML5 doc. Standardisation
- <html> element/tag > root element of HTML page - ALL other elements/tags come after this element
- <head> element/tag contains information about the page like page title
- <body> defines HTML doc body; only content inside of the body is shown in the browser
- <p> defines a paragraph
There are many other elements/tags
### Tags can also:
- Have a class attribute > ```<p class="bold-text">```
- Have an src attribute (specifies location of image); ```<img src="img/cat.jpg">```
  - src specifies **_location of the image relative to the HTML document. ```<img src="img/cat.jpg">``` indicates the image 'cat.jpg' is located in an 'img' folder_**
- Have an 'id' attribute ```<p id="example">```, becomes unique to the element. Elements need different id's to identify them uniquely. Often used for styling and to identigy it by JavaScript


---


# **Example Code**

## Adding Images

```<!DOCTYPE html>
<html>
    <head>
        <title>TryHackMe HTML Editor</title>
    </head>
    <body>
        <h1>Cat Website!</h1>
        <p>See images of all my cats!</p>
        <img src='img/cat-1.jpg'>
        <img src='img/cat-2.'>
        <!-- Add dog image here -->
    </body>
</html>
```

## Adding buttons

```<!DOCTYPE html>
<html>
<button onclick='document.getElementById("demo").innerHTML = "Button Clicked";'>Click Me!</button>
    <head>
        <title>TryHackMe Editor</title>
    </head>
    <body>
        <div id="demo">Hi there!</div>
        <script type="text/javascript">
            // add your JavaScript here
        </script>
    </body>
</html>
```

---

# Sensitive Data Exposure
- Occurs when websites don't properly remove clear-text information to the end user; usually found in frontend source code
- Page source can have data like login credentials, private links, or other things
- Can leverage source code information for data to use in other applications, to then get further access and exploits

## HTML Injection
- Vulnerability when the website doesn't sanitise information inputted from the user
- Can therefore 'inject' malicious code
- HTML injection is Client side

# My custom script for tutorial

## Self Dive
- The <a> tag is used to create hyperlinks
- The 'href' attribute specifies the URL of the page link goes to
---
```<HTML>
  <script
    <a href='http://hacker.com'>Click here</a>
</HTML>
```
The above version is incorrect; the correct version below
```<html>
  <body>
    <a href='http://hacker.com'>Click here</a></body></html>
```



  


