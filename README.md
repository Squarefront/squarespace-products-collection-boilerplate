Squarespace Products Collection Boilerplate
=======

> A boilerplate for adding a "products" collection to Squarespace developer templates.



## Overview
Squarespace's Developer mode allows you to add [collections](http://developers.squarespace.com/collections/) to the backend CMS in order to create custom types of content collections. This repo is a boilerplate and starting point for adding a Products collection to your template.



## How Collection Templates Work
There are two ways to add collections to your Squarespace template: through Squarespace System Collections, or by creating your own collections.

#### Squarespace System Collections
Squarespace creates and manages an internal database of collection types called System Collections. These read-only System Collections are used in various [default Squarespace templates](http://squarespace.com/templates). To add a System Collection to your template, you would specify them in your [template.conf](http://developers.squarespace.com/template-configuration/) like the following example:


```json
{

    "name" : "Template Name",
    "author" : "Your Name",

    "layouts" : {
        "default" : {
            "name" : "Default",
            "regions" : [ "site" ]
        }
    },

    "navigations" : [
        {
            "title" : "Main Navigation",
            "name" : "nav-main"
        },
    ],

    "stylesheets" : [
        "base.less"
    ],

    "systemCollections" : [
        "album",
        "events",
        "gallery",
        "products"
    ]

}
```

The `systemCollections` key will configure your template to load System Collections for whichever collection types you want.

**Note:** Even if you have specified a System Collection in your `template.conf`, you can still overwrite the System Collection if a custom collection exists in your template files.


#### Custom Collections
Adding your own custom collections are done by creating a configuration file and one or two template files in the `collections` folder of your Squarespace template. So the two (or three) files you'll need are:

* yourcollectionname.conf
* yourcollectionname.list
* yourcollectionname.item

Please see the [official documentation](http://developers.squarespace.com/collections/) to learn how to add a custom collection to your template.



## Installation
The easiest way to install a template into your Squarespace Developer mode template is to clone this repo and move the collection template files and configuration file into your template's `collections` folder.

### How To Use Your Custom Collection
One you've installed your custom collection files, head into your Squarespace website. You should now see your custom collection when **adding a new page to a navigation**.