# GitHub Pages Setup

This project is designed to run as a static GitHub Pages website.

## 1. Create the repository

A suggested repository name is:

```text
car-mount-phone-holder-generator
```

Upload the **contents** of this project folder to the root of the repository.

`index.html` must remain in the repository root for the setup below.

## 2. Enable GitHub Pages

In the GitHub repository:

1. Open **Settings**.
2. Select **Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the `main` branch.
5. Select `/ (root)`.
6. Save.

After GitHub finishes publishing, the generator will be available at a URL similar to:

```text
https://YOUR-GITHUB-USERNAME.github.io/car-mount-phone-holder-generator/
```

## 3. Add the live URL to the repository

When the Pages site is working:

1. Open the repository's main page.
2. Edit the **About** section.
3. Add the GitHub Pages address as the **Website**.

You can also add the final URL to the README under **Live Generator**.

## 4. Social preview

Use a current project image carrying the **Car Mount Phone Holder Generator** branding if you add a GitHub social preview. Avoid older assets that contain the previous project name.


## 5. Updating the generator

Keep the current public application named:

```text
index.html
```

When a new version is released:

1. Replace `index.html` with the new stable version.
2. Update the displayed version number.
3. Add the changes to `CHANGELOG.md`.
4. Commit the update.

Git history provides version history, so old HTML versions do not need to remain in the repository root.

## 6. Optional releases

For major versions, GitHub Releases can be used to provide downloadable snapshots or ZIP archives while `index.html` always represents the current stable version.
