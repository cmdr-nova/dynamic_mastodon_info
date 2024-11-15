# dynamic_mastodon_info
Include JavaScript on your website that automatically updates your author name and an avatar image with whatever your Mastodon account is using!

How to get this to work:

Save both JavaScript files into a directory on your website. Make sure to include this in the head:
```
<script src="/path/to/dynamic-avatar.js"></script>
<script src="/path/to/dynamic-author.js"></script>
```
Be sure to replace this section at the top of each script with whatever your Mastodon profile is.
```
https://your.mastodon.profile
```

Then, let's say you're writing blog posts on your site, and you want these elements to update automatically with whatever it says on your Mastodon profile, *even if you change it* (elminating the need to update a bunch of things, taking up sweet, sweet time).

Include "dynamic-avatar" as a class on an IMG element, and include "author-link" as a class in an <a> tag.

Example:
```
<img class="dynamic-avatar no-center pack-avatar" src="https://mkultra.monster/system/accounts/avatars/111/939/142/189/797/780/original/f0c02ed45a83472f.png" height="100" width="100">
Author: <a id="author-link" href="https://mkultra.monster/@cmdr_nova" target="_blank">{{ page.author }}</a>
```
(the liquid isn't necessary, this is just part of Jekyll making calls to the front matter of a post, which I'm overriding)

And voila! Now your avatar and author name will update automatically on your website *any time you change them on Mastodon.*
