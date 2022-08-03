## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/jeffreywyman/one-click-google-form/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.
    <input type="text" placeholder="Paste your Pre-filled Link Here" id="inputId">
    <button type="button" onclick="getInputValue();">Get Value</button>
    <div id="my_field">test</div>
    <script>
      function getInputValue() {
        // Selecting the input element and get its value 
        var inputVal = document.getElementById("inputId").value;

        inputVal = inputVal.replace("viewform?", "formResponse?");

        // Displaying the value
        document.getElementById("my_field").innerText = inputVal;
      }
    </script>
### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/jeffreywyman/one-click-google-form/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
