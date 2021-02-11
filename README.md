# OpenCV Introduction for 2.5D raster map processing


This repository is testing for Python 3.5+ although should still work for 2.7+.

To download files open terminal and browse to the folder you want to store the data using the `cd` command.

Clone the repository by typing: 

`git clone https://github.com/3Dimaging-ucl/ucl_cege0092`

Next move into the folder and open jupyter notebook with: 

```
cd ucl_cegeg075
jupyter notebook
```

Finally, open the file `opencv_practical.ipynb`. It is important you run `jupyter notebook` whilst in the `ucl_cege075` directory as otherwise the file paths will not work correctly.

## Running on Google Colab ##

This notebook can be run on google colab with a few minor alterations to avoid the need for setting up a local python environment. First navigate to [Google Colab](https://colab.research.google.com/). If you have not already, you will need to create a google account.

On the top bar navigate to `GITHUB` and enter the organization Upload GitHub Repo3Dimaging-ucl`. Open the file `opencv_practical.ipynb` under the `ucl_cege0092` respository. 

Next, run the following code cell at the top of the notebook:

`!git clone https://github.com/3Dimaging-ucl/ucl_cege0092 data`

Open the files tab (small arrow below CO logo in top left) and click `refresh` if you do not see the folder `data`. These are all the files required for the practical.

To enable the new file structure to work, you will need to append the string `data/` infront of any file paths. For example, `file = 'images/aerial_small.tif'` becomes `file = 'data/images/aerial_small.tif'`. 

The rest of the practical will now work as normal.

## Installing OpenCV on your own machine ##

Below are my recommendations for install OpenCV on your own machine. However, you should ***not*** attempt these if you already have a working python environment on your machine. Either remove your current installation, or use google to find the appropriate way to install OpenCV.

***Mac***

The easiest way to install OpenCV on a mac is through a package manager. There are two popular package managers for mac `HomeBrew` and `MacPorts`. Here we will show you how to install the required dependencies using `HomeBrew`.

If you have never done any programming on your mac you may need to first install xcode from the app store:
The open terminal and type:

```
sudo xcode-select --install
sudo xcodebuild -license
```

To install HomeBrew open your terminal and enter:

`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

Add HomeBrew to your path (here I use nano but you can use which ever command line text editor you like):

`nano ~/.bash_profile`

Append this text to the end of your file and save:

`export PATH=/usr/local/bin:$PATH`

To refesh your profile type:

`source ~/.bash_profile`

Next install a local version of python:

```
brew update
brew install python
```

Then we will install `pip` a python specific package installer:

```
curl -O http://python-distribute.org/distribute_setup.py
python distribute_setup.py
curl -O https://raw.github.com/pypa/pip/master/contrib/get-pip.py
python get-pip.py
```

Once we have pip we can install the required dependencies:

`pip install jupyter numpy opencv-python matplotlib`

To be able to clone the content from `github` as described above type:

`brew install git`



***Windows***

To install with windows and to programme in general with python on a windows machine I would recommend using [Anaconda](https://conda.io/docs/user-guide/install/windows.html). Follow the link and click the `Anaconda Installer for Windows` link. Then follow all the necessary steps.

Once Anaconda is installed you can open the `anaconda` prompt that will now be in your start menu. `pip` comes installed with Anaconda so you can go ahead and install the dependencies:

`pip install jupyter numpy opencv-python matplotlib`

Finally, to install git to allow us to clone the content:

`conda install git`
