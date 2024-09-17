## Usage 

Please download the weights by this link: [https://drive.google.com/file/d/1TgQyLShReeVxePQwR7LtO_hbqouEa-kN/view?usp=sharing](https://drive.google.com/file/d/1TgQyLShReeVxePQwR7LtO_hbqouEa-kN/view?usp=sharing), and put the weight named "last.ckpt" into the folder datacentric-baseline/weights/ You can build the container by running `bash build.sh`. 

## Testing

Use a python 3.10 based environment and install the requirements.txt file via `pip install -r requirements.txt`. 
Make sure model weights exist in `/weights`. Download the baseline weights by running `bash download_model_weights.sh`. 
Then run `predict.py` to create an expected_output mask. After that you can run `bash test.sh`. The test will 
only pass if your model is deterministic. For this repo you will need to disable test-time augmentation in the 
`process.py` file by setting `self.tta = False` in the init function. 

