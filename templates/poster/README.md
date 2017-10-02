# Latex Poster Template (from Theory in Practice)

## How to compile

To make this template, run ``make``! We've included a ``compiled_poster.pdf``, make sure your ``poster.pdf`` looks similar.

The provided ``Makefile`` is usually sufficient for a poster, but may require changes if you do fancy things.

## Navigating the template

Our poster template uses ``a0poster``, which uses a grid-based system. The downside to using a grid is that you'll have to put some thought into the shape of your poster before writing latex. The upside is that you get very tight control of where things appear. We encourage you to outline on paper the dimensions that you want, then set up the template accordingly, then start filling in content.

The template is set up to be 36 inches high by 24 inches wide (the required dimensions for the OpportunityID project):

```latex
27: \setlength\paperwidth{24in}
28: \setlength\paperheight{36in}
```

and use a border of a half-inch:

```latex
130: \TPGrid[0.5in,0.5in]{35}{23}  
```

Once you set up the size grid you want, you can define a textblock:

```latex
\begin{textblock}{11.5}(0,0)
\begin{center}
Hello world
\end{center}
\end{textblock}
```

Note that textblocks have the format ``\begin{textblock}{width}(x,y)``, where ``x`` and ``y`` determine the horizontal and vertical distance from the upper-left textblock corner to the upper-left corner of the poster, and ``width`` determines how wide this block will be.

Remember to leave space between your columns! If you have a 36x24 inch grid with 0.5 inch border, you have 35x23 to work with. If you have three columns of content (probably a bad idea!), then you'll probably also want 0.5 inch of space between them, so you only have 22.5 inches of horizontal space to allocate to the textblocks. Plan according.

## Presenting your content

### Content structure
One reasonable structure for these posters would be:

|       Title, Authors         |
|--------------|---------------|
|       Problem Statement      |
|         (with figure)        |
|--------------|---------------|
|    Definitions (as needed)   |
|--------------|---------------|
|    Related   |   Research    |
|     Work     |    Ideas      |
|--------------|---------------|

The poster should probably include some high-level visualizations of the fundamentals (e.g. what is a poset (an object that might be part of your problem statement)? what is branchwidth (or another parameter you will use)? etc.). The definitions should be as visual as possible, but sometimes you also need to explicitly state a few definitions in text.  

You might want to include motivation or applications (either in the problem statement area, or a separate part of the poster -- remember, the layout here is completely up to you - the diagram above is not in any way mandatory. Feel free to move things around!).

Note that in Related Work, it's reasonable to use a little bit smaller font for citations, and give abbreviated information about the actual works (not full length bib entries).

It should be easy to visually navigate your poster!
Use fonts, colors, and boxes wisely to help the viewer find the most important parts (the open problem should really be visually most prominent). Note that not all columns must be the same width (or rows the same height - they don't even have to line up as rows)!  

### Making the most out of latex

You should prefer using visuals over text. Remember that you will be _presenting_ your poster! Your audience will have a hard time reading and listening at the same time, but images are great to point at while you talk. If you must use text, try to format it to visually guide the audience (highlight important words, use bullet points for related concepts, etc.).

One tip for modularizing your code is to use ``\input{[otherfile.tex]}``, which directly inserts the text from another .tex file. For example, you might have file per section from your content structure. This modularization helps when working on the poster with collaborators and git.

Latex can handle ``.pdf`` images, so we encourage creating your figures in tikz or converting ``.svg`` (scaling) graphics to ``.pdf`` with Imagemagick. Once you go with scalable graphics, everything else looks terrible!

Historically, we have found that handling captions and citations by hand works better than trying to hook up standard latex machinery. At the end of the day, get something working and then clean it up, don't waste too much time wrestling with latex.
