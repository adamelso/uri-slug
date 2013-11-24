UriSlug
========

Canonicalizes a string to a URL-friendly format. Based on a combination of WordPress functions.


Installation with Composer
-----------------------------------

Add to your composer.json

    {
        "require": {
            "urislug/urislug": "dev-master"
        }
    }


Example Usage
---------------------

    <?php

    require __DIR__.'/vendor/autoload.php';

    // Create as a new instance
    $greeting = new \UriSlug('Hello, there ^_^'); 

    // automatically casts to a string if treated as such
    echo $greeting; // prints 'hello-there-_'

    // same as above
    echo $greeting->getSlug(); 
    
    // Factory method creates new instance with the given text and returns the slug string
    echo \UriSlug::create('Welcome to Großröhrsdorf!!1!one!'); // prints 'welcome-to-grosrohrsdorf1one';


Licence
----------

As this is based on functions found in WordPress 3, and WordPress is released under the GPL v2 licence, so is this helper class.
