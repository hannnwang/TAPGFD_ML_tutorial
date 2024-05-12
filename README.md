# TAPGFD_ML_tutorial

Tutorial material for the ICTS TAGFD program (https://www.icts.res.in/program/TAPGFD). 

Step zero is that you need the data. I've been lazy and just uploaded the pack onto a Google Drive, which you can access [here](https://drive.google.com/drive/folders/1JJ0cpshu6-JE8wp93UsHuqy6V33rQy7s?usp=sharing). You'll need to download the whole pack for the above, see picture below.

![Google Drive pointer](https://i.imgur.com/QLpt4MM.png)

There there are at least three known ways of running these:

1) On your computer, `git clone` this repository, then in the load data part, point to where your data folder is (or move the data to where the notebook folder is going to live). Then you can do `git pull` you get updates (if any). You may or may not want to fork the repository (need a GitHub account), then you can in principle contribute material too!

2) On your computer, by downloading the pack (there should be a green "code" button near the top right of this page, click it and there should be "download"). Point to data as above.

3) Via Google colab, but you will need to pull copies (code and data) to your own Google drive, otherwise changes are not saved. Clicking the icon below will open a temporary Colab instance; there should be a "copy to drive button" near "file" near the top left for copying to drive.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/julianmak/TAPGFD_ML_tutorial/blob/main/) (requires Google login)

Then we need to mount the drive and point to the data, something like

```
from google.colab import drive
drive.mount('/content/drive')
data = xr.open_zarr("/path/to/folder/GLOB_HOMOGENEOUS_variables.zarr/")
```