# vuepress-2-boilerplate-netlify-cms
Vuepress 2 Boilerplate with Netlify CMS
This boilerplate has had the neccessary ressources added to it for the use of GIT enabled Netlify CMS.

# Resources

[NetlifyCMS](https://www.netlifycms.org)

[Vuepress 2](https://v2.vuepress.vuejs.org)

[Vuepress 2 - Config Reference](https://v2.vuepress.vuejs.org/reference/default-theme/config.html#logo)

[Yarn Package Manager](https://yarnpkg.com/getting-started)

[Tutorial - Midstride](https://midstride.com/vuepress-netlify-cms-integration/)

[Sample Repo](https://github.com/andreliem/vuepress-netlify-cms)

[NetlifyCMS Configuration Options](https://www.netlifycms.org/docs/configuration-options/)

## Editorial Workflow

Publish Mode
By default, all entries created or edited in the Netlify CMS are committed directly into the main repository branch.

The publish_mode option allows you to enable "Editorial Workflow" mode for more control over the content publishing phases. All unpublished entries will be arranged in a board according to their status, and they can be further reviewed and edited before going live.

Note: Editorial workflow works with GitHub repositories, and support for GitLab and Bitbucket is in beta.

You can enable the Editorial Workflow with the following line in your Netlify CMS config.yml file:

```
# /admin/config.yml
publish_mode: editorial_workflow
From a technical perspective, the workflow translates editor UI actions into common Git commands:
```

Actions in Netlify UI	Perform these Git actions
Save draft	Commits to a new branch (named according to the pattern cms/collectionName/entrySlug), and opens a pull request
Edit draft	Pushes another commit to the draft branch/pull request
Approve and publish draft	Merges pull request and deletes branch
