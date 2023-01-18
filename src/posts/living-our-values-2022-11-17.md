---
title: "Living our values: building a sustainable website for ourselves"
metaTitle: "Living our values: building a sustainable website for ourselves"
metaDesc: How Tech Works For Us chose a tech static and content that would keep
  our environmental impact to an absolute minimum
date: 2023-01-18T16:51:00.220Z
tags:
  - sustainable-web
  - blog
---
![A screenshot from the Website Carbon checker that says "Hurrah! This web page is cleaner than 98% of web pages tested"](/images/webcarbonresult2.png "Results for our website from the Website Carbon checker ")

Creating the website for Tech Works For Us (TWFU) was both an opportunity and a challenge. We knew that if we were going to make a lot of noise about our "planet-centred" values and sustainable digital technology, then we were going to have to live up to these principles when choosing hosting, web technologies and content. To this end, we enlisted digital expert and consultant Kim Plowright to investigate our options in this area and build the tech stack and the core website. The below is an outline of what we discovered, and the choices we made as a result.

It is worth saying that sustainable web design is a fairly new area of practice, and whilst we are not alone in thinking about this (many others go before us, as you will see, in particular we valued the work of Tom Greenwood, author of [Sustainable Web Design](https://abookapart.com/products/sustainable-web-design) and founder of [Wholegrain Digital](https://www.wholegraindigital.com) there is little in the way of standards to look to for guidance or good examples to follow and copy. We also found that many providers of web services and platforms provide no information about their environmental impact or ethical practices, which makes it very hard to evaluate them against our ideals. Our goal, ultimately, is to find or develop a robust rubric that we can use for this evaluation process, but in the meantime we simply tried to do the best we could with the information that we had.

To minimise carbon emissions from web traffic on the site, we needed to create pages that were not making high demands on the server or the user's computer. It is common for websites to be constantly making calls back to the server to dynamically create pages, or to serve content, or to the browser to download fonts or render pages for example. Since the TWFU pages are largely informational and won't change often, there was really no need for this. We also wanted a fairly simple system that would be easy to learn without investing a huge amount of time and effort, not least because ideally we'd like to be able to suggest a similar system to clients as well. 

We decided early on that we would probably want a "tech stack" (the combination of software or services used to develop, deploy and display a website) that spat out flat html at the end (just like in the olden days of the web!). This static and unchanging html file is also cached, so that it doesn't need to be downloaded again on each visit. We went for [Eleventy](https://www.11ty.dev), because it is simple, has a strong open source community, very flexible templating, and would work well across our mix of PC and Mac. We adapted a nice straightforward starter theme called [Hylia](https://hylia.website) that seemed to fit the bill (it doesn't include complicated JavaScript frameworks, and includes a dark theme, which should be lower impact as well). Pages created in Eleventy go into our Github repository, which is linked to Netlify, the service that puts it online (in an entirely automated workflow). Netlify also has a very simple CMS that can be used to create and edit new pages and modules within them. 

We also thought about the energy used by the servers: were they running on sustainable, carbon neutral energy? You can find out more about the [sustainability of cloud providers in this excellent article from Wired.](https://www.wired.com/story/amazon-google-microsoft-green-clouds-and-hyperscale-data-centers/) We've favoured platforms that use Microsoft or Google Cloud hosting, as both these companies run carbon neutral servers. Some elements of Netlify may run on Amazon's AWS, which is less sustainable; this is not ideal, and we'll keep monitoring our choice to see if we can do better. 

In terms of content, we have avoided large images, using compression and dithering to keep file sizes tiny, and the background leaf in our theme is a teeny SVG file (we'll share a bit more about this process in future). Currently we have no video and would only use that in very specific and sparing circumstances.

So theoretically, all very lightweight, but does it achieve our low carbon aims? We ran it through the Website Carbon checker, and were pretty pleased with [the results which you can view yourself here](https://www.websitecarbon.com/website/tech-works-for-us-netlify-app/). We also needed to make sure it met accessibility standards, so ran it through [Lighthouse](https://developer.chrome.com/docs/lighthouse/overview/), results below.

![A screenshot from the Lighthouse developer report for this website that shows 100% scores for performance, best practices and SEO, and 97% for accessibility](/images/lighthousescores2.png "A screenshot from the Lighthouse developer report for this website")

As you can see it is a near perfect score, but the accessibility could be improved by increasing the colour contrast between the brand orange and other colours, so we are going to tweak that soon.

A good start for us. We still need to review other areas of technology that we use, however, such as our email systems, social media, apps and services. And we continue to look into options that are likely to be more relevant to our clients. Keep an eye on this blog where we will continue to share what we find.

Written by Martha Henson with additions from Kim Plowright (thank you Kim!)