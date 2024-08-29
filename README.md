# Exercise: Create an Interactive Registration Form

## Learning Goals

By completing this exercise, you will be able to:

- Design and implement a complex registration form using HTML
- Apply advanced CSS styling techniques to form elements
- Enhance form usability and accessibility
- Implement basic form validation using HTML5 attributes

## Introduction

Welcome to the world of web form mastery!

In this exercise, you’ll step into the shoes of a front-end developer tasked with creating a sleek, user-friendly registration form for a cutting-edge tech startup. Your mission is to craft a form that not only collect essential user information but also provides an engaging, intuitive user-experience.

Aas you build this form, you’ll apply your knowledge of HTML form elements and CSS styling techniques. You’ll also explore new concepts like form validation. Remember, in the world of web development, forms are often the gateway between users and services - your form could be the first impression a user has of the entire platform!

Are you ready to create a registration form that’s both functional and fabulous? 

## Getting Started

1. Fort this repository
2. Clone the repository to your computer
3. Open the repository in VS Code
4. Start the Live Server in VS Code
5. Follow instructions

## Required Fields for the Registration Form

Your form should include the following fields:

- First Name (required)
- Last Name (required)
- Email Address (required)
- Password (required)
- Date of Birth (optional)
- Terms and Conditions Checkbox (required)
- Submit Button

## Instructions

### Part 1: Sketch Out a Form

Before you start to write even the first line of code, we want you to first create a sketch of the anticipated registration form. It doesn’t matter whether you use pen and paper, or you use a tool like Excallidraw.

Make sure to include the sketch in the `sketch` folder. Please use one of the following file formats:

- PNG
- JPG
- PDF

Once you have completed your sketch, proceed to the next part.

### Part 2: HTML Structure

Now that you have a visual representation of your form, it's time to bring it to life with HTML. Follow these steps:

1. Create a new HTML file named `index.html` in the root directory of your project.
2. Set up the basic HTML structure with `<!DOCTYPE html>`, `<html>`, `<head>`, and `<body>` tags.
3. Within the `<body>` tag, create a `<form>` element to contain your registration fields.

### Part 3: CSS Styling

Style your form in `styles.css` to make it visually appealing. 

You styling should include:

1. A cohesive color scheme
2. Custom styles for input fields, radio buttons, and checkboxes
3. Hover and focus states for interactive elements
4. A responsive layout that works on both desktop and mobile devices

### Part 4: Form Validation

Implement basic form validation using HTML5 attributes.

Include:

1. Required field validation
2. Email form validation
3. Password strength requirements (e.g. minimum length)

### Part 5: Enhances User Experience

Add features to improve the user experience:

1. Placeholder text for input fields
2. Clear error messages for validation failures

## Submission

When you’re completed the exercise:

1. Commit your changes:

```bash
git add .
git commit -m "Completed Registration Form exercise"
git push origin main
```

2. Create a Pull Request
3. Submit the URL of your Pull Request

## Bonus Challenge

### Add a Country Dropdown to the Form

Because the tech startup expanded and now offers their services in many countries, it is now required to add a dropdown element in which users can select their residential country.

1. Add a dropdown menu to the form with a list of countries.
    1. Use the `<select>` and`<option>` elements to create the dropdown.
2. Include a diverse range of countries to accommodate the startup's global user base.
3. Style the dropdown menu to match the overall design of the form.
4. Ensure the dropdown is responsive and works well on both desktop and mobile devices.

## You Got Questions? We Got Answers!

<details>
<summary>How do I make my form responsive?</summary>

Here are a couple of ways you could use to make your form responsive:
    
1. Use relative units (%, em, rem) instead of fixed units (px) for sizes.
2. Implement flexbox for form elements.
3. Use CSS media queries to adjust layout for different screen sizes.
4. Consider the mobile-first approach: design for mobile, then add complexity for larger screens.

Example:

```css
    @media screen and (min-width: 768px) {
        form {
            max-width: 600px;
            margin: 0 auto;
        }
    } 
```
</details>

<details>
<summary>How can I style form validation messages?</summary>

You can style for m validation messages using CSS Pseudo-classes `:valid` and `:invalid`, along with the `:required` pseudo-class for required fields.
    
Example:

```css
    input:invalid {
        border-color: red;
    } 

    input:valid {
        border-color: green;
    }

    input:required {
        border-left: 2px solid blue;
    }
```
</details>

<details>
<summary>How do I create custom checkboxes?</summary>

To create custom radio buttons or checkboxes:
    
1. Hide the default input with `opacity: 0;`
2. Create a custom appearance using the label
3. Use the `:checked` pseudo-class to style the selected state

Example:

```css
    .custom-radio input[type="checkbox"] {
        opacity: 0;
        position: absolute;
    }
        
    .custom-radio label {
        position: relative;
        padding-left: 30px;
    }

    .custom-radio label::before {
        content: '';
        position: absolute;
        left: 0;
        top: 0;
        width: 20px;
        height: 20px;
        border: 2px solid #333;
        border-radius: 50%;
    }

    .custom-radio input[type="checkbox"]:checked + label::before {
        content: '';
        position: absolute;
        left: 5px;
        top: 5px;
        width: 10px;
        height: 10px;
        background: #333;
        border-radius: 2px;
    }
```
</details>

<details>
<summary>How do I ensure my form is accessible?</summary>
To improve form accessibility:
    
1. Use semantic HTML elements (e.g. `<label>`, `<fieldset>`, `<legend>`)
2. Ensure all form controls have associated labels
3. Use the `for` attribute on labels, matching the id of the form control
4. Provide clear, descriptive error messages
5. Ensure sufficient color contrast
6. Make your form keyboard-navigable

Example:

```html
    <div class="form-group">
        <label for="email">Email Address:</label>
        <input type="email" id="email" name="email" required">
    </div>
```
</details>

Remember, every great website you've ever used stared with these same fundamental building blocks. The skills you're developing now - crafting clean HTML, writing efficient CSS, and thinking about user experience - are the very same skills used by professional web developers every day!