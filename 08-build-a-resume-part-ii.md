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

