## Linux Containers
Docker is really just Linux containers which are a type of virtualization.

Virtualization has its roots at the beginning of computer science when large, expensive mainframe computers were the norm.

Virtualization and specifically virtual machines which are complete copies of a computer system from the operating system on up.

The downside to a virtual machine? Size and speed. A typical guest operating system can easily take up 700MB of size.

So if one physical server supports three virtual machines, that’s at least 2.1GB of disk space taken up along with separate needs for CPU and memory resources.


### Containers vs Virtual Environments
Virtual environments are used to isolate Python software packages locally.
We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer.
They still rely on a global, system-level installation of Python albeit they can refer to the proper version.
So when we use Python 2.7 in a project, we’re pointing to an installation of Python 2.7 on the computer itself, not actually within the virtual environment.

### What is Docker?
Docker its a tool to isolate the whole development environment you are working on , programming language, software packages, databases, and more.

### Why Docker?
With Docker we now longer have to mess around with virtual environments. We can faithfully reproduce a production environment locally. And Docker can be shared among team members so everyone is working on the same setup. Wins all around.

### How It works ?
Docker is really just Linux containers which are a type of virtualization. Virtualization has its roots at the beginning of computer science when large, expensive mainframe computers were the norm. How could multiple programmers use the same single machine? The answer was virtualization and specifically virtual machines which are complete copies of a computer system from the operating system on up.
Conclusion
Docker is a way to run Linux containers
Containers are a lightweight alternative to Virtual Machines
Dockerfile is a list of instructions for creating an image
Images are made up of one or more layers
Containers are a running instance of an image
docker-compose.yml controls how to run the container
Containers are stateless and ephemeral in nature. We can link the local filesystem via volumes but things become more - complex with databases

### Django for APIs
Note that Django’s REST framework works alongside the regular Django web framework, which means that to build an API, Django must be also installed an configured before.

To start, we start a new project and a new app, we do the regular setup like adding the app to our settings, as well as the templates and the urls. We might also need to create a model and a superuser in case we want to control the project from the admin panel.

Now to start working with Django’s REST framework, you will have to install it:

### poetry add djangorestframework
Then we will have to add it to our settings.py as a third party app, for example: 'rest_framework'. After that, it is preferred if we create a new app named differently like 'api', and add it to our apps list in settings.py. This is a good practice so that if we create new apps in the future, each app can contain the models, views, templates and the urls for dedicated webpages. Note that this api app will not have its own database model, so we do not have to migrate. Then we add the app’s urls and update the views just like we usually do.
In the views file, we import the class generics from rest_framework. Also, assuming that for the first app, it was just an app that handles books that have titles, ISPNs and so on. We also import this model from its dedicated models file. Finally, we import BookSerializer from .serializers
