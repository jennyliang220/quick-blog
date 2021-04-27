# 这是一个大标题

## WEB ACCESSIBILITY COMMUNITY GROUP
<section class="box" id="submit-form">
  <h2 class="footnote">
    Submit a talk proposal {{title}}
  </h2>
  <label for="speaker-name">Your name:</label>
  <input id="speaker-name" placeholder="Your name" maxlength="64">
  <br>

  <label for="speaker-bio">Your bio:</label>
  <input id="speaker-bio" placeholder="Your related experience or expertise" maxlength="64">
  <br>

  <label for="talk-title">Talk title:</label>
  <input id="talk-title" placeholder="Your talk title" maxlength="64">
  <br>

  <label for="talk-abstract">Talk abstract:</label>
  <textarea id="talk-abstract" placeholder="Summarize in a single paragraph the major aspects of the proposal you want to present." rows="3" maxlength="512"></textarea>
  <br>
  <br>

  <button id="submit-button">Submit</button>
  <br>
  <small>(Submit opens a prepopulated mail compose window. You may customize your submission at this point before sending it.)</small>
</section>
<script>
  (() => {
    const button = document.querySelector('#submit-button');
    if (button) addSubmitButtonListener();

    function addSubmitButtonListener() {
        document.querySelector('#submit-button').onclick = () => {
            const name = document.querySelector('#speaker-name').value;
            const bio = document.querySelector('#speaker-bio').value;
            const title = document.querySelector('#talk-title').value;
            const abstract = document.querySelector('#talk-abstract').value;

            const subject = `[workshop proposal] ${title}`;
            const body = `Hi Program Committee,

I would like to submit a talk proposal for the W3C Beihang Event.


Name: ${name}

Bio: ${bio}

Talk title: ${title}

Talk abstract: ${abstract}


Best regards,\n${name}`;
          window.open(`mailto:team-beihang-events@w3.org?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`);
        };
    }
})();
</script>
### Markdown

这里可以使用简单的 Markdown。Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

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

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/jennyliang220/quick-blog/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
