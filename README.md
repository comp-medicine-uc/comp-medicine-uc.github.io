# Computational Medicine Group @ PUC website

Welcome to the website for our lab!

## For group members

These are instructions on how to contribute to the website.

1. To add a paper, include it in BibTeX in `_bibliography/papers.bib`. Be sure to include the `website` and `abstract` fields correctly for them to show up on the website. If you want, you can add a `code` field that links to the associated repo, and a `preview` field to an image or GIF file that will appear as a thumbnail to the paper. To add a preview file, upload it onto `assets/img/publication_preview/`.

2. To update your data, edit the `_data/members.yml` file. This is a YAML format file that contains the information presented in the website. Simply type in the relevant information into the respective field. To add a profile picture, upload the respective image file to `assets/img/`.

3. To update project or course pages, simply edit the respective Markdown file in `_projects/` or `_courses/`. The Markdown format here, as in many other places, allows for HTML tags. For more details on how that can be used to edit a page, check out an [example in the original al-folio theme repo](https://github.com/alshedivat/al-folio/blob/master/_projects/1_project.md?plain=1). Projects and courses also support image files, that should be uploaded to `assets/img/`.

## License

This website uses the [**al-folio theme**](https://github.com/alshedivat/al-folio), and its modification used by the [UCSF Decision Lab website](https://github.com/winstonchiong/decisionlabucsf.github.io). Originally, **al-folio** was based on the [\*folio theme](https://github.com/bogoli/-folio) (published by [Lia Bogoev](https://liabogoev.com) and under the MIT license).
Since then, it got a full re-write of the styles and many additional cool features.
