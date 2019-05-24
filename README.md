# nh3-mag-user-guide
Source code for the NH3 Mag WordPress site user guide.

# Deployement

This repos is supposed to be deployed using [GitHub Pages][1].

To do so, you need access to the **Settings** tab in the repo.

1. Go to the **Settings** tab
2. Scroll down to the **GitHub Pages** section
3. Under the **Source** param, click the select list and choose the **master branch** option
4. The page should reload and tell you that the site is being deployed
4. Under the **Theme Chooser** param, click the **Change theme** button, and be sure to select the **Cayman** theme
  > This is important as the site does not support any other theme

From now on, each time you push new commits to the `master` branch, GitHub will redeploy your site with GitHub Pages

# Add new documentation page

The documentation is structured in folders, each of them representing a page in the site.

Each page (folder) has the same structure :
* an `index.md` file that contains the Markdown for the content of the page
* an `img` folder that contains the image files used in the Markdown

To link to a page from another page, use a relative link to the page folder, **not the page's `index.md` file!**.

So, to link to the `index.md` file of the `categories` page folder, at the same level as the current `.md` file, one would need to write :

```md
[Gestion des catégories](./categories)
```

Thus, to create a new page, go to the folder that should get this new page, and...
* Create a new folder for this page _(it does not have to be the actual displayed name for the page)_
* Create a new `index.md` file in this new folder
* If necessary, create a new `img` folder in this new folder
* Write your Markdown in the new `index.md` file, referecing your images with a relative path to the `img` folder, like this :

  ```md
  ![](./img/loco-menu.png)
  ```

# Config files

The displayed title and description for the site are defined in the `_config.yml` file.

[1]: https://pages.github.com/
