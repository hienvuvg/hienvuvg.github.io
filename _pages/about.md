---
permalink: /
title: "Hien Vu"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

About
------
Text

Education
------
Text

Publications
------
- Hanwook Chung, Hien Vu, Younghyun Kim, and Christopher Choi, Subcutaneous temperature monitoring through ear tag for heat stress detection in dairy cows, Biosystems Engineering 2023 ([Link](https://www.sciencedirect.com/science/article/pii/S153751102300209X?via%3Dihub))

- Hien Vu, Hanwook Chung, Christopher Choi, and Younghyun Kim, eTag: An Energy-Neutral Ear Tag for Real-Time Body Temperature Monitoring of Dairy Cattle, MobiCom 2023 ([ACM Link](https://dl.acm.org/doi/10.1145/3570361.3613262)) ([Slides](https://drive.google.com/drive/folders/1_LsDmNXU9k3Lfi257sbmy3_jWMtwXUDQ))

- Hien Vu, Donghwa Shin, Simultaneous internal heating for balanced temperature and state-of-charge distribution in lithium-ion battery packs, Journal of Energy Storage, 2023 ([Link](https://www.sciencedirect.com/science/article/pii/S2352152X22025087?dgcid=author))

- NA Nguyen, H Vu, M Pedram, D Shin, An Attachable Battery–Supercapacitor Hybrid for Large Pulsed Load, IEEE Design & Test, 2022 ([Link](https://ieeexplore.ieee.org/document/9781313))

- Hien Vu and Donghwa Shin, Scheduled Pre-heating of Li-ion Battery Packs for Balanced Temperature and State-ofcharge Distribution, Energies MDPI 2020 ([Link](https://www.mdpi.com/1996-1073/13/9/2212))

- Hien Vu, Nhan Tran, Loan Pham-Nguyen and Huy-Dung Han, LQG Regulator for Control Moment Gyroscope based Balancing System, IEEE ICCE 2018 ([Link](https://ieeexplore.ieee.org/document/8465717))


Text

Getting started
======
1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Fork [this repository](https://github.com/academicpages/academicpages.github.io) by clicking the "fork" button in the top right. 
1. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and create content & metadata (see below -- also see [this set of diffs](http://archive.is/3TPas) showing what files were changed to set up [an example site](https://getorg-testacct.github.io) for a user with the username "getorg-testacct")
1. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section

Site-wide configuration
------
The main configuration file for the site is in the base directory in [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml), which defines the content in the sidebars and other site-wide features. You will need to replace the default variables with ones about yourself and your site's github repository. The configuration file for the top menu is in [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). For example, if you don't have a portfolio or blog posts, you can remove those items from that navigation.yml file to remove them from the header. 

Create content & metadata
------
For site content, there is one markdown file for each type of content, which are stored in directories like _publications, _talks, _posts, _teaching, or _pages. For example, each talk is a markdown file in the [_talks directory](https://github.com/academicpages/academicpages.github.io/tree/master/_talks). At the top of each markdown file is structured data in YAML about the talk, which the theme will parse to do lots of cool stuff. The same structured data about a talk is used to generate the list of talks on the [Talks page](https://academicpages.github.io/talks), each [individual page](https://academicpages.github.io/talks/2012-03-01-talk-1) for specific talks, the talks section for the [CV page](https://academicpages.github.io/cv), and the [map of places you've given a talk](https://academicpages.github.io/talkmap.html) (if you run this [python file](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py) or [Jupyter notebook](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb), which creates the HTML for the map based on the contents of the _talks directory).

**Markdown generator**

I have also created [a set of Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator
) that converts a CSV containing structured data about talks or presentations into individual markdown files that will be properly formatted for the academicpages template. The sample CSVs in that directory are the ones I used to create my own personal website at stuartgeiger.com. My usual workflow is that I keep a spreadsheet of my publications and talks, then run the code in these notebooks to generate the markdown files, then commit and push them to the GitHub repository.

How to edit your site's GitHub repository
------
Many people use a git client to create files on their local computer and then push them to GitHub's servers. If you are not familiar with git, you can directly edit these configuration and markdown files directly in the github.com interface. Navigate to a file (like [this one](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md) and click the pencil icon in the top right of the content preview (to the right of the "Raw | Blame | History" buttons). You can delete a file by clicking the trashcan icon to the right of the pencil icon. You can also create new files or upload files by navigating to a directory and clicking the "Create new file" or "Upload files" buttons. 

Example: editing a markdown file for a talk
![Editing a markdown file for a talk](/images/editing-talk.png)

For more info
------
More info about configuring academicpages can be found in [the guide](https://academicpages.github.io/markdown/). The [guides for the Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (which this theme was forked from) might also be helpful.
