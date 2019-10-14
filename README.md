# HAML  (HTML Abstraction Markup Language) - HTML Preprocessors

Haml is a templating engine for HTML. It's designed to make it both easier and more pleasant to write HTML documents, by eliminating redundancy, reflecting the underlying structure that the document represents, and providing an elegant syntax that's both powerful and easy to understand.

## Basic Usage

Haml can be used from the command line or as part of a Ruby web framework. The
first step is to install the gem:

~~~sh
gem install haml
~~~

After you write some Haml, you can run

~~~sh
haml document.haml
~~~

to compile it to HTML. For more information on these commands, check out

~~~sh
haml --help
~~~


## Formatting

The most basic element of Haml is a shorthand for creating HTML:

~~~haml
%tagname{:attr1 => 'value1', :attr2 => 'value2'} Contents
~~~

No end-tag is needed; Haml handles that automatically. If you prefer HTML-style
attributes, you can also use:

~~~haml
%tagname(attr1='value1' attr2='value2') Contents
~~~

Adding `class` and `id` attributes is even easier. Haml uses the same syntax as
the CSS that styles the document:

~~~haml
%tagname#id.class
~~~

In fact, when you're using the `<div>` tag, it becomes _even easier_. Because
`<div>` is such a common element, a tag without a name defaults to a div. So

~~~haml
#foo Hello!
~~~

becomes

~~~html
<div id='foo'>Hello!</div>
~~~