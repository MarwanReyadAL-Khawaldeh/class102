**Markdown is a lightweight and easy-to-use syntax for styling all forms of writing on the GitHub platform.**

# What is Markdown?
Markdown is a way to style text on the web. You control the display of the document; formatting words as bold or italic, adding images, and creating lists are just a few of the things we can do with Markdown. Mostly, Markdown is just regular text with a few non-alphabetic characters thrown in, like # or *.

You can use Markdown most places around GitHub:

 * Gists
* Comments in Issues and Pull Requests
* Files with the .md or .markdown extension

# Syntax guide
Here’s an overview of Markdown syntax that you can use anywhere on GitHub.com or in your own text files.

# Example
1. # Headers 

* # Headers
* ## Headers
* ### Headers

2.  # imges
![GitHub Logo](https://miro.medium.com/max/719/1*WaaXnUvhvrswhBJSw4YTuQ.png)

----

# GitHub.com
 uses its own version of the Markdown syntax that provides an additional set of useful features, many of which make it easier to work with content on GitHub.com.

# Syntax highlighting
Here’s an example of how you can use syntax highlighting with GitHub Flavored Markdown:
```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
----

# Remote Repositories
In order to collaborate on Git projects, you must interact with remote repositories, versions of a project residing online or on a network. You can work with multiple repositories, for which you can have read/write or read-only privileges. Teams can use remote repositories to push information to and pull data from.

# Seeing Your Remotes
By running the git remote command, you can view the short names, such as “**origin,**” of all specified remote handles.

By using **git remote -v**, you can view all the remote URLs next to their corresponding short names.

# **Example**
$ cd example

$ git remote -v
---
remote1 https://github.com/remote1/example (fetch)
---
remote1 https://github.com/remote1/example (push)
---
remote2 https://github.com/remote2/example (fetch)
---
remote2 https://github.com/remote2/example (push)
---
remote3 https://github.com/remote3/example (fetch)
---
remote3 https://github.com/remote3/example (push)
---
