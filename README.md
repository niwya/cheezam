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

You can then run the scripts from Jupyter Notebook, on Google Colab or directly from Visual Studio Code, for instance. Just make sure the virtual environment is actually used to run the code. 

___

### The datasetBuilder folder
#### The imageScraping folder
This folder contains the scripts to scrape and rename the images that I used to build the cheese dataset. If you do run the `image_scraper` script, the images will be downloaded in `/downloads/keyword` folder.

**Important:** to use the `image_scraper`, you will need to download a [chromedriver](https://chromedriver.chromium.org/downloads), whose version will depend on your version of Google Chrome. Please save the chromedriver in the `imageScraping` folder, under `chromedriver.exe`. The `image_scraper` script only supports scraping images in Google Images using the Google Chrome browser. 
 
#### The imageProcessing folder
This folder contains the scripts to preprocess the images that I used to build the cheese dataset.

___

#### The cheese_classifier file
This is the file that builds each model trained to classify cheeses. It contains four different models. At this time, there is no inference capabilities - just for training, testing and validation.

### External links
[Want to know more?](https://chloebenz.com/projects/cheezam/)

### Status
The code in this repo is currently **being refactored**. Not everything works together yet. 