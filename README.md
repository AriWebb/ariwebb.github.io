# Website Repo for ariwebb.com
Ari Webb

## Motivation:

I wanted to make this website so that I could have a place to share with the world a little bit about myself and my coding projects. I was inspired to build this by my friend James Qiu, you can find his website [here][james]. I encourage anyone looking at this to take a look at his website too!

## Codebase:

Putting together this website was super quick! It is hosted through [GitHub][github] and built using the [Jekyll][jekyll] and [minimal mistakes][mistakes] frameworks. Look at the three preceeding links to find more info. Feel free also to clone the repo to gain insight into what makes it work and how you can build your own!

## Testing:

One way to test in real time without having to constantly push to Github then wait for the build is as follows: (instructions in Linux shell)

1. Navigate to outermost directory.
2. Install ruby-dev (sudo apt install ruby-dev)
3. Bundle everything (sudo bundle install)
4. Serve the jekyll application: (bundle exec jekyll serve --incremental --watch)

You should then be able to access the website through localhost. The --incremental tag makes it so that the website only builds incrementally and --watch keeps a process running in the background that checks for changes. So, whenever you change any file it automatically rebuilds at localhost allowing rapid testing.

## Custom Domain:

The default domain name for your pages website takes the form of username.github.io. What if you want to change to a non-github domain? Follow these steps:

1. Choose a domain name. I went with ariwebb.com.
2. Purchase the domain name. I used [namecheap][namecheap].
3. Configure a new CNAME record through your DNS provider. If you used namecheap, instructions are [here][ncdns]
4. Create the custom domain through GitHub pages. Find general info about this [here][ghpcustom] and specific instructions [here][ghpins]

[james]: https://qiujames.github.io/
[github]: https://pages.github.com/
[jekyll]: https://jekyllrb.com/docs/
[mistakes]: https://mmistakes.github.io/minimal-mistakes/
[namecheap]: https://www.namecheap.com/
[ncdns]: https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages/
[ghpcustom]: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages
[ghpins]: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-a-subdomain
