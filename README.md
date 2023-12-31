# 2023 ADL HW1
Author: 栗漢文  r11922191 

## Training
1. Make sure the datas like train.json, valid.json and context.json are already locate in `./data/`
2. Train the Paragraph Selection and Span Selection model by:
   ``` shell
   sudo bash ./train.sh
   ```
   The train.sh contains three steps:
   * run PS_train.py to train a paragraph selection model
   * run preprocess.py to transfer data format into squad format, the new datas will be in `./preprocessed`
   * run QA_train.py to train a span selection model
      
   The hyper-parameters in train.sh can be modified  
   The model will locate in `./ckpt/PS` and `./ckpt/QA`

## Testing
1. Download the model I trained by:
   ``` shell
   sudo bash ./download.sh
   ```  
2. Test the model by:
   ``` shell
   sudo bash ./run.sh /path/to/context.json /path/to/test.json /path/to/pred/prediction.csv
   ```

## Others
1. QA_train_plot.py is the code I plot the loss and EM for Report Q3.  
2. QA_train_from_scratch.py is the code I train span selection model from scratch for Report Q4.

