# AML Project : Grab AI Safety Challenge 
Project for ISSS610 Applied Machine Learning (AML) in SMU MITB. 
Group members: Chew Wen Wei, Geraldine Pang, Tan Woo Leong Benjamin, Yew Teik Kheng and Zhu WanYi

## Background
Given the telematics data for each Grab transport trip and the label if the trip is tagged as dangerous driving, derive a model that can detect dangerous driving trips.

## Project Status
- [x] Cleaning Data/ EDA + Document steps
- [ ] Everyone to think about Window/Rolling/Moving Average for the seconds data
- [ ] Ben & TK: Reading papers on similar studies
- [ ] WY/WW/GP: get Baseline model
- [ ] Feature Engineering
- [ ] Test with Models

## Pre-Requisite Downloads 
#### Safety Dataset 
Information about the challenge and the dataset can be found from (Grab AI website)[https://www.aiforsea.com/safety]. 
Dataset has been saved onto our shared OneDrive folder, under `/safety`. **Important:** Save it to your local repo under a `/data` folder.

#### Requirements 
See the `howto.md` file on how to activate your environment and install the packages that are needed.

## Project Structure 
1. docus folder
    - For documentation such as this `readme.md`, `howto.md` 
    - For cleaning documentation/reports? 
2. notebooks
    - to store out jupyter notebooks 
3. `.gitignore` 
    -  list of dir contents to be ignored when uploading to git.
    - Probably want to exclude our `.docx` and `.pptx` files later on; or just store them separately.
4. `requirements.txt` - list of packages that are used in this proj
5. data folder 
    - To store your data - PLEASE name it correctly! else it will be pushed to Gh and we really don't want that

