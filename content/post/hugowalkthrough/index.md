---
title: "Portfolio Website Walkthrough"
description: "I made a video documenting how I created my website with Hugo."
date: 2023-08-12T02:36:09Z
image: hugothumbfinal.png
math: 
license: 
comments: true
draft: false
---

## Build a Portfolio Website with Hugo (for free)

I created this [portfolio website](jwcaterine.com) (the one you're looking at right now) for my freelance writing business and [documented the process](https://www.youtube.com/watch?v=6MKW4gzLItU) to teach other writers how to set up their own. This walkthrough is based on the [quickstart guide by theme author CaiJimmy](https://github.com/CaiJimmy/hugo-theme-stack-starter), but mine includes additional steps that may be helpful for users less experienced with programming. Note that if you choose a different theme, the set up will be different, so I’d recommend following this example first to learn the basics, and then you can explore other themes after.

{{< youtube 6MKW4gzLItU >}}

### What is Hugo?

This project uses [Hugo,](https://www.youtube.com/watch?v=0RKpf3rK57I) a static-site generator, “static” meaning that the elements on the webpage are the same for every user (versus “dynamic” where they change). To use Hugo, you select a [“Theme” from their website,](https://themes.gohugo.io/) and then you can customize the configurations and add posts as markdown files. It is a more affordable alternative to sites like Squarespace or Wordpress, but it does require some grit to set up and maintain.

You don’t need to be a veteran programmer in order to use Hugo. You do need a [GitHub account](https://docs.github.com/en/get-started/onboarding/getting-started-with-your-github-account) and optionally a custom domain. This is the only part that would cost money, but typically you can find something for less than $20 USD/year. I used [Netlify.](https://docs.netlify.com/domains-https/netlify-dns/domain-registration/)

### Step-by-step guide to launch website in less than an hour

1. Copy theme and set up GitHub pages - On the [“Stack” theme Github template,](https://github.com/CaiJimmy/hugo-theme-stack-starter) click the green “Use this template” button to clone the template as your own repository. Then, go to the settings tab of your new repository and click the “Pages” menu item on the sidebar. Under the “Branch” subheader, select “gh-pages” from the dropdown menu. (If you don’t see it immediately, wait a few minutes). Click “Save.” If you’re using a custom domain, you can enter that below and save also.
2. Launch Codespace - Click on the “Code” tab on the top, and then click the green “Code” button, and launch a new Codespace. This takes several minutes, but it will open a virtual coding environment in the cloud, so you don’t have to install anything on your local machine. Of course if you’d rather do that, it’s certainly an option.
3. Set up extensions and “baseurl” in config file - Go to the “Extensions” tab on the sidebar (building blocks icon) and search for “GitHub Actions.” Click the blue install button. Once the new icon appears on the sidebar, click that and make sure you’re signed in to your GitHub account so it syncs. Then, click the File Explorer tab (top-left), you can navigate to the “config.toml” file. At the top, change the link in the quotation marks next to “baseurl” to your domain. If you don’t have a custom domain, that will be “[yourgithubusername].github.io/[yourrepositoryname]”. Save the file.
4. Use Terminal to build website - if you don’t see a terminal window at the bottom of the screen, you can create a new one from the menu at the top left. Click to the right of the “$” sign and type “hugo” and hit enter. This essentially builds your website based on the changes you made.
5. Use Git to Launch Website - After you save, you should see a blue bubble with a number appear on one of the sidebar icons. Click it. This is where the [“Git” in “GitHub”](https://www.youtube.com/watch?v=hwP7WQkmECE) comes from - it’s a source control system, similar to how version history works if you’ve ever used that in Microsoft Word. In the box that says “Message” type in a short note to describe the changes you made, in this case something like “update baseurl” and then click the blue button that says “Commit.” Once that processes, click the blue button again to “Sync Changes.” Congrats, you can go to your domain to view your website!
6. Customize - now that your website is up, you can customize the profile picture and social media links by making changes to the “params.toml” and “menu.toml” file. To create a new post, in the terminal type “hugo new post/[yourpostname]/index.md”, and you will see the new folder and file appear under the “post” folder in your directory. You can modify the frontmatter at the top of your index.md file and [then write your post just like you would on Reddit](https://www.markdownguide.org/) under the dash marks. You can also embed social media posts and other things with [Hugo shortcodes.](https://gohugo.io/content-management/shortcodes/) Watch my video for more details on these steps.

That’s it! I hope this encourages some of you to give Hugo a try. Like I said before, you’ll need grit to solve problems that come up with your Hugo site, but fortunately there is documentation for most themes you can refer to. The themes are fairly basic and to do anything fancier would require more programming knowledge. I prefer a more minimalist look anyway, so it works for me. Good luck!