---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
Hi,

I'm Kellan. I made my first website in 1994.  This is the lightly updated version.

I think a lot about software and leading engineering teams, complex systems, and engineering capacity for social change.  Lately I'm thinking more climate change and healthcare.  

I'm also coaching a handful of organizations who want more effective and higher impact engineering organizations.

Any of those topics interest you? [Get in touch](/about).

<h2>Recent notes on engineering leadership:</h2>

<ul class="post-link">
	 {%- for post in site.posts -%}
	 {%- if post.mlp != null %}
	 {% else %}
	<li>
		<a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }} <span class="post-meta">({{ post.date | date: "%b %-d" }})</span></a></li>
	{% endif %}
	{%- endfor -%}
</ul>

More [notes on engineering leadership](/notes)

<h2>A bit more about me:</h2>

Some people like talks I've given. Here is one on [building learning cultures](https://www.youtube.com/watch?v=a772VLZ4ot8), and another on [supporting women in engineering](https://www.youtube.com/watch?v=w4LExVkv4Pw).

I've been [blogging at Laughing Meme](http://laughingmeme.org/) since 2002, though not much these days.

I've been [pretty active on Twitter as @kellan](https://twitter.com/kellan) for a while now (#47).  Yes, I love it and hate it as much as you do. 

I'm on [LinkedIn: Kellan Elliott-McCrea](https://www.linkedin.com/in/kellanem/), but the abridged version is:

<h3> Currently </h3>

* Coaching executive leadership in technology startups for high impact. Building a technology leadership ecosystem centered on New York.

* Thinking about what comes next.

<h3> Previously </h3>

* SVP of [Blink Health](https://blinkhealth.com). Working to fix the affordability and accessibility of prescription medication in the US by overhauling the supply chain. Lead engineering, product and design.

* CTO of [Etsy](https://etsy.com). Built and led Etsy's famously generative and human centered engineering organization through IPO.

* Architect of [Flickr](https://flickr.com) (Yahoo). Social media doesn't have to be an exploitative hell hole. 


[My GitHub](https://github.com/kellan/) isn't very interesting, but if you're a web developer of a certain age, you can walk down memory lane with [MagpieRSS](https://github.com/kellan/magpierss). If that doesn't produce enough (deeply ambivalent) nostalgia, you could always revisit the [Oauth spec](https://tools.ietf.org/html/rfc5849) I helped author.


