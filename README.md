# What is it ?

## The problem to solve

In my professional work, we have recently started using Webex, and there's one really annoying thing about it:
the links in messages are only clickable if they point to a site visible on the internet.
Naturally, most of the links we use are to our internal systems.

## BREAKING NEWS December 12, 2024 :
It seems that the problem is fixed in latest version of Webex, so this little piece of code is longer useful in this case.

## The solution

To work around this problem, the chosen solution is to use a web page that is visible on the internet,
which will then redirect to the page whose URI is passed as a parameter.
This way, Webex considers the link valid and makes it clickable, automatically redirecting to the internal page.

## Usage

The principle is to prepend the desired link with https://joelhecht.github.io/auto-redirect/redirect.html?, or for a shorter version, with https://tinyurl.com/5n8jmysz?.

So, let's suppose we want to post a message containing a link to the page http://localhost.
In Webex, you add the link using the shortcut CTRL-K.
In the link address, you simply enter https://tinyurl.com/5n8jmysz?http://localhost.

## More

Of course, this principle is not only applicable to Webex. Any other tool that performs the same link verification can benefit from it.
