[Prose](http://prose.io) is not only suitable for managing website content. You can use it as a full-featured writing environment too. It provides you a distraction-free writing experience, with a focus on content and structure. Also, you can share your work at any time or invite other people to collaborate on your document. 

Here's what you need to get started.

### Create a new Github Repository

This will be the home of your documents. Make sure there's at least one branch available. The easiest way to do it, is by initializing a new GitHub Repository. Keep in mind, this is a plain old GitHub repository, there's no need for setting up Jekyll.

{screenshot new repo on github}


### Start writing

Open your fresh repository in prose and start writing your first document. To do so, click on "New File" enter some text in markdown. And hit save.

{screenshot hello world}

## Remember every change

Only changes are stored on every save. Thanks to git you can access older versions of your document using [GitHub](https://github.com/prose/documents/commits/master). In future we'll allow you to access them right within Prose. Just give us some more time please. :)

{screenshot to git Changeset}


### Invite collaborators

If your co-workers haven't created a Github Account yet. Now they have a new reason. Permissions are totally transparent to Github. So what you need to do is 
Let others collaborate.

{screenshot to invite collaborators}

### Share your work

Make sure your repository is public and just share the URL of the post. Readers will always see the most up to date version. So if you or some of your collaborators makes a change, it will immediately be visible. Just point them to the appropriate URL for either editing, or viewing the document.

- `http://prose.io/#prose/documents/blob/master/articles/hello-world.md`
- `http://prose.io/#prose/documents/edit/master/articles/hello-world.md`



### Turn it into a website

Remember that you always have the option to turn your document repository in a Jekyll website. However before creating a website, you should write some content. :)

(screenshot for copy and pasting the URL)

### Organize your posts in folders

Add a new folder directly within Prose. 

{screenshot}

## Properties

- Prose is closely tied to GitHub. We intentionally made the process transparent, and expose git concepts such as branches, folders and files. You can access every file either with Prose or the Github User interface. So you can mix your workflow by editing in your local text editor and use the regular git commit/push workflow along with Prose.


## Future outlook

- Accessing revision history through the interface
- allow assigning permissions to repos (aka invite new writer)