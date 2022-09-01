
# Learn Accessibility by Building a Quiz, Completed

> - Accessibility is making your webpage easy for all people to use – even people with disabilities.
> - In this course, you'll build a quiz webpage. You'll learn accessibility tools such as keyboard shortcuts, ARIA attributes, and design best practices.
---

> **Step 1** <br>
Welcome to the first part of the Accessibility Quiz. As you are becoming a seasoned HTML and CSS developer, we have started you off with the basic boilerplate.<br>
Start this accessibility journey by providing a `lang` attribute to your `html` element. This will assist screen readers in identifying the language of the page.

```html
#index.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>

  </body>
</html>
```
> **Step 2** <br>
You may be familiar with the `meta` element already; it is used to specify information about the page, such as the title, description, keywords, and author.<br>
Give your page a `meta` element with an appropriate `charset` value.<br>
The `charset` attribute specifies the character encoding of the page, and, nowadays, `UTF-8` is the only encoding supported by most browsers.

```html
#index.html
  <head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="styles.css" />
  </head>
```
> **Step 3** <br>
Continuing with the `meta` elements, a `viewport` definition tells the browser how to render the page. Including one betters visual accessibility on mobile, and improves SEO (search engine optimization).<br>
Add a `viewport` definition with a `content` attribute detailing the `width` and `initial-scale` of the page.

```html
#index.html
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css" />
  </head>
```
> **Step 4** <br>
Another important `meta` element for accessibility and SEO is the `description` definition. The value of the `content` attribute is used by search engines to provide a description of your page.<br>
Add a `meta` element with the `name` attribute set to `description`, and give it a useful `content` attribute.

```html
#index.html
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="freeCodeCamp Accessibility Quiz practice project" />
    <link rel="stylesheet" href="styles.css" />
  </head>
```
> **Step 5** <br>
Lastly in the `head`, the `title` element is useful for screen readers to understand the content of a page. Furthermore, it is an important part of *SEO*.<br>
Give your page a `title` that is descriptive and concise.

```html
#index.html
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="freeCodeCamp Accessibility Quiz practice project" />
    <title>Accessibility Quiz</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
```
> **Step 6** <br>
Navigation is a core part of accessibility, and screen readers rely on you to provide the structure of your page. This is accomplished with semantic HTML elements.<br>
Add a `header` and a `main` element to your page.<br>
The `header` element will be used to introduce the page, as well as provide a navigation menu.<br>
The `main` element will contain the core content of your page.

```html
#index.html
  <body>
    <header></header>
    <main></main>
  </body>
```
> **Step 7** <br>
Within the `header`, provide context about the page by nesting one `img`, `h1`, and `nav` element.<br>
The `img` should point to `https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg`, and have an `id` of `logo`.<br>
The `h1` should contain the text `HTML/CSS Quiz`.

```html
#index.html
    <header>
      <img src="https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg" id="logo">
      <h1>HTML/CSS Quiz</h1>
      <nav></nav>
    </header>
```
> **Step 8** <br>
A useful property of an SVG (scalable vector graphics) is that it contains a `path` attribute which allows the image to be scaled without affecting the resolution of the resultant image.<br>
Currently, the `img` is assuming it's default size, which is too large. Correctly, scale the image using it's `id` as a selector, and setting the `width` to `max(100px, 18vw)`.

```css
#styles.css
#logo {
	width: max(100px, 18vw);
}
```
> **Step 9** <br>
As described in the [freeCodeCamp Style Guide](https://design-style-guide.freecodecamp.org/), the logo should retain an aspect ratio of `35 / 4`, and have padding around the text.<br>
First, change the `background-color` to `#0a0a23` so you can see the logo. Then, use the `aspect-ratio` property to set the desired aspect ratio to `35 / 4`. Finally, add a `padding` of `0.4rem` all around.

```css
#styles.css
#logo {
  width: max(100px, 18vw);
	background-color: #0a0a23;
	aspect-ratio: 35 / 4;
	padding: 0.4rem;
}
```
> **Step 10** <br>
Make the `header` take up the full width of its parent container, set it's `height` to `50px`, and set the `background-color` to `#1b1b32`. Then, set the `display` to use *Flexbox*.

```css
#styles.css
header {
	width: 100%;
	height: 50px;
	background-color: #1b1b32;
	display: flex;
}
```
> **Step 11** <br>
Change the `h1` font color to `#f1be32`, and set the font size to `min(5vw, 1.2em)`.

```css
#styles.css
h1 {
	color: #f1be32;
	font-size: min(5vw, 1.2em);
}
```
> **Step 12** <br>
To enable navigation on the page, add an unordered list with the following three list items:<br>
> - `INFO`
> - `HTML`
> - `CSS` <br>
> 
> The list items text should be wrapped in anchor tags.

```html
#index.html
      <nav>
        <ul>
          <li><a>INFO</a></li>
          <li><a>HTML</a></li>
          <li><a>CSS</a></li>
        </ul>
      </nav>
```
> **Step 13** <br>
Target unordered list elements within `nav` elements, and use *Flexbox* to evenly space the children.

```css
#styles.css
nav > ul {
	display: flex;
	justify-content: space-evenly;
}
```
> **Step 14** <br>
You can semantically separate the content within the form using `section` elements.<br>
Within the `main` element, create a form with three nested `section` elements. Then, make the form submit to `https://freecodecamp.org/practice-project/accessibility-quiz`, using the correct method.

```html
#index.html
    <main>
      <form method="post" action="https://freecodecamp.org/practice-project/accessibility-quiz">
        <section></section>
        <section></section>
        <section></section>
      </form>
    </main>
```
> **Step 15** <br>
To increase the page accessibility, the `role` attribute can be used to indicate the purpose behind an element on the page to assistive technologies. The `role` attribute is a part of the *Web Accessibility Initiative* (WAI), and accepts preset values.<br>
Give each of the `section` elements the `region` role.

```html
#index.html
      <form method="post" action="https://freecodecamp.org/practice-project/accessibility-quiz">
        <section role="region"></section>
        <section role="region"></section>
        <section role="region"></section>
      </form>
```
> **Step 16** <br>
Every `region` role requires a visible label, which should be referenced by the `aria-labelledby` attribute.<br>
To the `section` elements, give the following `aria-labelledby` attributes:
> - `student-info`
> - `html-questions`
> - `css-questions`
> 
> Then, within each `section` element, nest one `h2` element with an `id` matching the corresponding `aria-labelledby` attribute. Give each `h2` suitable text content.

```html
#index.html
      <form method="post" action="https://freecodecamp.org/practice-project/accessibility-quiz">
        <section role="region" aria-labelledby="student-info">
          <h2 id="student-info">Student Info</h2>
        </section>
        <section role="region" aria-labelledby="html-questions">
          <h2 id="html-questions">HTML Questions</h2>
        </section>
        <section role="region" aria-labelledby="css-questions">
          <h2 id="css-questions">CSS Questions</h2>
        </section>
      </form>
```
> **Step 17** <br>
Typeface plays an important role in the accessibility of a page. Some fonts are easier to read than others, and this is especially true on low-resolution screens.<br>
Change the font for both the `h1` and `h2` elements to `Verdana`, and use another web-safe font in the sans-serif family as a fallback.<br>
Also, add a `border-bottom` of `4px solid #dfdfe2` to `h2` elements to make the sections distinct.

```css
#styles.css
h1, h2 {
	font-family: Verdana, sans-serif;
}

h2 {
	border-bottom: 4px solid #dfdfe2;
}
```
> **Step 18** <br>
To be able to navigate within the page, give each anchor element an `href` corresponding to the `id` of the `h2` elements.

```html
#index.html
        <ul>
          <li><a href="#student-info">INFO</a></li>
          <li><a href="#html-questions">HTML</a></li>
          <li><a href="#css-questions">CSS</a></li>
		</ul>
```
> **Step 19** <br>
Filling out the content of the quiz, below `#student-info`, add three `div` elements with a `class` of `info`.<br>
Then, within each `div` nest one `label` element, and one `input` element.

```html
#index.html
        <section role="region" aria-labelledby="student-info">
          <h2 id="student-info">Student Info</h2>
          <div class="info">
            <label></label>
            <input />
          </div>
          <div class="info">
            <label></label>
            <input />
          </div>
          <div class="info">
            <label></label>
            <input />
          </div>
        </section>
```
> **Step 20** <br>
It is important to link each `input` to the corresponding `label` element. This provides assistive technology users with a visual reference to the input.<br>
This is done by giving the `label` a `for` attribute, which contains the `id` of the `input`.<br>
This section will take a student's name, email address, and date of birth. Give the `label` elements appropriate `for` attributes, as well as text content. Then, link the `input` elements to the corresponding `label` elements.

```html
#index.html
        <section role="region" aria-labelledby="student-info">
          <h2 id="student-info">Student Info</h2>
          <div class="info">
            <label for="student-name">Name:</label>
            <input id="student-name" />
          </div>
          <div class="info">
            <label for="student-email">Email:</label>
            <input id="student-email" />
          </div>
          <div class="info">
            <label for="birth-date">D.O.B.:</label>
            <input id="birth-date" />
          </div>
        </section>
```
> **Step 21** <br>
Keeping in mind best-practices for form inputs, give each `input` an appropriate `type` and `name` attribute. Then, give the first `input` a `placeholder` attribute.

```html
#index.html
        <section role="region" aria-labelledby="student-info">
          <h2 id="student-info">Student Info</h2>
          <div class="info">
            <label for="student-name">Name:</label>
            <input type="text" name="student-name" id="student-name" placeholder="e.g. Quincy Larson" />
          </div>
          <div class="info">
            <label for="student-email">Email:</label>
            <input type="email" name="student-email" id="student-email" />
          </div>
          <div class="info">
            <label for="birth-date">D.O.B.:</label>
            <input type="date" name="birth-date" id="birth-date" />
          </div>
        </section>
```
> **Step 22** <br>
Even though you added a `placeholder` to the first `input` element in the previous lesson, this is actually not a best-practice for accessibility; too often, users confuse the placeholder text with an actual input value - they think there is already a value in the input.<br>
Remove the placeholder text from the first `input` element, relying on the `label` being the best-practice.

```html
#index.html
          <div class="info">
            <label for="student-name">Name:</label>
            <input type="text" name="student-name" id="student-name" />
          </div>
```
> **Step 23** <br>
Arguably, `D.O.B.` is not descriptive enough. This is especially true for visually impaired users. One way to get around such an issue, without having to add visible text to the label, is to add text only a screen reader can read.<br>
Append a `span` element with a class of `sr-only` to the current text content of the third `label` element.

```html
#index.html
          <div class="info">
            <label for="birth-date">D.O.B.<span class="sr-only"></span></label>
            <input type="date" name="birth-date" id="birth-date" />
          </div>
```
> **Step 24** <br>
Within the `span` element, add the text `(Date of Birth)`.

```html
#index.html
          <div class="info">
            <label for="birth-date">D.O.B.<span class="sr-only">(Date of Birth)</span></label>
            <input type="date" name="birth-date" id="birth-date" />
          </div>
```
> **Step 25** <br>
The `.sr-only` text is still visible. There is a common pattern to visually hide text for only screen readers to read.<br><br>
This pattern is to set the following CSS properties:
> ```css
> position: absolute;
> width: 1px;
> height: 1px;
> padding: 0;
> margin: -1px;
> overflow: hidden;
> clip: rect(0, 0, 0, 0);
> white-space: nowrap;
> border: 0;
> ```
> 
> Use the above to define the `sr-only` class. 

```css
#styles.css
.sr-only {
	position: absolute;
	width: 1px;
	height: 1px;
	padding: 0;
	margin: -1px;
	overflow: hidden;
	clip: rect(0, 0, 0, 0);
	white-space: nowrap;
	border: 0;
}
```
> **Step 26** <br>
Within the second `section` element, add two `div` elements with a class of `question-block.`<br>
Then, within each `div.question-block` element, add one `p` element with text of incrementing numbers, starting at `1`, and one `fieldset` element with a class of `question`.

```html
#index.html
        <section role="region" aria-labelledby="html-questions">
          <h2 id="html-questions">HTML</h2>
          <div class="question-block">
            <p>1</p>
            <fieldset class="question"></fieldset>
          </div>
          <div class="question-block">
            <p>2</p>
            <fieldset class="question"></fieldset>
          </div>
        </section>
```
> **Step 27** <br>
Each `fieldset` will contain a true/false question.<br>
Within each `fieldset`, nest one `legend` element, and one `ul` element with two options.

```html
#index.html
        <section role="region" aria-labelledby="html-questions">
          <h2 id="html-questions">HTML</h2>
          <div class="question-block">
            <p>1</p>
            <fieldset class="question">
              <legend></legend>
              <ul>
                <li></li>
                <li></li>
              </ul>
            </fieldset>
          </div>
          <div class="question-block">
            <p>2</p>
            <fieldset class="question">
              <legend></legend>
              <ul>
                <li></li>
                <li></li>
              </ul>
            </fieldset>
          </div>
        </section>
```
> **Step 28** <br>
Give each `fieldset` an adequate `name` attribute. Then, give both unordered lists a `class` of `answers-list`.<br>
Finally, use the `legend` to caption the content of the `fieldset` by placing a true/false question as the text content.

```html
#index.html
        <section role="region" aria-labelledby="html-questions">
          <h2 id="html-questions">HTML</h2>
          <div class="question-block">
            <p>1</p>
            <fieldset class="question" name="html-question-one">
              <legend>
                The legend element represents a caption for the content of its
                parent fieldset element
              </legend>
              <ul class="answers-list">
                <li></li>
                <li></li>
              </ul>
            </fieldset>
          </div>
          <div class="question-block">
            <p>2</p>
            <fieldset class="question" name="html-question-two">
              <legend>
                A label element nesting an input element is required to have a
                for attribute with the same value as the input's id
              </legend>
              <ul class="answers-list">
                <li></li>
                <li></li>
              </ul>
            </fieldset>
          </div>
        </section>
```
> **Step 29** <br>
To provide the functionality of the true/false questions, we need a set of inputs which do not allow both to be selected at the same time.<br>
Within each list element, nest one `label` element, and within each `label` element, nest one `input` element with the appropriate `type`.

```html
#index.html
              <ul class="answers-list">
                <li>
                  <label>
                    <input type="radio" />
                  </label>
                </li>
                <li>
                  <label>
                    <input type="radio" />
                  </label>
                </li>
              </ul>
            </fieldset>
          </div>
          <div class="question-block">
            <p>2</p>
            <fieldset class="question" name="html-question-two">
              <legend>
                A label element nesting an input element is required to have a
                for attribute with the same value as the input's id
              </legend>
              <ul class="answers-list">
                <li>
                  <label>
                    <input type="radio" />
                  </label>
                </li>
                <li>
                  <label>
                    <input type="radio" />
                  </label>
                </li>
              </ul>
```
> **Step 30** <br>
Although not required for `label` elements with a nested `input`, it is still best-practice to explicitly link a `label` with its corresponding `input` element.<br>
Link the `label` elements with their corresponding `input` elements.

```html
#index.html
              <ul class="answers-list">
                <li>
                  <label for="q1-a1">
                    <input type="radio" id="q1-a1" />
                  </label>
                </li>
                <li>
                  <label for="q1-a2">
                    <input type="radio" id="q1-a2" />
                  </label>
                </li>
              </ul>
            </fieldset>
          </div>
          <div class="question-block">
            <p>2</p>
            <fieldset class="question" name="html-question-two">
              <legend>
                A label element nesting an input element is required to have a
                for attribute with the same value as the input's id
              </legend>
              <ul class="answers-list">
                <li>
                  <label for="q2-a1">
                    <input type="radio" id="q2-a1" />
                  </label>
                </li>
                <li>
                  <label for="q2-a2">
                    <input type="radio" id="q2-a2" />
                  </label>
                </li>
              </ul>
```

> **Step 31** <br>
Give the `label` elements text such that the `input` comes before the text. Then, give the `input` elements a `value` matching the text.<br>
The text should either be `True` or `False`.

```html
#index.html
              <ul class="answers-list">
                <li>
                  <label for="q1-a1">
                    <input type="radio" id="q1-a1" value="true" />
                    True
                  </label>
                </li>
                <li>
                  <label for="q1-a2">
                    <input type="radio" id="q1-a2" value="false" />
                    False
                  </label>
                </li>
              </ul>
            </fieldset>
          </div>
          <div class="question-block">
            <p>2</p>
            <fieldset class="question" name="html-question-two">
              <legend>
                A label element nesting an input element is required to have a
                for attribute with the same value as the input's id
              </legend>
              <ul class="answers-list">
                <li>
                  <label for="q2-a1">
                    <input type="radio" id="q2-a1" value="true" />
                    True
                  </label>
                </li>
                <li>
                  <label for="q2-a2">
                    <input type="radio" id="q2-a2" value="false" />
                    False
                  </label>
                </li>
              </ul>
```
> **Step 32** <br>
If you click on the radio inputs, you might notice both inputs within the same true/false fieldset can be selected at the same time.<br>
Group the relevant inputs together such that only one input from a pair can be selected at a time.

```html
#index.html
              <ul class="answers-list">
                <li>
                  <label for="q1-a1">
                    <input type="radio" id="q1-a1" name="q1" value="true" />
                    True
                  </label>
                </li>
                <li>
                  <label for="q1-a2">
                    <input type="radio" id="q1-a2" name="q1" value="false" />
                    False
                  </label>
                </li>
              </ul>
            </fieldset>
          </div>
          <div class="question-block">
            <p>2</p>
            <fieldset class="question" name="html-question-two">
              <legend>
                A label element nesting an input element is required to have a
                for attribute with the same value as the input's id
              </legend>
              <ul class="answers-list">
                <li>
                  <label for="q2-a1">
                    <input type="radio" id="q2-a1" name="q2" value="true" />
                    True
                  </label>
                </li>
                <li>
                  <label for="q2-a2">
                    <input type="radio" id="q2-a2" name="q2" value="false" />
                    False
                  </label>
                </li>
              </ul>
```
> **Step 33** <br>
To prevent unnecessary repetition, target the `before` pseudo-element of the `p` element, and give it a `content` property of `"Question #"`.

```css
#styles.css
p::before {
	content: "Question #";
}
```
> **Step 34** <br>
The final section of this quiz will contain a dropdown, and a text box.<br>
Begin by nesting a `div` with a `class` of `formrow`, and nest four `div` elements inside of it, alternating their `class` attributes with `question-block` and `answer`.

```html
#index.html
        <section role="region" aria-labelledby="css-questions">
          <h2 id="css-questions">CSS</h2>
          <div class="formrow">
            <div class="question-block"></div>
            <div class="answer"></div>
            <div class="question-block"></div>
            <div class="answer"></div>
          </div>
        </section>
```
> **Step 35** <br>
Within the `div.question-block` elements, nest one `label` element, and give the `label` elements text content

```html
#index.html
        <section role="region" aria-labelledby="css-questions">
          <h2 id="css-questions">CSS</h2>
          <div class="formrow">
            <div class="question-block">
              <label>Are you a frontend developer?</label>
            </div>
            <div class="answer">
            </div>
            <div class="question-block">
              <label>Do you have any questions:</label>
            </div>
            <div class="answer">
            </div>
          </div>
        </section>
```
> **Step 36** <br>
Within the first `div.answer` element, nest one required `select` element with three `option` elements.<br>
Give the first `option` element a `value` of `""`, and the text `Select an option`. Give the second `option` element a `value` of `yes`, and the text `Yes`. Give the third `option` element a `value` of `no`, and the text `No`.

```html
#index.html
            <div class="answer">
              <select required>
                <option value="">Select an option</option>
                <option value="yes">Yes</option>
                <option value="no">No</option>
              </select>
            </div>
```
> **Step 37** <br>
Link the first `label` element to the `select` element, and give the `select` element a `name` attribute.

```html
#index.html
            <div class="question-block">
              <label>Do you have any questions:</label>
            </div>
            <div class="answer">
              <select name="customer" id="customer" required>
                <option value="">Select an option</option>
                <option value="yes">Yes</option>
                <option value="no">No</option>
              </select>
            </div>
```
> **Step 38** <br>
Nest one `textarea` element within the second `div.answer` element, and set the number of rows and columns it has.<br>
Then, give the `textarea` placeholder text describing an example answer.

```html
#index.html
            <div class="answer">
              <textarea rows="5" cols="24" placeholder="Who is flexbox..."></textarea>
            </div>
```
> **Step 39** <br>
As with the other `input` and `label` elements, link the `textarea` to its corresponding `label` element, and give it a `name` attribute.

```html
#index.html
            <div class="question-block">
              <label for="css-questions">Do you have any questions:</label>
            </div>
            <div class="answer">
              <textarea id="css-questions" name="css-questions" rows="5" cols="24" placeholder="Who is flexbox..."></textarea>
            </div>
```
> **Step 40** <br>
Do not forget to give your `form` a submit button.

```html
#index.html
      <form method="post" action="https://freecodecamp.org/practice-project/accessibility-quiz">
        <section role="region" aria-labelledby="student-info">
          <h2 id="student-info">Student Info</h2>
          <div class="info">
            <label for="student-name">Name:</label>
            <input type="text" name="student-name" id="student-name" />
          </div>
          <div class="info">
            <label for="student-email">Email:</label>
            <input type="email" name="student-email" id="student-email" />
          </div>
          <div class="info">
            <label for="birth-date">D.O.B.<span class="sr-only">(Date of Birth)</span></label>
            <input type="date" name="birth-date" id="birth-date" />
          </div>
        </section>
        <section role="region" aria-labelledby="html-questions">
          <h2 id="html-questions">HTML</h2>
          <div class="question-block">
            <p>1</p>
            <fieldset class="question" name="html-question-one">
              <legend>
                The legend element represents a caption for the content of its
                parent fieldset element
              </legend>
              <ul class="answers-list">
                <li>
                  <label for="q1-a1">
                    <input type="radio" id="q1-a1" name="q1" value="true" />
                    True
                  </label>
                </li>
                <li>
                  <label for="q1-a2">
                    <input type="radio" id="q1-a2" name="q1" value="false" />
                    False
                  </label>
                </li>
              </ul>
            </fieldset>
          </div>
          <div class="question-block">
            <p>2</p>
            <fieldset class="question" name="html-question-two">
              <legend>
                A label element nesting an input element is required to have a
                for attribute with the same value as the input's id
              </legend>
              <ul class="answers-list">
                <li>
                  <label for="q2-a1">
                    <input type="radio" id="q2-a1" name="q2" value="true" />
                    True
                  </label>
                </li>
                <li>
                  <label for="q2-a2">
                    <input type="radio" id="q2-a2" name="q2" value="false" />
                    False
                  </label>
                </li>
              </ul>
            </fieldset>
          </div>
        </section>
        <section role="region" aria-labelledby="css-questions">
          <h2 id="css-questions">CSS</h2>
          <div class="formrow">
            <div class="question-block">
              <label for="customer">Are you a frontend developer?</label>
            </div>
            <div class="answer">
              <select name="customer" id="customer" required>
                <option value="">Select an option</option>
                <option value="yes">Yes</option>
                <option value="no">No</option>
              </select>
            </div>
            <div class="question-block">
              <label for="css-questions">Do you have any questions:</label>
            </div>
            <div class="answer">
              <textarea id="css-questions" name="css-questions" rows="5" cols="24" placeholder="Who is flexbox..."></textarea>
            </div>
          </div>
        </section>
        <button type="submit">Submit</button>
      </form>
```
> **Step 41** <br>
Two final semantic HTML elements for this project are the `footer` and `address` elements. The `footer` element is a container for a collection of content that is related to the page, and the `address` element is a container for contact information for the author of the page.<br>
After the `main` element, add one `footer` element, and nest one `address` element within it.

```html
#index.html
    <footer>
      <address></address>
    </footer>
```
> **Step 42** <br>
Within the `address` element, add the following:
> ```html
> freeCodeCamp<br />
> San Francisco<br />
> California<br />
> USA
> ```

```html
#index.html
    <footer>
      <address>
        freeCodeCamp<br />
        San Francisco<br />
        California<br />
        USA
      </address>
    </footer>
```
> **Step 43** <br>
The `address` element does not have to contain a physical geographical location. It can be used to provide a link to the subject.<br>
Wrap a link around the text `freeCodeCamp`, and set its location to `https://freecodecamp.org`.

```html
#index.html
    <footer>
      <address>
        <a href="https://freecodecamp.org">freeCodeCamp</a><br />
        San Francisco<br />
        California<br />
        USA
      </address>
    </footer>
```
> **Step 44** <br>
Back to styling the page. Select the list elements within the navigation bar, and give them the following styles:
> ```css
> color: #dfdfe2;
> margin: 0 0.2rem;
> padding: 0.2rem;
> display: block;
> ````

```css
#styles.css
nav > ul > li {
  color: #dfdfe2;
  margin: 0 0.2rem;
  padding: 0.2rem;
  display: block;
}
```
> **Step 45** <br>
On the topic of visual accessibility, contrast between elements is a key factor. For example, the contrast between the text and the background of a heading should be at least 4.5:1.<br>
Change the font color of all the anchor elements within the list elements to something with a contrast ratio of at least 7:1.

```css
#styles.css
li > a {
  color: inherit;
}
```
> **Step 46** <br>
To make the navigation buttons look more like typical buttons, remove the underline from the anchor tags.<br>
Then, create a new selector targeting the navigation list elements so that when the cursor hovers over them, the background color and text color are switched, and the cursor becomes a pointer.

```css
#styles.css
nav > ul > li:hover {
	background-color: #dfdfe2;
	color: #1b1b32;
	cursor: pointer;
}

li > a {
  color: inherit;
  text-decoration: none;
}
```
> **Step 47** <br>
Tidy up the `header`, by using *Flexbox* to put space between the children, and vertically center them.<br>
Then, fix the `header` to the top of the viewport.

```css
#styles.css
header {
  width: 100%;
  height: 50px;
  background-color: #1b1b32;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: fixed;
  top: 0;
}
```
> **Step 48** <br>
When the screen width is small, the `h1` does not wrap its text content how it should. Align the text for the `h1` element in the center.<br>
Then, give the `main` padding such that the `Student Info` section header can be fully seen.

```css
#styles.css
h1 {
  color: #f1be32;
  font-size: min(5vw, 1.2em);
  text-align: center;
}

main {
  padding-top: 50px; 
}
```
> **Step 49** <br>
On small screens, the unordered list in the navigation bar overflows the right side of the screen.<br>
Fix this by using *Flexbox* to wrap the `ul` content. Then, set the following CSS properties to correctly align the text:
> ```css
> align-items: center;
> padding-inline-start: 0;
> margin-block: 0;
> height: 100%;
> ```

```css
#styles.css
nav > ul {
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
  align-items: center;
  padding-inline-start: 0;
  margin-block: 0;
  height: 100%;
}
```
> **Step 50** <br>
Set the width of the `section` elements to `80%` of their parent container. Then, use margins to center the `section` elements, adding `10px` to the bottom margin.<br>
Also, ensure the `section` elements cannot be larger than `600px` in width.

```css
#styles.css
section {
	width: 80%;
	margin-top: 0;
	margin-right: auto;
	margin-bottom: 10px;
	margin-left: auto;
	max-width: 600px;
}
```
> **Step 51** <br>
Replace the top margin of the `h2` elements with `60px` of top padding.

```css
#styles.css
h2 {
  border-bottom: 4px solid #dfdfe2;
  padding-top: 60px;
  margin-top: 0;
}
```
> **Step 52** <br>
Add padding to the top and left of the `.info` elements, and set the other values to `0`.

```css
#styles.css
.info {
  padding: 10px 0 0 5px;
}
```
> **Step 53** <br>
Give the `.formrow` elements top margin, and left and right padding. The other padding values should be `0`.<br>
Then, increase the font size for all `input` elements.

```css
#styles.css
.formrow {
  margin-top: 30px;
  padding: 0px 15px;
}

input {
  font-size: 16px;
}
```
> **Step 54** <br>
To make the first section look more inline, target only the `input` elements within `.info` elements, and set their `width` to `50%`, and left-align their text.

```css
#styles.css
.info input {
  width: 50%;
  text-align: left;
}
```
> **Step 55** <br>
Target all `label` elements within `.info` elements, and set their `width` to `10%`, and make it so they do not take up less than `55px`.

```css
#styles.css
.info input {
  width: 50%;
  text-align: left;
}

.info label {
  width: 10%;
  min-width: 55px;
}
```
> **Step 56** <br>
To align the `input` boxes with each other, set the `display` property to `inline-block` for all `input` and `label` elements within `.info` elements.<br>
Also, align the text to the right.

```css
#styles.css
.info input, .info label {
  display: inline-block;
  text-align: right;
}

.info input {
  width: 50%;
  text-align: left;
}

.info label {
  width: 10%;
  min-width: 55px;
}
```
> **Step 57** <br>
To neaten the `.question-block` elements, set the following CSS properties:
> ```css
> text-align: left;
> display: block;
> width: 100%;
> margin-top: 20px;
> padding-top: 5px;
> ``` 

```css
#styles.css
.question-block {
    text-align: left;
    display: block;
    width: 100%;
    margin-top: 20px;
    padding-top: 5px;
}
```
> **Step 58** <br>
Make the paragraph elements appear as a higher priority, with the following CSS properties:
> ```css
> margin-top: 5px;
> padding-left: 15px;
> font-size: 20px;
> ```

```css
#styles.css
p {
    margin-top: 5px;
    padding-left: 15px;
    font-size: 20px;
}
```
> **Step 59** <br>
It is useful to see the default border around the `fieldset` elements, during development. However, it might not be the style you want.<br>
Remove the border and bottom padding on the `.question` elements.

```css
#styles.css
.question {
  border: none;
  padding-bottom: 0;
}
```
> **Step 60** <br>
Remove the default styling for the list items of `.answers-list`, and remove the unordered list padding.

```css
#styles.css
.answers-list {
  list-style: none;
  padding: 0;
}
```
> **Step 61** <br>
Give the submit button a freeCodeCamp-style design, with the following CSS properties:
> ```css
> display: block;
> margin: 40px auto;
> width: 40%;
> padding: 15px;
> font-size: 23px;
> background: #d0d0d5;
> border: 3px solid #3b3b4f;
> ```

```css
#styles.css
button {
  display: block;
  margin: 40px auto;
  width: 40%;
  padding: 15px;
  font-size: 23px;
  background: #d0d0d5;
  border: 3px solid #3b3b4f;
}
```
> **Step 62** <br>
Set the `footer` background color to `#2a2a40`, and use Flexbox to horizontally center the text.

```css
#styles.css
footer {
  background-color: #2a2a40;
  display: flex;
  justify-content: center;
}
```
> **Step 63** <br>
Now, we cannot read the text. Target the `footer` and the anchor element within to set the font color to a color of adequate contrast ratio.

```css
#styles.css
footer, footer a {
  color: #dfdfe2;
}
```
> **Step 64** <br>
Horizontally center all the text within the `address` element, and add some padding.

```css
#styles.css
address {
  text-align: center;
  padding: 0.3em;
}
```
> **Step 65** <br>
Clicking on the navigation links should jump the viewport to the relevant section. However, this jumping can be disorienting for some users.<br>
Select all elements, and set the `scroll-behavior` to `smooth`.

```css
#styles.css
* {
  scroll-behavior: smooth;
}
```
> **Step 66** <br>
Certain types of motion-based animations can cause discomfort for some users. In particular, people with *vestibular* disorders have sensitivity to certain motion triggers.<br>
The `@media` at-rule has a media feature called `prefers-reduced-motion` to set CSS based on the user's preferences. It can take one of the following values:
> - `reduce`
> - `no-preference`
> ```css
> @media (feature: value) {
>   selector {
>     styles
>   }
> }
> ```
> Wrap the style rule that sets `scroll-behavior: smooth` within an `@media` at-rule with the media feature `prefers-reduced-motion` having `no-preference` set as the value.

```css
#styles.css
@media (prefers-reduced-motion: no-preference) {
  * {
    scroll-behavior: smooth;
  }
}
```
> **Step 67** <br>
Finally, the navigation accessibility can be improved by providing keyboard shortcuts.<br>
The `accesskey` attribute accepts a space-separated list of access keys. For example:
> ```html
> <button type="submit" accesskey="s">Submit</button>
> ```
> Give each of the navigation links a single-letter access key.<br>
> ***Note***: *It is not always advised to use access keys, but they can be useful*<br>
> Well done. You have completed the *Accessibility Quiz* practice project.

```html
#index.html
        <ul>
          <li><a href="#student-info" accesskey="i">INFO</a></li>
          <li><a href="#html-questions" accesskey="h">HTML</a></li>
          <li><a href="#css-questions" accesskey="c">CSS</a></li>
	</ul>
```
