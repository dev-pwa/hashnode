## WEb формы для сайта онлайн генератор. Создать форму для сайта



Web forms are a very powerful tool for interacting with users. It's one of the main points of interaction between a user and a web site or application. 

Forms allow users to enter data, which is generally sent to a web server for processing and storage, or used on the client-side to immediately update the interface in some way. 

A web form's HTML is made up of one or more form controls (sometimes called widgets).

Let's make a local copy of our HTML template — you'll enter your form HTML into here.

```
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8">
    <title>Test page</title>
  </head>

  <body>
    <p>Hello, this is a test page!</p>
  </body>

</html>
```

Forms start with `<form>` container element, specifically for containing forms that supports some specific attributes to configure the way the form behaves. The standard practice is to set at least the `action` and `method` attributes like this:

```
<form action="/my-handling-form-page" method="post">
 <ul>
  <li>
    <label for="name">Name:</label>
    <input type="text" id="name" name="user_name">
  </li>
  <li>
    <label for="mail">E-mail:</label>
    <input type="email" id="mail" name="user_email">
  </li>
  <li>
    <label for="msg">Message:</label>
    <textarea id="msg" name="user_message"></textarea>
  </li>
 </ul>
</form>

```

The `action` attribute defines the location (URL) where the form's collected data should be sent when it is submitted.
The `method` attribute defines which HTTP method to send the data with (`get` or `post).

Let's add the above `<form>`element into your HTML `<body>`. On the `<input>` element, the most important attribute is the `type` attribute, it defines the way the <input> element appears and behaves. 

In our example, we use the value `<input/text>` , it's a single-line text field that accepts any kind of text input.

For the second input, we use the value `<input/email>`, which defines a single-line text field that only accepts a well-formed e-mail address. 

The `<input>` tag is an empty element, that doesn't need a closing tag. `<textarea>` is not an empty element, it should be closed with the proper ending tag. To define the default value of an `<input>` element you have to use the value attribute like this:
```<input type="text" value="by default this element is filled with this text">``` 

To define a default value for a `<textarea>`, you put it between the opening and closing tags of the` <textarea>` element, like this:
`<textarea>and by default it will be text</textarea>`


## The `button` element  

The `<button>` element accepts a `type` attribute - one of three values: `submit`, `reset`, or `button`.

- A click on a `submit` button (the default value) sends the form's data to the web page defined by the action attribute of the `<form>` element.

- A click on a `reset` button resets all the form widgets to their default value immediately. 

- A click on a `button` is just a clickable button.

![Alt Text](https://cdn.hashnode.com/res/hashnode/image/upload/v1624819634546/Xwj-H6-ps.png)

## Sending form data to your web server

The last part is to handle form data on the server side. The `<form>` element defines where and how to send the data thanks to the `action` and `method` attributes.

We provide a name to each form control. It tells the browser which name to give each piece of data and, on the server-side, they let the server handle each piece of data by name. The form data is sent to the server as `name/value` pairs.

To name the data in a form you need to use the `name` attribute on each form widget that will collect a specific piece of data. In our example, the form will send 3 pieces of data named "user_name", "user_email", and "user_message". That data will be sent to the URL "/my-handling-form-page" using the HTTP POST method.

![Alt Text](https://cdn.hashnode.com/res/hashnode/image/upload/v1624819636569/yedQ8CweT.png)

This form with added styling can be found [here](https://github.com/ivanadokic/form/blob/main/form.html)

### Next Steps

We will need to add some form validations.

To connect please check my [Github](https://github.com/ivanadokic), [LinkedIn](https://www.linkedin.com/in/ivana-dokic/) or [Twitter](https://twitter.com/LloydPile). 

Thank you for reading!
