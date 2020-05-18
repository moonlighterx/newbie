# Build The Resume (Part II) With Style

# Improving Our Resume With Design

Using the advice I gave you in the previous section on design, I've put together a styled up resume.  Let's use the HTML layout we created in Chapter 5, and use the CSS we learned in Chapter 7 to make a lovely looking resume webpage!

![alt text](resume-pretty.jpg "Pretty Resume")

## Reviewing Our Layout

```html
<html>
  <head>
    <title>My Resume</title>
  </head>
  <body>
      <h1>Resume of Vijay Menon</h1>
      <img src="images/myphoto.png" alt="Vijay's Photo" />
      <p>Phone: 000-000-0000 | Email: <a href="mailto:vmenon@email.com">vmenon@email.com</a> | <a href="https://linkedin.com">Linkedin</a></p>
      <h2>Experience</h2>
      <h2>Education</h2>
      <h2>Skills</h2>
  </body>
</html>
```

This is what we had from Chapter 5.  Let's create a new folder called `Resume` under this path:

`~/Tutorials/Chapter-08`.

Change directory then to `Resume`.

```
cd ~/Tutorials/Chapter-08/Resume
```

Make a new file called `index.html`.

```
touch index.html
```

Copy and paste the layout code from above into `index.html`.

Open the `index.html` with your browser, just to verify you can see the layout.

### Result

If all goes well, we should be able to see our bare-bones webpage.  

## Adding in CSS

Let's add in the `<style>` tag now to the HTML.  Add your style tag to the `<head>` section.  Let's make sure we can see some CSS changes by adding in a simple **"health check"** (programmer lingo) where we color our paragraphs red.

```html
<html>
  <head>
    <title>My Resume</title>
    <style>
        p {
            color: red;
        }
    </style>
  </head>
  <body>
      <h1>Resume of Vijay Menon</h1>
      <img src="images/myphoto.png" alt="Vijay's Photo" />
      <p>Phone: 000-000-0000 | Email: <a href="mailto:vmenon@email.com">vmenon@email.com</a> | <a href="https://linkedin.com">Linkedin</a></p>
      <h2>Experience</h2>
      <h2>Education</h2>
      <h2>Skills</h2>
  </body>
</html>
```

### Result

How was your **health check**? If the paragraphs are red, you should be good to go.  

## Analyzing Our Design

The first thing to notice about our design is that it's divided into sections:  

We have the main section which has a big heading, "Vijay Menon. Marketing Specialist".  After that is a smaller heading that says "Specializing in digital marketing and advertising with over 10 years experience.".   Finally there's a big button with "Contact Me" on it.   In marketing, we call this main section sometimes the "Hero" section, or the "Jumbo" section -- because it's the section we want people to pay the most attention to.  A hero section usually has a giant heading, a sub-heading, and then a call to action (usually a button or form).

Below this section, we have an Experience section, followed by an Education section, and then a Skills section.  Let's divide our page up in HTML so that it follows this organizational structure.

### Div Tags

A `<div>` is used to mark a division in the page we want some code block to fall into. 

For simplicity, I've omitted the rest of the HTML, but when viewing your page you'll need the entire HTML layout:

```html
    <div>
        <h1>Resume of Vijay Menon</h1>
        <img src="images/myphoto.png" alt="Vijay's Photo" />
        <p>Phone: 000-000-0000 | Email: <a href="mailto:vmenon@email.com">vmenon@email.com</a> | <a href="https://linkedin.com">Linkedin</a></p>
    </div>
    <div>
        <h2>Experience</h2>
    </div>
    <div>
        <h2>Education</h2>
    </div>
    <div>
        <h2>Skills</h2>
    </div>
```

If we were to save this code (make sure you only change this affected part in your `<body>` and don't delete the rest of your HTML), we see that design wise, nothing has really changed.  The page looks exactly the same.

### ids

However, by using `<div>` tags, it's a little easier to see what code blocks go to what divs.  We can even make these divisions more helpful by giving them each an `id` attribute with a value that can tell us what each division is meant for.

For example:

```html
    <div id="hero">
        <h1>Resume of Vijay Menon</h1>
        <img src="images/myphoto.png" alt="Vijay's Photo" />
        <p>Phone: 000-000-0000 | Email: <a href="mailto:vmenon@email.com">vmenon@email.com</a> | <a href="https://linkedin.com">Linkedin</a></p>
    </div>
    <div id="experience">
        <h2>Experience</h2>
    </div>
    <div id="education">
        <h2>Education</h2>
    </div>
    <div id="skills">
        <h2>Skills</h2>
    </div>
```

If we save our code now, and view our webpage, we notice that still nothing changed.  However, now our code is more meaningful to us the developer, as we know by using divisions what code is supposed to go in what `<div>` block.   For example any code about my skills should go under the `<div id="skills>`.   It would not make sense to put education related material there.

### Section Tags

Taking it one step further, we can use the `<section>` tag.  `<div>` tags are a bit generic and don't really describe that any content inside belongs to a section.

```html
    <section id="hero">
        <h1>Resume of Vijay Menon</h1>
        <img src="images/myphoto.png" alt="Vijay's Photo" />
        <p>Phone: 000-000-0000 | Email: <a href="mailto:vmenon@email.com">vmenon@email.com</a> | <a href="https://linkedin.com">Linkedin</a></p>
    </section>
    <section id="experience">
        <h2>Experience</h2>
    </section>
    <section id="education">
        <h2>Education</h2>
    </section>
    <section id="skills">
        <h2>Skills</h2>
    </section>
```

**Note** You don't need to use the `<section>` tag, however it is more meaningful to someone because earlier we talked about dividing our page into sections, not divisions.

### More Semantic Tags

#### Header

When talking about sections of a page, sometimes you want to be very specific.  The `hero` section is also a bit like a header for our page.  We can replace section with `<header>` instead.  Perhaps we might want to reuse this code again someday, so it would be nice to have all our header code in a simple `<header>` tag.

```html
    <header id="hero">
        <h1>Resume of Vijay Menon</h1>
        <img src="images/myphoto.png" alt="Vijay's Photo" />
        <p>Phone: 000-000-0000 | Email: <a href="mailto:vmenon@email.com">vmenon@email.com</a> | <a href="https://linkedin.com">Linkedin</a></p>
    </header>
    <section id="experience">
        <h2>Experience</h2>
    </section>
    <section id="education">
        <h2>Education</h2>
    </section>
    <section id="skills">
        <h2>Skills</h2>
    </section>
```


### Footer

You can also use the `<footer>` tag if you think some part of your page will always be at the bottom (and could be reused througout other pages).  Typically, copyright and site map information go in the footer.  Go ahead and add the `<footer>` tag to your HTML (and be sure to do it before the closing `<body>` tag). 

```html
    <header id="hero">
        <h1>Resume of Vijay Menon</h1>
        <img src="images/myphoto.png" alt="Vijay's Photo" />
        <p>Phone: 000-000-0000 | Email: <a href="mailto:vmenon@email.com">vmenon@email.com</a> | <a href="https://linkedin.com">Linkedin</a></p>
    </header>
    <section id="experience">
        <h2>Experience</h2>
    </section>
    <section id="education">
        <h2>Education</h2>
    </section>
    <section id="skills">
        <h2>Skills</h2>
    </section>
    <footer>
        Copyright 2020 Vijay Menon
    </footer>
```

There are more tags, which we will visit shortly, but now let's turn our attention to CSS.

## Styling

Let's look at our `<style>` tag section now (again isolated for your reading convenience).

```html
    <style>
        p {
            color: red;
        }
    </style>
```

In looking at our design, we see that our sections have different background colors.  For example, our Experience section is gray, while our Education and Hero section are white, and our Skills section and footer are blue.

Let's add to our CSS rule sets for our different sections so they get the right background color.   To set a background color, use the `background` property.

```html
    <style>
        p {
            color: red;
        }
        header {
            background: white;
        }
        section#experience {
            background: #cccccc;
        }
        section#education {
            background: #fff;
        }
        section#skills {
            background: #006AAE;
        }
        footer {
            background: #006AAE;
        }
    </style>
```

Save your page and check the result.  

### What's the # sign?

Remember the `id` we created earlier for each section of our page?  The `#` sign in CSS means `id`.  

CSS is all about being specific.  If you just write `section` by itself, how will CSS know which section to target with your ruleset?  We use ids as one way to help us be more specific about where want our rules to be applied.

So by saying `section#experience`, any rules defined in that CSS block will be applied to any HTML sections with an id of `experience`.

Typically ids are only used once on a webpage.  You only have one education section, so it makes sense to mark that HTML with an id.

### Okay but what about the # sign after `background`?

When you see a `#` sign followed by six numbers and letters (or three numbers and letters), this is what's known as **Hex code**.  Hex, or hexadecimal code is a short-hand way of writing out a color.  Since most computers now support over 16 million colors, we need a simple way of telling our computer which color we want specifically.   Hex is that simple way of doing so.

You don't need to memorize hex code, for the most part when you pick a color in your favorite design tool, you can have it give you the hex code for it as well in the color properties area.  That hex code can then be pasted in the place of a simple color like `blue` or `black`. 

CSS supports basic colors like `red`, `green`, `black`, and so on which we were able to just type after a property like `color` or `background`.  But using hex allows you to be more specific than a basic color.   

The good news is you can get even more specific about your color combinations, but we'll save all that for later.  

## Getting More Detailed

Okay so far so good, we've now got our page organized pretty neatly and it's got some color.  But now some of our page is not easy to read and needs better styling.  

Let's work more closely on the `<header>` area and get more specific about everything related to that section.

The first thing we need to fix is our `<h1>` tag.  The design has it looking `color` blue (hex code: #006AAE), as well as having a `font-size` of about 48 pixels, (or `48px` when written in CSS as a rule).  Let's code those rules up in our CSS:

Again, I'm omitting the rest of the code for clarit (but it's still there in the final output):

```html
 <style>
    header {
        background: white;
    }
    header h1 {
        color: #006AAE;
        font-size: 48px;
    }
</style>
```

If you save your webpage now, you should see the `<h1>` tag nice and big with a blue color.  

Take a look at the syntax we wrote.  It's more specific -- which is a recurring theme with CSS.  By writing `header h1`, we are saying we want to target all `h1` tags inside our `header` and give them a color of `#006AAE` along with a `font-size: 48px;`.

The space between `header` and `h1` **IS IMPORTANT**.  Whereas indentation and spacing don't really matter between rulesets, any time you are targeting a new section or element, spaces **DO matter**.

When you say `header h1`, it's really saying any `h1` inside any `header`.  

### Parent Child Relationships

Anytime we want to reach an element inside another element with CSS, we use the space to separate a **parent** element from a **child** element.  In the previous example, the `header` was the parent element for the `h1` element.  

Let's say we wanted to target all `<a>` tags inside paragraph tags `<p>` inside `<header>` tags.  Add this code to your style tag below the other rules, then refresh your webpage to see the result:

```css
header p a {
    color: black;
}
```

You should now see that the links are black (not blue anymore).   We'll come back to more ways you can be specific about parent and child elements (and even grandchild elements), but for now let's carry onward with styling. 

This section is already quite large, so we'll continue on in the next section.

## Review

- Use `<div>` tags to organize HTML content in meaningful ways
- You can use semantic tags like `<section>`, `<header>` and `<footer>` given `<div>` tags are more generic (and in this way you can be more specific)
- Use the `id` attribute in HTML to help label and be even more specific about a section of code.
- Use the `#` sign in CSS with a rule to target any `id` in your HTML
- Use the `#` sign with any hex color value to indicate a specific color
- Space matters when targeting children elements.  `header p a` means any `a` tags inside any `p` tags inside any `header` tags.  
- CSS is very specific.  The more specific you are with your rulesets, the more you can control the look and feel of your webpage.

## Homework

Go ahead and create the following folder `homework` under this path:

`~/Chapter-08/Resume/homework`

Next, make a simple `index.html`, then copy and paste our code from our `index.html` in the `Resume` folder to this new `index.html` inside `homework`.  

For this assignment, your goal is to fix the colors of the other sections so they don't contrast sharply with the page.  For example, the Skills section text is black.  It might look better if the text were white.   The header paragraph text is red still and the links are black.  Let's make them the same color, black, then for extra credit, see if you can remove the underline property under the links.   (You'll have to be resourceful and look up how to do this via a search engine).