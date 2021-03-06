#CSS Trainings, Tips and Best Practices

This is the CSS training and best practices repository for Globant Mobile Studio. Here you'll find an index with snippets, comments, common practices, explanations, video tutorials and so much more.

{% include "./SUMMARY.md" %}

## Credits

This hadn't been possible without definitions and documentation from:

{% for resource in book.creditsExternalResources %}
**{{ resource.name }}** >> {{ resource.homepage }}  
{% endfor %}

## Resources

A list of usefull resources that will help you through this journey!

{% for resource in book.resources %}
* ### {{resource.name}}

    {{resource.description}}

    [Check it out]({{resource.link}})

{% endfor %}

## Authors

{% for author in book.authors %}
**{{ author.name }}** >> {{ author.email }}  
{% endfor %}

## Contributing

If you want to contribute just fork the repo, ```cp template/template-(snippet|doc).md [category]/awesome-(snippet
|doc).md``` and share the awesome :godmode:

For a contribution to be accepted there are three musts:

1. Codepen and gist link for snippets (on codepen.io just click on Share > Save as Github Gist)
1. No typos.
1. Be awesome.
