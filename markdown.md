# Topics

## 1. Styling text

1. Bold ( ** ** [or] __ __ )
   
   **Hello** __Hello__

1. Italics (* * [or] _ _)

   *Hello* _Hello_

1. Bold and nested italic ( ** ** and _ _ )

   **This text is _extremely_ important**

1. All bold and italic ( *** *** )

   ***This is just a test***

1. Strikethrough (~~ ~~)

   ~~This is a strike~~

## 2. Quoting text

You can quote text with a >.
> HI this is a quote test

## 3. Quoting code

You can call out code or a command within a sentence with single backticks. 
The text within the backticks will not be formatted.

```
This is a test
git status
git commit -am "msg"
git statu 
```

## 4. Links

You can create an inline link by wrapping link text in brackets [ ], and then wrapping the URL in parentheses ( ). You can also use the keyboard shortcut command + k to create a link.

This site was built using [GitHub Pages](https://pages.github.com/).

* Section links
   - 
  [Custom foo description](#1-styling-text)
  
* Relative links
   - You can define relative links and image paths in your rendered files 
to help readers navigate to other files in your repository.

   -  A relative link is a link that is relative to the current file. 
For example, if you have a README file in root of your repository, 
and you have another file in docs/CONTRIBUTING.md,
the relative link to CONTRIBUTING.md in your README might look like this:

[Contribution guidelines for this project](docs/CONTRIBUTING.md)


## 5. Lists 

You can make an unordered list by preceding one or more lines of text with - or *.
- George Washington   
- John Adams   
- Thomas Jefferson

To order your list, precede each line with a number.
1. James Madison
1. James Monroe    
1. John Quincy Adams

## 6. Nested Lists
You can create a nested list by indenting one or more list items below another item.

1. First list item
   - First nested list item
      - Second nested list item
1. First list item
   - First nested list item
      - Second nested list item   



1. First item
2. Second item
3. Third item
   1. Indented item
   2. Indented item
4. Fourth item

## 7. Task lists
To create a task list, preface list items with a regular space character followed by [ ]. 
To mark a task as complete, use [x].

- [x] This is task 1
- [ ] This is task 2
- [ ] This is task 3

If a task list item description begins with a parenthesis, you'll need to escape it with \:

- [ ] \(Optional) Open a follow up issue

## 8. Mentioning people and teams

You can mention a person or team on GitHub by typing @ plus their username or team name.
This will trigger a notification and bring their attention to the conversation.
People will also receive a notification if you edit a comment to mention their username or team name. 
For more information about notifications, see "About notifications."

### code 

`this is code`

## 9. Emoji

:bowtie: 
Gone camping! :tent: Be back soon.

That is so funny! :joy:


## 10. ignore case

Let's rename \*our-new-project\* to our-old-project.

## 11. Images
Its syntax is  similar to link. You just need to add '!' before [txt](location to the image)
You can create an inline link by wrapping link text in brackets [ ], and then wrapping the URL in parentheses ( ). You can also use the keyboard shortcut command + k to create a link.

This site was built using ![someName](/home/syed/Documents/2020-12-28_17-52.png).


## 12. Horizontal Rules
To create a horizontal rule, use three or more asterisks (***), dashes (---), or underscores (___) on a line by themselves.

***
---
_________________



## 13. Escaping Backticks (`` ``)

If the word or phrase you want to denote as code includes one or more backticks, 
you can escape it by enclosing the word or phrase in double backticks (``).

``Use `code` in your Markdown file.``

\* Without the backslash, this would be a bullet in an unordered list


## 14. Task

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

## link for header in Same .md file
[link](#code-1)


## 15. Alignment
You can align text in the columns to the left, right, or center by adding a colon (:) to the left, right, or on both side of the hyphens within the header row.

| Syntax for left      | Description for center | Test Text for right  |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |


## 16. Definition Lists

Some Markdown processors allow you to create definition lists of terms and their corresponding definitions. To create a definition list, type the term on the first line. On the next line, type a colon followed by a space and the definition.

<dl>
  <dt>First Term</dt>
  <dd>This is the definition of the first term.</dd>
  <dt>Second Term</dt>
  <dd>This is one definition of the second term. </dd>
  <dd>This is another definition of the second term.</dd>
</dl>

To create a heading, add number signs (#) in front of a word or phrase. The number of number signs you use should correspond to the heading level. For example, to create a heading level three (<h3>), use three number signs (e.g., ### My Header).