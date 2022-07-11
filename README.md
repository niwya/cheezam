# Cheezam
## A cheese classifier

___

### Download the dataset
Find the preprocessed 5-cheeses dataset [here](https://cheezam.s3.us-east-2.amazonaws.com/Cheezam_dataset.zip). All images are in 256 by 256 pixels `png` format. 

___

### How to use
0. Clone this repo. 
1. Create a virtual environment using `venv`.
2. Set up the virtual environments by installing all required packages using `pip install -r requirements.txt`. If you only want to check out the neural network, you can remove `google-images-download` from the `requirements.txt` file.

You can then run the scripts from Jupyter Notebook, on Google Colab or directly from Visual Studio Code (VSC), for instance. Just make sure the virtual environment is actually used to run the code. For this, you need to install `ipykernel` in your virtual environment (you can use `pip install ipykernel`), then install a new kernel with `ipython kernel install --user --name=whatever` (replace <whatever> by whatever name you want to give to your kernel). If you are using VSC, change the kernel used in the top right of the `.ipynb` file to the one you just created (you may need to restart VSC for it to automatically detect the new kernel). 

___

### The datasetBuilder folder
#### The image_scraper script
This folder contains the scripts to scrape and rename the images that I used to build the cheese dataset. If you do run the `image_scraper` script with a query for *keyword*, the images will be downloaded in `./downloads/keyword` folder. 

**Important:** to use the `image_scraper`, you will need to download a [chromedriver](https://chromedriver.chromium.org/downloads), whose version will depend on your version of Google Chrome. Please save the chromedriver in a location of your choice, add it to your PATH and modify the `chromedriver_path` in the file with the **absolute path** to your chromedriver. The `image_scraper` script only supports scraping images in Google Images using the Google Chrome browser. 

**Important 2:** at this time, there are issues with the downloading process and the google-images-download package. This might be because the Chrome browser has changed how it handles image queries. Please refer directly to the package documentation. 
 
#### The file_renamer script
This folder contains the scripts to preprocess the images that I used to build the cheese dataset. It just renames all the files in a folder with the template `prefix_number` with `prefix` a prefix of choice and `number` the number of the image in the folder starting from 0.

#### The preprocessing script
This script lets you choose a provenance folder, and preprocess all desired subfolder in that provenance folder, then save it to some destination folder of your choice, such that:
- Processed images are in `png` format
- Processed images are 256 by 256 pixels
To enforce these bullet points, the initial images are cropped and resized. It is assumed that the images in the provenance folder have their object of interest centered in the frame, so that the cropping operations yields good results. 
___

### The cheese_classifier script
This is the script that builds each model trained to classify cheeses. It contains four different models. At this time, there is no inference capabilities - just for training, testing and validation.

### External links
[Want to know more?](https://chloebenz.com/projects/cheezam/)

### Status
The code in this repo is currently **being refactored**. Not everything works together yet. 