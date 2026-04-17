---
layout: post
title:  "github pages"
---

## GitHub Pages


## Building your site locally
source: [Testing your GitHub Pages site locally with Jekyll](https://docs.github.com/api/article/body?pathname=/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll)


1. Open <span class="platform-mac">Terminal</span><span class="platform-linux">Terminal</span><span class="platform-windows">Git Bash</span>.

2. Navigate to the publishing source for your site. For more information, see [Configuring a publishing source for your GitHub Pages site](/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

3. Run `bundle install`.

4. Run your Jekyll site locally.

   ```shell
   $ bundle exec jekyll serve
   > Configuration file: /Users/octocat/my-site/_config.yml
   >   ... ... ...
   >    Server address: http://127.0.0.1:4000/
   >  Server running... press ctrl-c to stop.
   ```

   > \[!NOTE]
   >
   > * If you've installed Ruby 3.0 or later (which you may have if you installed the default version via Homebrew), you might get an error at this step. That's because these versions of Ruby no longer come with `webrick` installed.
       >
       >   To fix the error, try running `bundle add webrick`, then re-running `bundle exec jekyll serve`.
   >
   > * If your `_config.yml` file's `baseurl` field contains your GitHub repository's link, you can use the following command when building locally to ignore that value and serve the site on `localhost:4000/`:
       >
       >   ```shell
   >   bundle exec jekyll serve --baseurl=""
   >   ```

5. To preview your site, in your web browser, navigate to `http://localhost:4000`.

## Updating the GitHub Pages gem

> \[!NOTE] While the `github-pages` gem remains supported for some workflows, GitHub Actions is now the recommended approach for deploying and automating GitHub Pages sites.

Jekyll is an active open source project that is updated frequently. If the `github-pages` gem on your computer is out of date with the `github-pages` gem on the GitHub Pages server, your site may look different when built locally than when published on GitHub. To avoid this, regularly update the `github-pages` gem on your computer.

1. Open <span class="platform-mac">Terminal</span><span class="platform-linux">Terminal</span><span class="platform-windows">Git Bash</span>.
2. Update the `github-pages` gem.
    * If you installed Bundler, run `bundle update github-pages`.
    * If you don't have Bundler installed, run `gem update github-pages`.


