# Your First Webpage

Alright, the moment you've been waiting for!  Let's get to writing out code.  The first thing you'll need is a code editor.  

So let's download and install [Visual Studio Code](https://code.visualstudio.com/), the recommended code editor for our course.  You'll also want to enable a few extensions for Visual Studio Code, including syntax highlighting and enabling the PATH command to allow you to run `code` from the command line to open a project with the editor. [Instructions](https://code.visualstudio.com/docs/setup/mac).

**Navigate over to your command line and type out the following.  Replace `<home>` with your own home folder's name, so for example `cd /Users/vijay/Programming` would be what I'd type:**

```
cd /Users/<home>/Programming
touch index.html
code index.html
```

We are creating a file called `index.html`.  

## Intro to HTML

HTML (Hypertext Markup Language) is a special language that you write into an HTML document identified by the `.html` extension, in which a browser like Google Chrome can open up, and then display its contents to you.  To view your HTML document in a browser, you could simply navigate to the file in whatever folder you saved it in, and double click on it, which should launch your default browser.

Many people like the HTML language because it's really easy to learn and feels just like writing normal English with a little bit of code syntax to "mark up content".  **Note:** You can write any in any speaking language you like and mark it up with HTML, so Japanese, Chinese, Russian, etc all work with HTML markup.  

For the most part, you type whatever you want to display in plain English, wrapped by HTML tags `<>` that indicate how you either want to style or draw attention to that content.

For example if I write:

```html
<em>Hello World</em>
```

#### Output

<em>Hello World</em>

This code will emphasize the words Hello World using HTML tag syntax.

Copy this code and paste it into your `index.html` file now open with Visual Studio Code.  Save the file, then navigate over to it using your Finder or Windows Explorer, and open the file with Google Chrome.  You should see Hello World in a fun, italic font.

I'm telling the browser I want to show `Hello World` on my new page, and wrap it inside a emphasis tag, indicated by an opening tag `<em>` and a closing tag `</em>`.  Anything outside of the tag will not get the special emphasis styling.  HTML is always indicated by angular brackets, so `<>` followed by `</>` is usually a HTML tag.  Inside the angular brackets you also write what kind of tag you want to make, so for example:  `<b>Some content</b>`, means bold **Some content**.

## More Examples:

Try the following as exercises, save in your index.html file with Visual Studio Code, then refresh your browser to see the new result.

```html
<p>Here is my first paragraph for my beautiful essay.  Blah blah blah...</p>
<p>Here's a second paragraph for my beautiful essay. Blah blah blah</p>
<p>Here's a third paragraph for my beautiful essay.  Did you like the separation?</p>
```

#### Output

<p>Here is my first paragraph for my beautiful essay.  Blah blah blah...</p>
<p>Here's a second paragraph for my beautiful essay. Blah blah blah</p>
<p>Here's a third paragraph for my beautiful essay.  Did you like the separation?</p>


Use `<p>` tags to make paragraphs, to indicate new paragraphs like when writing a long blog post.  


```html
<p><a href="https://google.com">This is a link to Google.com</a></p>
<p><a href="https://apple.com">This is a link to Apple.com</a></p>
<p><a href="https://facebook.com">This is a link to Facebook.com</a></p>
```

#### Output

<p><a href="https://google.com">This is a link to Google.com</a></p>
<p><a href="https://apple.com">This is a link to Apple.com</a></p>
<p><a href="https://facebook.com">This is a link to Facebook.com</a></p>

Notice first that we can have tags inside tags.  The `<p>` tag wraps the `<a>` tag (link tag).  This is a common practice.  You can have tags inside tags, often called nested tags.

Use `<a>` tags to create links to other pages.  This is probably the most useful markup feature of HTML, when compared to something real world, like a physical book.  In a physical book you can only read and use your imagination about something the author describes, but with a link, the author can actually take you there in an HTML document!  The English content we want to link is wrapped by the `<a>` tag, while an `href` property is what actually is used to augment our `<a>` tag so it can actually navigate someone to a new page when clicked on.

The `href` property is a special attribute that allows the `<a>` tag to link somewhere.  Without it, the `<a>` tag will be a useless link. To feed a URL value to the `<a>` tag, we must add it in via the syntax `href="https://url.com"`.   

You must wrap your URL in quotes `"` before and after the url ends, and you must have an equal sign before your quotes so that we can feed the `href`.  In developer terms, any time you see text wrapped in quotes `"` (double) or `'` (single), it's referred to as a **string**.   We'll talk more about strings later on, but for now if you wrap text in a double quote `"`, you must end it in a double quote `"` for it to be a valid string.  If you start a string with a single quote `'`, it must be ended with a single quote as well `'`.   **Consistency does matter.**


```html
<h1>This is our page's main heading tag.</h1>
<h2>This a secondary heading tag.</h2>
<h3>This is a sub-heading tag.</h3>
<h4>This is a smaller sub-heading tag.</h4>
<h5>This is an even smaller sub-heading tag.</h5>
<h6>This is the smallest sub-heading tag you can have</h6>
```

#### Output

<h1>This is our page's main heading tag.</h1>
<h2>This a secondary heading tag.</h2>
<h3>This is a sub-heading tag.</h3>
<h4>This is a smaller sub-heading tag.</h4>
<h5>This is an even smaller sub-heading tag.</h5>
<h6>This is the smallest sub-heading tag you can have</h6>


Heading tags are used to mark important content on your page.  Usually the `<h1>` tag is for the most important item on your page, such as a page title aka `Use this weird trick to lose fat in 5 minutes a day!`.   You can also have sub-headings and smaller sub-headings to guide the reader to more sections of your page.

```html
<h2>Things to do</h2>
<ul>
    <li>Drive to work</li>
    <li>Check emails</li>
    <li>Fix website</li>
</ul>
<h2>Favorite Drinks</h2>
<ol>
    <li>Caramel Macchiato</li>
    <li>Earl Grey Tea</li>
    <li>Cafe Latte</li>
</ol>
```

#### Output

<h2>Things to do</h2>
<ul>
    <li>Drive to work</li>
    <li>Check emails</li>
    <li>Fix website</li>
</ul>
<h2>Favorite Drinks</h2>
<ol>
    <li>Caramel Macchiato</li>
    <li>Earl Grey Tea</li>
    <li>Cafe Latte</li>
</ol>


List tags that start with `<ul>` or `<ol>` allow us to mark up our English with bullets, giving us output that looks more like a list.  Use list tags to help make things like todo lists.  The `<ul>` tag is for lists with no order, hence you just see bullets.  The `<ol>` tag is for lists with order, so you'll see numbers instead.

```html
<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Email</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Jessie</td>
            <td>jessie@rocket.com</td>
        </tr>
        <tr>
            <td>James</td>
            <td>james@rocket.com</td>
        </tr>
    </tbody>
</table>
```

#### Output

<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Email</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Jessie</td>
            <td>jessie@rocket.com</td>
        </tr>
        <tr>
            <td>James</td>
            <td>james@rocket.com</td>
        </tr>
    </tbody>
</table>

This markup is used to make a table with HTML.  This code is a little more involved, so let's break it down.  You start a table with the `<table>` opening tag and end it with the `</table>` closing tag to indicate you want a table.   Inside the table, you need a section for a row that describes each column, usually the header row which indicates rows that follow will be organized by some value.  Here we are saying we have we want to organize our data by `Name` and `Email`.  So we first create the special header with the `<head>` tag, then inside we make a new row with the `<tr>` (table row) tag, and then we create a table heading column tag `<th>` for each column we want to have.   Again, all this reads more complex than it really is. 

Next, we have the main body of the table, which is for rows and columns that follow after our special heading row.  These rows and columns are for actual data, like names and emails.  We create the body of the table by using `<tbody>` for table body, then create a new row again using `<tr>`, then a table display column `<td>` for our actual values like `Jessie` and `jessie@rocket.com` which correspond to `Name` and `Email` above.

It's a bit more work to make a table, but if you get the idea, you can make these things easy with practice.


## Now Let's Look At Self Closing Tags

A tricky feature about HTML that throws off some students of web development is that it can have tags that close themselves (meaning no content in between).  For example, here's a tag that creates a horizontal line and has no content in between.  For that reason, we end this tag with a `/>`.

```html
<hr />
```

#### Output

<hr />

Some developers will drop the `/>` and just write `<hr>` but it's important to know that this is still a self closing tag.

Here's another self-closing tag:

```html
<img src="https://images.unsplash.com/photo-1542887486-c0aeb6d2fc46?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80" width="320" height="240" />
```

#### Output

<img src="https://images.unsplash.com/photo-1542887486-c0aeb6d2fc46?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80" width="320" height="240" />

The `<img>` tag closes itself as you notice again by the `/>` ending.  The image tag is used to show an image, but to actually show an image, you have to feed it an image URL (just like we did for the link tag `<a>` earlier).  In this case you would use the `src` attribute instead of the `href` attribute.   `src` is for images, while `href` is for links.  I made this example more interesting by adding two more attributes, one for `width` and one for `height`, set in pixels on the screen -- so a width of `320` pixels by `240` pixels high.

We will explore more attributes for HTML tags, but again think of these attributes as things that augment your HTML.  Without augmentation, your content would be non-interactive.  It's this interactivity that makes using the web better for reading than reading an actual textbook.

```html
<br />
```

#### Output

<br />

A line break tag, use this when you want to split a line into two exactly.  Commonly used for formatting addresses like so:

```html
<p>My house
<br />123 Fake St
<br />Fake city, FK
<br />00000-000
</p>
```

#### Output

<p>My house
<br />123 Fake St
<br />Fake city, FK
<br />00000-000
</p>

Notice this is a paragraph `<p>` with 3 line breaks `<br />` inside.

## Your HTML is broken

Though we have been doing our examples and having fun with HTML exercises, our code we've written so far has been broken.   Technically you are supposed to write your HTML using proper HTML guidelines, much like how in English you would use proper grammar, spelling and punctuation.

You didn't have to worry about all that because your browser takes care of the HTML "spell-checking" for you.  However, as you start to make real websites using HTML, you MUST be responsible for your own HTML syntax.  Not doing so will lead your website to render incorrectly and have browsers attempt to fix the code in different ways, leading to different results when people use different browsers to see your webpage.  Not only that, if search engines like Google crawl your webpage and try to process what's on it for their database; if code is broken -- you may rank lower or not at all when it comes to finding you on the web in a Google search engine.   Hence learning proper HTML structure is very important!


## Proper HTML

All HTML documents should start with the following set of tags:

```html
<!doctype html>
```

The `doctype` tells browsers and search engines reading our webpage that the document type is in the latest version of HTML (aka HTML5).  Without this tag, some browsers may not process the content that follows as HTML, and instead render just text.  That means all your hard work in marking everything up with tags will just look ugly and not work.   So always have a doctype to tell the browsers to render your HTML page as HTML (not text).

```html
<!doctype html>
<html>
</html>
```

You should also wrap your entire HTML page inside opening and closing `<html>` tags to indicate you are working in HTML.

```html
<!doctype html>
<html>
  <head>
    <title>This is the title of my webpage</title>
  </head>
  <body>
    <p>This is my webpage</p>
  </body>
</html>
```

Just like we saw with our `<table>`, we need a `<head>` section and a `<body>` section for our HTML.  However in the case of an HTML document, anything we put in the `<head>` tag is used to describe our webpage, while anything we put in the `<body>` tag is content that actually shows up on the webpage.   The `<title>` tag doesn't actually show up on your webpage, but it does show at the top of your browser or browser tab.  To be extremely clear, put content you want people to see in the `<body>` of your HTML webpage, while whatever you put in the `<head>` is content you want to describe your webpage, e.g. to a search engine.

## Good So Far? Onwards To Next Lesson!

Take a moment now to just rework through all the examples, and double check you understand for clarity.   In the coming lessons, we will add more complexity, so if you are struggling now, be sure to take notes, possibly make flash cards and review items you weren't clear on.   All that said, with enough practice, you will get the hang of HTML, especially as you build more websites.

Your next mission is to start making more HTML documents.  Here's your homework:

**NOTE:** There's also A LOT more HTML we haven't covered, and probably won't cover for this course -- but you can always reference any HTML you don't know by looking it up on reference sites like W3Schools as well as MDN.   That said, we will be sure to properly go through any new HTML we write together, and none of the exercises we do together will use any HTML we haven't talked about beforehand.

## Homework:

- Use your command line to make another HTML page.  Call it `about.html`.  
- Find the `about.html` page in your Programming folder, and open it with Visual Studio Code.  Next, using proper HTML syntax, write a page using paragraphs, images, links, lists and headings that explains everything about you.   Open your `about.html` page in a browser like Google Chrome or Firefox to see and verify your output.
- Repeat the above exercise and make a page that is called `blog.html`.  Write a few paragraphs about yourself with titles as if it were a blog post.  
