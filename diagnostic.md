# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.


What is the purpose of a backend?

```bash
The backend is what takes requests from the client and returns what the client
wants. It exists so that you can have states/data persist between sessions.
It also exists so that your application can serve more than one client at once.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```bash
model
```

Which layer in the MVC pattern communicates with the model?

```bash
controller
```

Why don't we use views in our interpretation of the MVC pattern?

```bash
We will send our data back to the client and render it with clientside
javascript/html/css etc. probably.
```

What does C.R.U.D stand for?

```bash
Create Read Update Destroy
```

In which part of the MVC pattern can we find C.R.U.D actions?

```bash
controller
```
List at least 5 standard actions that C.R.U.D corresponds to?

```bash
index, new, create, show, edit, update, destroy
```

A user action fires a `GET` request for `person/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list)

```bash
* the HTTP request gets to your backend over the web
* the request goes to the router first
* the router selects the proper controller and action and sends the request there
* the controller fires the method (show) that corresponds to the selected action
* the "show" action gets the `person/1` object from the model and returns it to the controller
* the controller sends that object to the view (but we skip that step)
* the view probably uses the object to render the html/css and sends it back to the client
* since we skip the view, probably the controller turns the object into JSON and sends it to the client
* the client uses the JSON and its own JavaScript to update what the user sees
```

What is the command to generate a new rails-api app?

```bash
rails-api new // and there are a lot of other options after that e.g. rails-api new blog_app --skip-javascript --skip-sprockets --skip-turbolinks --skip-test-unit --database=postgresql
```

What is the command to start an instance of a rails server?

```bash
rails server
```

What are the commands to drop, create and migrate a database? (3 bullet points)

```bash
* rake db:drop
* rake db:create
* rake db:migrate
```

What is the command to scaffold a pet with a name and an age?

```bash
rails-api g scaffold pet name:string age:integer
```

List two advantages of using serializers? (2 bullet points)

```bash
* serializers make the api safer
* serializers make the api easier to use
```
