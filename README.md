# 100 Objects Exhibition

[![license][license-image]][license-url] [![Build Status][travis-image]][travis-url]
> 100 Objects exhibit marketing page

## Credits

* Jack Kelly
* Starrie Williamson
* Holly Robertson - Content

Open Source Projects

* Stefan Kovac, Flex Layout Attribute
* Nick Williams - Headroom JS
* Davide Calignano - Medium Lightbox

## Prerequisites

To install this project, you'll need the following things installed on your machine.

* [Jekyll](http://jekyllrb.com/) - `$ gem install jekyll`
* [NodeJS](http://nodejs.org) - use the [installer](https://nodejs.org/en/download/)
* NPM - `$ npm install npm -g`
* Update Bundler - `$ bundle update`

## Local Installation

1. Clone this repo, or download it into a directory of your choice.
2. Inside the directory, run `npm install`.
3. Then run `bundle update`.

## Usage

**Development mode**

To build your site run the following command

```shell
$ gulp
```

This will give you file watching, browser synchronisation, auto-rebuild, CSS injecting etc.

```shell
$ gulp serve
```

**Deploy to Development - https://uvalib.github.io/100objects/**

You can easily deploy your site build to GitHub pages with the command
```shell
$ gulp deploy-to-test
```
**Deploy to Production - http://100objects.lib.virginia.edu/**

You can easily deploy your site build to UVA Libraries production server with the command
```shell
$ git push origin master
```

## Tests
You can run accessibility test set to WCAG Level AA
```shell
$ gulp accessibility
```

If you want to run the HTML tests on your local machine please install `gem install html-proofer`. And then run the tests using
```shell
$ htmlproofer ./_site
```

[license-image]: https://img.shields.io/badge/license-ISC-blue.svg
[license-url]: https://github.com/uvalib/100objects/blob/master/LICENSE
[travis-image]: https://travis-ci.org/uvalib/100objects.svg?branch=master
[travis-url]: https://travis-ci.org/uvalib/100objects

## Adding New 101st Object Submissions
* If an image was submitted, then save the image to your computer and upload into the github repository to the /images/newobjects 
directory. Identify the width and height of the uploaded image to use later.
* Create a new file in the _newobjects folder using the naming convention of object101?.md 
where the question mark gets replaced with a letter of the alphabet. Start backwards with 
the letter _z_ as you add a new one, which should allow for up to 26 submissions - we can come 
up with a name convention change if you expect more. This will place the newer item at the 
top of the file directory listing and thus put it at the top of the page. For example, 
_object101z.md_ was created with Molly's submission information into it since her entry is 
the first received. Then Margo Smith's entry was put in _object101y.md_ since it was the 
second.
* Populate the new *object101* file with the follow lines (which contain an example of content):
```
—
ready: "true"
date_submitted: "August 14, 2017"
name: "Eric Seidel"
affiliation: "Current UVA faculty or staff"
may_we_share: "no"
email_address: "eks4x@virginia.edu"
next_object: "The peace symbol"
why: "We need it now"
photo_file_name: "101.png"
photo_credit: "UVA Library"
photo_width: "800"
photo_height: "800"
—
```
* Make sure you specify the dimensions from the uploaded image file in the corresponding photo_width and photo_height 
lines inside of the new file. If an image was not submitted, then just use "101.png" for the file name and 800 for both 
the width and height. Without image width and height correctly entered, the image may be distorted.
* When may_we_share has a value of "no" then the person who submitted the item is not displayed on the output page.

NOTE: The code looks for the _ready_ line and makes sure it has a value of "true" before adding the content to the 
submissions page. So you may tentatively create new object submission files and have that 
line with a value of "false" and it will not appear on the page.

## Designers/Developers

The underlying templates used so far for exhibitions have the [Flex Layout Attribute](http://progressivered.com/fla/)
for responsive design and laying out the content.

## Content Writers
1. Edit the files in the [master branch](https://github.com/uvalib/100objects/tree/master)
2. Build will automatically begin
3. View your changes in production at http://100objects.lib.virginia.edu/

