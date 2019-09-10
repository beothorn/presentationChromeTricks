# Chrometricks

## Introduction

Today I want to show a bunch of tricks you can use to get more control over the websites you visit or develop.

With a bit knowledge about javascript and the help from chrome dev tools you can change how websites render for you, get more information from them and even add functionalities to them.

The tricks I am going to show are really basic, and there are many other ways to achieve the same result without using dev tools. But doing them inside chrome gives you the fast feedback of only using one tool.

## JS + CHROME

Much of what I am going to show is not a feature of dev tools but is more related to javascript.

I am also leaving out a lot of features. What I want is that at the end of this presentation you have seen at least one new trick that enables you to change a website to be more usefull to you.

## Dev tools

I believe everyone is familiar with this part. To open dev tools we use F12 or CTRL+SHIFT+C to inspect an element.

But first let's make ourselves comfortable. Using CTRL+SHIFT+P you can list all commands availables on all menus on dev tools.

Lets first switch to a dark theme.
__Select Switch to dark theme__
And then we have the panels that show up depending on context. For example on the elements tab it shows the styles, event listeners, etc. I prefer them as a horizontal panel so
__Select Use horizontal panel layout__


## Annoying popup / Playng around design

Now the first trick. Sometimes you enter a website and you have some annoying popups, or even some footer hiding a good part of the screen for no good reason. Sometimes you can't even close it.

There is a nice shortcut to hide items, if you select the element using CTRL+SHIFT+C and press H you can show or hide any element.

Another thing we sometimes want to do is see how things would look like if you move some elements around and change some contents.

If you inspect an element you can drag and drop inside the elements view. You can also edit the html code, but that is kind of cumbersome because you need to select the element you want to edit and select the option to change the html.

A neat trick, that is not so much a chrome thing but a javascript thing, is to select a component that is parent to the elements you want to change, put it on a global variable and then make it editable.

__Execute code on slide__

After that, you can use CTRL+SHIFT+P to find the option to take a screenshot from an area or for the whole page, including stuff that you need to scroll to see.

## EXECUTING CODE

With dev tools you also get a console where you can execute javascript. The console can also render other things beside text.

console.table renders a table

console.log with %c allows you to style the output

copy copies the parameter to your clipboard, if it is a JSON it prettyfies it, really handy

the console is wrapped on an async context, so you are free to use await

## Console limitations

But the console has its limitations. It is hard to edit multiline commands with it. You can mistakenly press up and move in the command execution history while editing the command.

Also, although the command history is kept between sessions, it is not easy to search for a specific command.

As an alternative we can use snippets.

__Opens Sources tab > Snippets__

Snippets are available across all websites. They execute in the context of the page. They are not wrapped inside an async function.

## Take control with overrides!

This a powerful tool for your day to day use of the web. With overrides you can persist changes you do on the sources of any website.

First you need to open Sources > Overrides and select the folder where the changes will be saved. 

Allow devtools to access your filesystem. Now everything you change will be persisted and loaded when you reopen this same website.

We can change the font color for example.

__Change font color and reload the page__

We can change the html.

__Change HTML on Source tab > Page and reload the page__
__Show the icon changed__

We can change the javascript.

__Add console log and reload__
__Show right click > Local modifications and undo with undo icon on bottom__

But, it only works with dev tools open.

## With extensions the sky is the limit

## That looks like this

If you want a solution that executes code seemingly everytime without having to open devtools the best option is an extension.

I will not go into length about extensions. Basically you can do anything with them, intercept requests, manipulate a website, run stuff on background, ignore CORS restrictions and so on.

I will instead just show how to inject javascript on any website, which is enough for day to day uses.

## Demo time

__Show our helper extension__
