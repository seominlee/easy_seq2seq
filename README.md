# A chatbot model based on tensorflow supporting utf8

I just added utf8 support code. (https://github.com/llSourcell/tensorflow_chatbot).
Oringinal codes came from suriyadeepan (https://github.com/suriyadeepan/easy_seq2seq).







------------------------------------------------------------
# easy\_seq2seq

An implementation of Seq2Seq that actually works. I want to make it easy for people to train their own seq2seq model with any corpus. I am also adding the parameters of my trained model for people to just use it without training. If you have a model that works share your model params here, as external link or do a pull request. I have used Cornell Movie Dialog Corpus to train my model. A link to preprocessed data and scripts for preprocessing can be found in this repo.

*Have Fun!*

## Update 1.1.2017


I have created another repository - [practical_seq2seq](https://github.com/suriyadeepan/practical_seq2seq) to experiment with the seq2seq model. The new model trained on Twitter chat log and Cornell Movie Dialog corpus performs well. I wrote an article - [Practical seq2seq](http://suriyadeepan.github.io/2016-12-31-practical-seq2seq/), explaining the code.

Happy New Year, **2017**


## Setup


* Create temporary working directory prior to training

```bash
mkdir working_dir
```

* Download test/train data from Cornell Movie Dialog Corpus

```bash
cd data/
bash pull_data.sh
```

## Training

```bash
# edit seq2seq.ini file to set 
#		mode = train
python execute.py
# or use custom ini file
#		python execute.py my_custom_conf.ini
```

## Testing

```bash
# edit seq2seq.ini file to set 
#		mode = test
python execute.py
```

## Serve

```bash
# configuration : seq2seq_serve.ini
python ui/app.py
# wait until this message shows up
#		"Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)"
# open up the address in browser, chat with the bot
```
