# 2023 ADL HW1
Author: 栗漢文  r11922191 

## Training
1. Make sure the datas like train.json, valid.json and context.json are already locate in `./data/`
2. Train the Paragraph Selection and Question Answering model by:
   ``` shell
   sudo bash ./train.sh
   ```
   The train.sh contains three steps:
   * run PS_train.py to train a paragraph selection model
   * run preprocess.py to transfer data format into squad format, the new datas will be in `./preprocessed`
   * run QA_train.py to train a question answering model
      
   The hyper-parameters in train.sh can be modified  
   The model will locate in `./ckpt/PS` and `./ckpt/QA`

## Testing
1. Download the model I trained by:
   ``` shell
   sudo bash ./download.sh
   ```  
3. Test the model by:
   ``` shell
   sudo bash ./run.sh /path/to/context.json /path/to/test.json /path/to/pred/prediction.csv
   ```  
