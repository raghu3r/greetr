# @raghu3r/greetr

Used to Greet users in the language you want to.

- Ex: Greeting of the Day Mr/Ms. XXXX  // Can get same greeting in whatever the language you want.

## Install

```
$ npm install @raghu3r/greetr
```

## Usage

```js

// app.js

// gets a new object (the architecture allows us to not have to use the 'new' keyword here)
var g = G$('John', 'Doe');

// use our chainable methods
g.greet().setLang('es').greet(true).log();

// let's use our object on the click of the login button
$('#login').click(function() {
   
    // create a new 'Greetr' object (let's pretend we know the name from the login)
    var loginGrtr = G$('John', 'Doe');
    
     // hide the login on the screen
    $('#logindiv').hide();
    
     // fire off an HTML greeting, passing the '#greeting' as the selector and the chosen language, and log the welcome as well
    loginGrtr.setLang($('#lang').val()).HTMLGreeting('#greeting', true).log();
    
});

// HTML to be

<html>
    <head>
        
    </head>
    <body>
        <div id="logindiv">
            <select id="lang">
                <option value="en">English</option>
                <option value="es">Spanish</option>
            </select>
            <input type="button" value="Login" id="login" />
        </div>
        <h1 id='greeting'></h1>
        <script src="//include jQuery"></script>
        <script src="// include Greetr.js"></script>
        <script src="app.js"></script>
    </body>
</html>

```

- Here you go!! Play around with different languages you know by editing Greetr.js library file. Currently we support English and Spanish.