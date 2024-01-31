# robots.txt
A robots.txt that allows indexing for search crawlers, but disallows harmful AI training bots that can take your content for AI training without your consent (see [example](robots.txt)):

```
Sitemap: https://[your domain name here]/sitemap.xml
Sitemap: https://[your domain name here]/image-sitemap.xml

# Disallow data scraping and usage of website content for AI model training or prompting.
# Explicit opt-out from certain crawlers is not an invitation for others to train AI models on our content.
# Data scraping and model training must be opt-in, not opt-out.
# Demand consent, credit, and compensation.
# #CreateDontScrape

User-agent: GPTBot
Disallow: /

User-agent: CCBot
Disallow: /

User-agent: Google-Extended
Disallow: /

User-agent: ClaudeBot
Disallow: /

User-agent: *
Allow: /
Disallow: /[Anything to exclude from indexing]
Host: https://[your domain name here without a closing slash]
```

Edit the above and place on your website as https://[your domain name here]/robots.txt .

[Create an issue](https://github.com/jumpingrabbit/robots.txt/issues/new) if you think more bots need to be added.
