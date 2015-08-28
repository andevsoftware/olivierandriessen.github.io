---
layout: post
title: Getting Started with Phalcon REST
comments: true 
redirect_from: "/2015/08/28/getting-started-with-phalcon-rest/"
permalink: /getting-started-with-phalcon-rest
color: e6db74
---

Setting up a REST API that is scalable, maintainable and better to document can be a huge amount of work. - *But it can be a lot less.* Phalcon REST provides a library of interchangable classes to help with authentication, permissions and formatting responses. 

First we look at the steps on how to set up a new project using the Phalcon REST boilerplate. After that we'll cover each concept.

## Quick start
A quick sum up, so you can quickly jump to each topic.

* [Get Started](#get-started) (*Installing boilerplate*)
* [Test endpoints using Postman](#test-endpoints-using-postman) (*You won't regret to read this first*)
* [Creating a user](#creating-a-user)
* [Retrieving user](#retrieving-user)
* [Creating a product](#creating-a-product)
* [Retrieving product(s)](#retrieving-products)
* [Updating a product](#updating-a-product)
* [Removing a product](#removing-a-product)

{% include title.html title="Get Started" %}

### Prerequisites

* PHP 5.6 or higher
* Phalcon v2 or higher
* Composer
* SQL-database

### Cloning project
We start with cloning the boilerplate

{% highlight bash %}
git clone https://github.com/olivierandriessen/phalcon-rest-boilerplate my-project
{% endhighlight %}

Then `cd` into that folder

{% highlight bash %}
cd my-project
{% endhighlight %}

### Install dependencies
Then we use [composer](https://getcomposer.org/) to pull in the dependencies

{% highlight bash %}
composer install
{% endhighlight %}

Note: When you are using a virtual box and you haven't installed Phalcon locally, you need to pass the flag `--ignore-platform-reqs` to the command.

### Setup config files

#### Default configuration
Next, copy `app/configs/default.template.php` and rename it to `app/configs/default.php`

{% highlight bash %}
cp app/configs/default.template.php app/configs/default.php 
{% endhighlight %}

**Note:** You can adjust this file to your needs later on.

#### Environment based configuration
We need to copy `app/configs/server.template.php` and rename it to `app/configs/server.develop.php`.

{% highlight bash %}
cp app/configs/server.template.php app/configs/server.develop.php 
{% endhighlight %}

**Tip:** Lets say you need to test this project on a staging server, what you could do is add `staging` to the switch statement inside of `app/bootstrap/config.php` and specify which config file to load. In order for this to work all you need to do after that is set the `APPLICATION_ENV` to `staging` on that environment.

### Import sql schema

Assuming that you've configured your database connection in `app/configs/server.develop.php` we can now import the sql schema from `schema/schema.sql`.

### It's working!
Now we've set everything up properly, when we open up the browser we should see the following:

![It's working](/public/images/getting-started-with-phalcon-rest-image-1.png)

{% include title.html title="Test endpoints using Postman" %}

### Installing Postman
Postman is a Chrome extension for building, testing and documenting API requests and keeping them organized inside collections. We are going to take advantage of that. But first we need to have it installed.

[Download Postman for Chrome](http://getpostman.com)

### Importing collection

Phalcon REST boilerplate comes with a built-in generator that outputs a Postman collection based on your endpoints.
It's located at `/export/postman-collection.json`.

![Import collection](/public/images/getting-started-with-phalcon-rest-image-2.png)

After you have saved the file to your local machine we can now open up Postman and import it.

![Import collection](/public/images/getting-started-with-phalcon-rest-image-3.png)

Now we've imported the collection we can start testing our endpoints!

{% include title.html title="Creating a user" %}

Coming soon

{% include title.html title="Retrieving user" %}

Coming soon

{% include title.html title="Creating a product" %}

Coming soon

{% include title.html title="Retrieving a product" %}

Coming soon

{% include title.html title="Updating a product" %}

Coming soon

{% include title.html title="Removing a product" %}

Coming soon
