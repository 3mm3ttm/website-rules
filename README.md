# Website Rules

The rules of HTML that every device follows.
> \[!NOTE]
> This repo is not finished. Try posting on the wiki!

all devices work differently, and their browsers are similar, but there are some tiny 
details to take into mind. For example, Linux Servers are case-sensitive.

## 1.  &ensp;index.html

if you name a file in the root directory "index.html," the browser will load this webpage 
instead of any other. `index.html is the magical name that can be assigned to any directory,
not just the root.

`www.example.com/` will bring you to `www.example.com/index.html`.

`www.example.com/directory/` will bring you to `www.example.com/directory/index.html`.

## 2.  &ensp;not_found.html

creating a webpage that will redirect to this one is not difficult on web hosting services, but on 
other services, it will be a bit harder.

### Apache Servers

1. create a new `.htaccess` dotfile in the root directory.

2. open the file in a text editor, and type `ErrorDocument 404 /not_found.html`.
3. create your `/not_found.html` file in the root.
4. open your domain, and enter an incorrect directory identifier in the URL bar.

### IIS Servers

1. use the [IIS Manager](https://learn.microsoft.com/en-us/iis/get-started/getting-started-with-iis/getting-started-with-the-iis-manager-in-iis-7-and-iis-8)
to navigate to Error Pages.

2. add a new entry for status code 404, and point it to the relative path of your file. in our case, `/not_found.html`.

### Website Hosting Services

most web hosting services have their own 404 error page, but some, like WordPress, give you a not-found file that you can edit.

[my website](https://trollfacegames.neocities.org), hosted on [Neocities](https://neocities.org), will give you a `not_found.html` that you can edit, but it only exists in the root
directory.
