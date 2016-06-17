---
# required metadata

title: [ARTICLE TITLE | SERVICE NAME]
description:
keywords:
author: [GITHUB USERNAME]
manager: [ALIAS]
ms.date: 04/28/2016
ms.topic: article
ms.prod:
ms.service:
ms.technology:
ms.assetid: [GET ONE FROM guidgenerator.com]

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
#ms.reviewer: [ALIAS]
#ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Metadata and Markdown Template

This docs.ms template contains examples of markdown syntax, as well as guidance on setting the metadata. To get the most of it you must view both the [raw markdown](https://raw.githubusercontent.com/Microsoft/Docs/master/template.md) and the [rendered view](https://github.com/Microsoft/Docs/blob/master/template.md) (or instance, the raw markdown shows the metadata block, while the rendered view does not).

When creating a markdown file you should copy this template to a new file, fill out the metadata as specified below, set the H1 heading above to the title of the article, and delete the content. 


## Metadata 

The full metadata block is above (in the [raw markdown](https://raw.githubusercontent.com/Microsoft/Docs/master/template.md)), divided into required fields and optional fields. Some key notes:

- You **must** have a space between the colon (:) and the value for a metadata element.
- If an optional metadata element does not have a value, comment out the element with a # (do not leave it blank or use "na"); if you are adding a value to an element that was commnted out, be sure to remove the #.
- Colons in a value (e.g., a title) break the metadata parser. In their place, use the HTML encoding of &#58; (e.g., "title: Azure Rights Management&#58; the basics | Azure RMS").
- **title**: This title will appear in search engine results. The title should end with a pipe (|) followed by the name of the service (e.g. see above). The title need not (and probably should not) be identical to the title in your H1 heading. It should be roughly 65 characters (including | SERVICE NAME)
- **author**, **manager**, **reviewer**: The author field should contain the **Github username** of the author, not their alias.  The "manager" and "reviewer" fields, on the other hand, should contain aliases. ms.reviewer specifies the name of the PM associated with the article or service.
- **ms.assetid**: This is the GUID of the article from CAPS. When creating a new markdown file, get a GUID from [https://www.guidgenerator.com](https://www.guidgenerator.com). 
- **ms.prod**, **ms.service**, **ms.technology**, **ms.devlang**, **ms.topic**, **ms.tgt_pltfrm**: Possible values for these elements can be found [here](https://microsoft.sharepoint.com/teams/STBCSI/Insights/_layouts/15/WopiFrame.aspx?sourcedoc=%7b7A321BF1-0611-4184-84DA-A0E964C435FA%7d&file=WEDCS_MasterList_CSIValues.xlsx&action=default).

## Basic Markdown, GFM, and special characters

All basic and Github-flavored markdown is supported. For more information on these, see:

- [Baseline markdown syntax](https://daringfireball.net/projects/markdown/syntax)
- [Github-flavored markdown (GFM) documentation](https://guides.github.com/features/mastering-markdown)

Markdown uses special characters such as \*, \`, and \# for formatting. If you wish to include one of these characters in your content, you must do one of two things:

- Put a backslash before the special charatcter to "escape" it (e.g., \\\* for a \*)
- Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (e.g. \&\#42\; for a &#42;).

## Headings

Examples of first- and second-level headings are above. 

There **must** be only one first-level heading in your topic, which will be displayed as the on-page title.  

Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.

### Third-level heading
#### Fourth-level heading
##### Fifth level heading
###### Sixth-level heading

## Text styling

*Italics* 

**Bold** 

~~Strikethrough~~

## Links

### Internal Links

To link to a header in the same markdown file, view the source of the published article, find the id of the head (e.g. `id="blockquote"`), and link using # + id (e.g. `#blockquote`).

- Example: [Blockquotes](#blockquote)

To link to a markdown file in the same repo, use [relative links](https://www.w3.org/TR/WD-html40-970917/htmlweb.html#h-5.1.2), including the ".md" at the end of the filename.

- Example: [Readme file](readme.md)
- Example: [Tools and setup for contributors](./ContributorGuide/tools-and-setup.md)

To link to a header in a markdown file in the same repo, use relative linking + hashtag linking.

- Example: [Permissions in Guthub](./ContributorGuide/tools-and-setup.md#permissions-in-github)

### External Links

To link to an external file, use the full URL as the link.

- Example: [Github](http://www.github.com)

If a URL appears in a markdown file, it will be transformed into a clickable link.

- Example: http://www.github.com

## Lists

### Ordered lists

1. This 
1. Is
1. An
1. Ordered
1. List  


#### Ordered list with an embedded list

1. Here
1. comes
1. an
1. embedded
    1. Miss Scarlett
    1. Professor Plum
1. ordered
1. list


### Unordered Lists

- This
- is
- a
- bulleted
- list


##### Unordered list with an embedded lists

- This 
- bulleted 
- list
    - Mrs. Peacock
    - Mr. Green
- contains  
- other
    1. Colonel Mustard
    1. Mrs. White
- lists


## Horizontal rule

---

## Tables

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| col 1 is default | left-aligned     |    $1 |


## Code

### Generic codeblock

Indent code four spaces for generic codeblock coding.

    function fancyAlert(arg) {
      if(arg) {
        $.docs({div:'#foo'})
      }
    }


### Codeblocks with language identifier

Use three backticks (&#96;&#96;&#96;) + a language ID to apply language-specific color coding to a code block.  Here is the entire list of [GitHub Flavored Markdown (GFM) language IDs](https://github.com/jmm/gfm-lang-ids/wiki/GitHub-Flavored-Markdown-(GFM)-language-IDs).

##### C&#9839;

```c#
using System;
namespace HelloWorld
{
    class Hello 
    {
        static void Main() 
        {
            Console.WriteLine("Hello World!");

            // Keep the console window open in debug mode.
            Console.WriteLine("Press any key to exit.");
            Console.ReadKey();
        }
    }
}
```
#### Python

```python
friends = ['john', 'pat', 'gary', 'michael']
for i, name in enumerate(friends):
    print "iteration {iteration} is {name}".format(iteration=i, name=name)
```
#### PowerShell

```powershell
Clear-Host
$Directory = "C:\Windows\"
$Files = Get-Childitem $Directory -recurse -Include *.log `
-ErrorAction SilentlyContinue
```

### In-line code

Use backticks (&#96;) for `in-line code`.

## Blockquotes

> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.

## Images

### Static Image

![this is the alt text](./media/AzRMS_elements.png)

### Linked Image

[![alt text for linked image](./media/AzRMS_elements.png)](https://docs.microsoft.com) 

### Animated gif

![animated gif](./media/hololens.gif)

## Alerts

### Note

> [!NOTE]
> This is NOTE

### Warning

> [!WARNING]
> This is WARNING

### Tip

> [!TIP]
> This is TIP

### Important

> [!IMPORTANT]
> This is IMPORTANT

## Videos

### Channel 9

<iframe src="http://channel9.msdn.com/Series/Azure-Active-Directory-Videos-Demos/Azure-Active-Directory-Connect-Express-Settings/player" width="960" height="540" allowFullScreen frameBorder="0"></iframe>

### Youtube

<iframe width="420" height="315" src="https://www.youtube.com/embed/R6_eWWfNB54" frameborder="0" allowfullscreen></iframe>

## docs.ms extentions

Doc.ms provides a few extentions to Github Flavored Markdown. 

###  Includes

You can embed the markdown of one file into another using an include.

[!INCLUDE[sample include file](./includes/sampleinclude.md)]

### Buttons

> [!div class="button"]
[button links](/rights-management)

### Selectors

> [!div class="op_single_selector"]
- [foo](/rights-management/template.md)
- [bar](/rights-management/scratch.md)

### Step-By-Steps

>[!div class="step-by-step"]
[Pre](https://www.example.com)
[Next](https://www.example.com)