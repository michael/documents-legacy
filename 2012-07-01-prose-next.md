We successfully launched Prose.io (0.1.0) on Monday last week. And the feedback was **really** good. :) After digging through the issues, and wrapping my head around future potential here's what could be worth investing time in next.

First off, the next release will be pretty straight forward. We're going to bring in support for organizations, and knock out most of the issues reported. Depending on my schedule I can see 0.2.0 (+ further patches) land next week.

Among them:

test

- Organizations of course (it's already implemented in Github.js 0.6.0, we just need a UI for it)
- Several edge cases with routing (e.g. dots within branch names)
- Easier access for listing repositories of users/organizations (not only from the startpage but also through routes)
  We want to have http://prose.io#developmentseed work as well as http://prose.io#dhcole. Also with the release of 0.2.0 we can leave out the branch, and get the contents of the default branch.
- Fixing issues regarding the YAML frontmatter. We want to get rid of most YAML parsing/serialization to overcome edgecases. YAML and JS are definitely not meant for each other. Not yet.

There are two major use-cases Prose covers (Content Management for websites, and well... Text File Management for Github repos in general) , each of which important on it's own and they don't rule each other out, which is really cool. So there's one simple rule I'm trying to follow during development. That is making the website management usecase a priority, but without giving up the generic interface. Most parts for this separation are already done. It's a matter of polishing and refining/easing configuration options, so we can ensure both, a non-technical content manager only sees the relevant Jekyll-related parts, and a more experienced Github user can browse any repository, without limitations. And even use it as a code editor.

Given that there's a lot of attention we get from the GitHub community (they're mostly excited about the generic usecase) we should consider pushing the general usecase forward too. We really might get substantial work back from the dev community.

Next Actions on the Website Content Management Side

- Better visual response for the filebrowser (Saman and I are considering using a list view instead of the matrix view 
- Better navigation (bring in search -> such as hitting t in the Github Filebrowser)
- Bring in commit messages


Next Actions for the general use-case

- Making it a code-editor as well. Edit HTML files etc. too, I see this as an extention for our publishing use-case. Cause the designer/developer might just want to make quickfixes on the live system, without doing the whole Git add/commit + push workflow.
- Syntax Highlighting (this is actually a no-brainer since CodeMirror supports a lot of formats)