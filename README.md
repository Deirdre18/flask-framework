# The Flask framework 

is a web-based framework using Python language that began it's life as an April Fool's joke was has since risen to become one of the biggest Python frameworks become the most popular and widely supported Python frameworks within the Python community. 

The flask framework is what is known as a micro framework it allows us to get up and running building websites with as minimal Python code as possible It doesn't come with, micro frameworks don't come with batteries included which means that we don't get a lot of features that we would get with Django but the appeal of flask is its simplicity. 

We'll use flask throughout this lesson.  To run a Python server side project we use to serve HTML files from a server we'll use it to write logic inside of our Python templates, which will allow us to use 'for' loops and 'if' statements and also inheritance, which will look out, and we'll also learn how to submit forms which will allow us to take data from the client posted to the server.  In the instance that a user fills with that information. So we're going to learn how to create and run a flask application, we're gonna learn how to serve HTML, CSS and JavaScript from the backend. I'm gonna make you learn how to make our code reusable. By using template logic, we learn how to post data from HTML forms on back-end, and we'll also learn how to deploy our project using a platform called Heroku so we can serve our project. Also we can host our project externally for all the world to see.

# Hello Flask

## What is it?

Flask is a small framework

## What does it do?

Allows us to build web apps

## How do you use it?

First we need to install it!
LESSON:

    Start of transcript. Skip to the end.
    In order to get up and running with the flask framework what I'm going to do is I'm
    going to create a new brand new workspace in cloud 9 I will give it a name of
    flask and this is going to be using a blank template and then we're
    going to click on create workspace so what we're going to do throughout this
    this lesson is we're going to just create a simple website that outputs
    some pages and we'll take a look at how you tie those pages together and how we
    can inject content from the server side and pass information back from the
    client side to the server side. What we're going to do is
    we're just gonna create a simple little hobbit website for the the company of
    dwarves later on but what we're going to do now is firstly I'm just going to
    delete this readme file and I'm going to create a brand new file but first let's
    do sudo pip3 install Flask and that will install the Flask framework for us
    and once that's done then we can go ahead and we should be able to we can go
    ahead and create a new file now. This would be the default file that we
    will use this would be the main file that will run the application and in flask
    the convention is to either called this run.py or app.py. I'm going to call it
    run.py so what I want to do now is I want to open up that run.py file
    and I'm going to say from flask import flask through the import flask object
    from the flask module and then we want to say app = flask
    then underscore underscore name what we want to do that is we want to say we
    want to use our decorator to say we have @ symbol app.route and then in
    their brackets we have just forward slash as a string then we say def hello()
    and then we're going to return hello world and this will just output hello
    world out to the browser and what we want to do then is we won't say if
    dunder name is equal to dunder main and inside of that we're a few things we
    need to do here so we need to app.run() which will run the
    server but there are a couple of things we need to pass in and we can retrieve
    those from the cloud nine but this here these kind of ten lines here are the
    usual ten lines of code that you would use to run a flask application we need a
    couple of things here we need from retrieved from the cloud nine work space
    and we do that by importing OS and then inside of our app.run we pass in the
    series of arguments so the first argument passing is the host name
    OS.environ.get will allow us to get the IP address now this is so we can
    tell flask which what the IP address we want to run this on is the port that we
    want to open for this so next one we do is the port and we need to cast that to a
    string or an int sorry so int OS out and fire not get past your port and we want
    to say that the debug mode is true because we're going to be developing and
    we want to be able to to do some debugging so what I need to do now is
    there a couple ways I could run this I can either bring this directly from the
    command line now by doing Python3 run.py and that will allow us to run
    brill in our application here or what we can do is we once we have this
    information we can just use click on the Run button up the very top on there on
    cloud nine will give us the URL that's running on so we can see now we're a
    flask - username
    .c9users.IO now if I go in and change something some piece of
    code we can see that changes so hello flask now if I remove our debug
    statement and stop running code and run the code again now head over to that in
    the browser so I'm gonna click open now if I go change something while debug
    mode is not on it won't allow us to change so I can refresh here and it
    doesn't update to hello hello it sticks with hello Flask so this is why
    it's important to have debug equal to true when we're developing our applications
    
    
    
# Rendering HTML Code
 
## What is it?

Returning HTML code from a Flask function


## What does it do?

Allows us to render HTML code from the server


## How do you use it?

By returning a string that contains HTML tags

LESSON:

Now that we have our Flask application running what we can do is inside the
return statement of our hello function we can actually put in pure HTML so if I
were to say h1 hello and then close that h1 and then say create a h2 after
that and say flask I can go ahead I'm gonna save this and then I can just let
me make sure my application is running so if i refresh now we can see hello and
flask are now being displayed in a h1 and h2 respectively so this shows us
that we can actually return pure HTML code from from inside of our methods and
then the browser sees that and goes oh this is HTML code so I'm gonna render
this as HTML code a better way to do this is to use the render template
function so the render template function we can import from flask and then we
return render function and we can say index.html now when we say when we put
the name of a file flask always assumes the top file as any directory called
templates which would be in the same the same directory level as the
run.py file. So in order to do that was a create templates folder inside of the
Flask directory we'll create a new file called index.html. Iinside of there we're
just gonna pop it in some HTML code so I'm gonna have my HTML tags inside of
that and I'll have a head tag we give that title and we just say give it a
title of hello flask and then give our code body
an inside of the body then we will just create simple nav bar for example we'll
have a ul and we'll have an li inside of that and inside of the li then we'll
have an href is equal to put in a content that just says low or
homepage and we just put in hash as the href there for the time being so if I go
ahead and refresh now you can see that this little index.html page is
in fact running so we have our navigation bar we have our lists
displaying inside of the inside of the browser so the render template is
retrieving the text from the HTML index.html file and then sending it to
the browser and the browser is picking up on it and displaying displaying it as
markup so if I put in a h1 and just say homepage and inside of our nav I'll
just create a second page it says about and I get rid of the word page there I get rid
of both page in both of those and then what I can do is I can actually copy all
of this code and I'll create in an HTML page and inside that about the HTML page
I'll paste the content from the index.html page I'll just update the
h1 to say that this is the about page and then what we'll look at next is how
we can actually link to these different pages using by different methods of
using the href to determine the path.

# Routing
 
## What is it?

Routing


## What does it do?

Allows us to swich between views using URLs


## How do you use it?

By creating routes

LESSON: 

Okay so in order to hook up our views in our templates now what we need to do is
we need to use what's called routing and routing will allow us to basically route
to a specific function or a view and I suppose this was called here this
function here is typically referred to as a view and then this
decorator on top at the very top here on line six this is the route so our
application knows that if we go to our domain forward slash then it will use the
function that has that route so what we can do is we can create additional
routes so what I'm going to do now is I'm going to create a new view function
so we're gonna say you have decorator of app.route and then we say forward
slash about supplies a def about and then I can just return render template
about.html I'm just going to rename my hello function there to index just to make it a bit more but
more readable and a bit more correct so instead of them having our hash symbol
inside of the href's I'm going to update them to forward slash for the home index page and then
forward slash about for the about page so what I need to do is I need to add those
changes to both of those pages so inside of the index.html I need to do it on the
inside of the about.html so once I've done that both those files I can
just go ahead and refresh and you can see them once we click on the about link
then we're brought to the about page we can click between the two for a while
and okay get a feel for how it works there is another way of doing this we
can what we can do is we can say we can use what's called a template logic and
the template logic allows us to inside of these curly braces we can say URL
underscore for and that's a function where it will take a string argument we
will say index in the first one and these two curly braces here allow, we'll
say to flasks look I need you to inject some piece of text here the piece of I
wants is the output of this URL for index so go ahead and we do that again
for the about page so if you remember earlier we have view functions are named
index and about and so we pass in the name of the views that we want to call
and flask will give us tell us what the route for that is and inject it in place
there I mean do the same then on the about page so you can see if you keep an eye
on the URL bar there when you're switching between the two the URLs are
actually updating to the number forward slash index and for slash about for the about page
and that's just those name function names there so we say URL for the
specific view if I change mine to say hello now then it will give me an error
to say they couldn't find a name an endpoint for the index did you mean
hello instead and then evens go so far as to suggest the name that we should
have inside the URL there so let's go ahead add another one so add in a
contact page say app.route and then this is forward slash content and then the
name of the function would be contact and we just returned another template called render template. And the template that will return will be contact on HTML so I'm gonna copy the code from the index.html file actually I won't just yet I will update the index.html file to include the URL for the contact page so we'll just update that there in the href and then we'll update the content I then I can go ahead once that's done then I'll copy the whole a copy that cross into the about HTML page first and then I'll copy the whole HTML file and I will copy it in to create a new template in templates directory called contact HTML and I will paste all of that code in there and I'll just update the h1 on the page to say contact us okay I still have my error in there because I didn't update save this file and I need to change this back to index,and if I change contact to hello, Flask is actually smart enough to actually know the difference and get an idea of the actual page that it is supposed to render of the details. Suppose app will actually suggest that to you to us when we're trying to get it to work so I'm gonna say it everything back to normal then refresh and we can see now that everything is working.