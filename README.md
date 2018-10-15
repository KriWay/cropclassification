# cropclassification
This is a collection of scripts that can help to classify crops using Sentinel data.

## Installation manual

1. As google earth engine is used to get the Sentinel data for the classification, you will need a
google account that has google earth engine access enabled.
So go to https://earthengine.google.com/ and click "Sign up" at the top right if you haven't used
google earth engine yet.
Once you are signed up you should be able to visit https://code.earthengine.google.com/.

2. As the scripts are written in Python, you need to use a package manager to be able to install
the packages the scripts depend on. The rest of the installation manual assumes you use anaconda and
python 3.6+. The installer for anaconda can be found here: https://www.anaconda.com/download/.

If you need some more installation instructions, have a look here:
https://conda.io/docs/user-guide/install/index.html

3. Once you have anaconda installed, you can open an anaconda terminal window and follow the
following steps:

      1. Create and activate a new conda environment
      ```
	  conda create --name cropclassification python=3.6
      conda activate cropclassification
	  ```
      2. Install the dependencies for the crop classification scripts:
      ```
	  conda install -c conda-forge earthengine-api
	  conda install -c conda-forge google-api-python-client
	  conda install scikit-learn
	  conda install geopandas
	  ```
      3. I use spyder to edit my scripts. After installing geopandas Spyder doesn't seem to work
      anymore, but installing it in the new environment explicitly solves this. If you use another
      editor, you can use that of course.
      ```
	  conda install spyder
	  ```

4. When you want to download data from google earth engine, this data is placed on your google
drive. For the scripts to be able to download this data they scripts need (read-only) access to your
google drive. Follow the steps explained on the following page, but skip step 2 as it will be
installed already and using pip and conda together can break some things:
https://developers.google.com/drive/api/v3/quickstart/python.

5. You can now open the scripts in eg. spyder, and check out especially `marker_cropgroup.py` and
`global_settings.py`. You need to update those to match your environment, eg. set the paths as you
want them,...

6. Now run `marker_cropgroup.py` to start a crop classification...

## Sample data

Sample data can be downloaded from the following location. If you don't change the default paths in the scripts in needs to be put in the directory C:\temp\CropClassification\InputData
https://drive.google.com/open?id=1eN9cBcWyvM0msNMCD6nivcGuZfYyqV5q
