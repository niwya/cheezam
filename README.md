# Cheezam
## A cheese classifier

___

### Download the dataset
Find the preprocessed 5-cheeses dataset [here](https://cheezam.s3.us-east-2.amazonaws.com/Cheezam_dataset.zip).

___

### How to use
0. Clone this repo. 
1. Create a virtual environment using `venv`.
2. Set up the virtual environments by installing all required packages using `pip install -r requirements.txt`. If you only want to check out the neural network, you can remove `google-images-download` from the `requirements.txt` file.

You can then run the scripts from Jupyter Notebook, on Google Colab or directly from Visual Studio Code (VSC), for instance. Just make sure the virtual environment is actually used to run the code. For this, you need to install `ipykernel` in your virtual environment (you can use `pip install ipykernel`), then install a new kernel with `ipython kernel install --user --name=whatever` (replace <whatever> by whatever name you want to give to your kernel). If you are using VSC, change the kernel used in the top right of the `.ipynb` file to the one you just created (you may need to restart VSC for it to automatically detect the new kernel). 

___

### The datasetBuilder folder
#### The image_scraper script
This folder contains the scripts to scrape and rename the images that I used to build the cheese dataset. If you do run the `image_scraper` script, the images will be downloaded in `/downloads/keyword` folder.

**Important:** to use the `image_scraper`, you will need to download a [chromedriver](https://chromedriver.chromium.org/downloads), whose version will depend on your version of Google Chrome. Please save the chromedriver in a location of your choice, add it to your PATH and modify the `chromedriver_path` in the file with the **absolute path** to your chromedriver. The `image_scraper` script only supports scraping images in Google Images using the Google Chrome browser. 
 
#### The file_renamer script
This folder contains the scripts to preprocess the images that I used to build the cheese dataset.

#### The preprocessing script
[TO COME]
___

### The cheese_classifier script
This is the script that builds each model trained to classify cheeses. It contains four different models. At this time, there is no inference capabilities - just for training, testing and validation.

### External links
[Want to know more?](https://chloebenz.com/projects/cheezam/)

### Status
The code in this repo is currently **being refactored**. Not everything works together yet. 