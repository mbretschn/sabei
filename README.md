I try to build a traineddata model for a dot matrix font with custom box data.
The pictures only contain numbers and were taken with a Raspicam. 
I set the value for DPI to 600.

Am example for a single image 

![imagedata](https://github.com/3epnm/sabei/blob/master/09.png "imagedata")

Boxdata
```
0 37 26 132 159 0
9 166 29 261 162 0
```

.gt.txt (i tried also without a blank between the numbers
```
0 9
```

I had no success building traineddata which can recognize the image shown above. 
I wonder, if it is even possible to create traineddata for the given images.

In the following the output of `make training`

```
> make training 
find data/sabei-ground-truth -name '*.gt.txt' | xargs cat | sort | uniq > "data/sabei/all-gt"
unicharset_extractor --output_unicharset "data/sabei/unicharset" --norm_mode 2 "data/sabei/all-gt"
Bad box coordinates in boxfile string! 23171014343530070829312213062132042527261519002033030116241109021205283618
Extracting unicharset from plain text file data/sabei/all-gt
Wrote unicharset file data/sabei/unicharset
+ tesseract data/sabei-ground-truth/23.png data/sabei-ground-truth/23 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/17.png data/sabei-ground-truth/17 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/10.png data/sabei-ground-truth/10 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/14.png data/sabei-ground-truth/14 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/34.png data/sabei-ground-truth/34 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/35.png data/sabei-ground-truth/35 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/30.png data/sabei-ground-truth/30 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/07.png data/sabei-ground-truth/07 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/08.png data/sabei-ground-truth/08 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/29.png data/sabei-ground-truth/29 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/31.png data/sabei-ground-truth/31 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/22.png data/sabei-ground-truth/22 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/13.png data/sabei-ground-truth/13 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/06.png data/sabei-ground-truth/06 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/21.png data/sabei-ground-truth/21 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/32.png data/sabei-ground-truth/32 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/04.png data/sabei-ground-truth/04 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/25.png data/sabei-ground-truth/25 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/27.png data/sabei-ground-truth/27 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/26.png data/sabei-ground-truth/26 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/15.png data/sabei-ground-truth/15 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/19.png data/sabei-ground-truth/19 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/00.png data/sabei-ground-truth/00 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/20.png data/sabei-ground-truth/20 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/33.png data/sabei-ground-truth/33 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/03.png data/sabei-ground-truth/03 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/01.png data/sabei-ground-truth/01 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/16.png data/sabei-ground-truth/16 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/24.png data/sabei-ground-truth/24 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/11.png data/sabei-ground-truth/11 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/09.png data/sabei-ground-truth/09 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/02.png data/sabei-ground-truth/02 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/12.png data/sabei-ground-truth/12 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/05.png data/sabei-ground-truth/05 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/28.png data/sabei-ground-truth/28 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/36.png data/sabei-ground-truth/36 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
+ tesseract data/sabei-ground-truth/18.png data/sabei-ground-truth/18 --psm 13 lstm.train
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
find data/sabei-ground-truth -name '*.lstmf' | python3 shuffle.py 0 > "data/sabei/all-lstmf"
+ head -n 33 data/sabei/all-lstmf
+ tail -n 4 data/sabei/all-lstmf
wget -Odata/radical-stroke.txt 'https://github.com/tesseract-ocr/langdata_lstm/raw/master/radical-stroke.txt'
--2020-08-14 13:33:13--  https://github.com/tesseract-ocr/langdata_lstm/raw/master/radical-stroke.txt
Resolving github.com (github.com)... 140.82.118.3
Connecting to github.com (github.com)|140.82.118.3|:443... connected.
HTTP request sent, awaiting response... 302 Found
Location: https://raw.githubusercontent.com/tesseract-ocr/langdata_lstm/master/radical-stroke.txt [following]
--2020-08-14 13:33:13--  https://raw.githubusercontent.com/tesseract-ocr/langdata_lstm/master/radical-stroke.txt
Resolving raw.githubusercontent.com (raw.githubusercontent.com)... 151.101.112.133
Connecting to raw.githubusercontent.com (raw.githubusercontent.com)|151.101.112.133|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 330874 (323K) [text/plain]
Saving to: 'data/radical-stroke.txt'

     0K .......... .......... .......... .......... .......... 15% 1.24M 0s
    50K .......... .......... .......... .......... .......... 30% 1.40M 0s
   100K .......... .......... .......... .......... .......... 46% 2.05M 0s
   150K .......... .......... .......... .......... .......... 61% 2.60M 0s
   200K .......... .......... .......... .......... .......... 77% 4.68M 0s
   250K .......... .......... .......... .......... .......... 92% 1.54M 0s
   300K .......... .......... ...                             100% 1.74M=0.2s

2020-08-14 13:33:14 (1.84 MB/s) - 'data/radical-stroke.txt' saved [330874/330874]

combine_lang_model \
  --input_unicharset data/sabei/unicharset \
  --script_dir data \
  --numbers data/sabei/sabei.numbers \
  --puncs data/sabei/sabei.punc \
  --words data/sabei/sabei.wordlist \
  --output_dir data \
   \
  --lang sabei
Failed to read data from: data/sabei/sabei.wordlist
Failed to read data from: data/sabei/sabei.punc
Failed to read data from: data/sabei/sabei.numbers
Loaded unicharset of size 13 from file data/sabei/unicharset
Setting unichar properties
Setting script properties
Failed to load script unicharset from:data/Latin.unicharset
Warning: properties incomplete for index 3 = 2
Warning: properties incomplete for index 4 = 3
Warning: properties incomplete for index 5 = 1
Warning: properties incomplete for index 6 = 7
Warning: properties incomplete for index 7 = 0
Warning: properties incomplete for index 8 = 4
Warning: properties incomplete for index 9 = 5
Warning: properties incomplete for index 10 = 8
Warning: properties incomplete for index 11 = 9
Warning: properties incomplete for index 12 = 6
Config file is optional, continuing...
Failed to read data from: data/sabei/sabei.config
Null char=2
lstmtraining \
  --debug_interval 0 \
  --traineddata data/sabei/sabei.traineddata \
  --learning_rate 0.002 \
  --net_spec "[1,36,0,1 Ct3,3,16 Mp3,3 Lfys48 Lfx96 Lrx96 Lfx256 O1c`head -n1 data/sabei/unicharset`]" \
  --model_output data/sabei/checkpoints/sabei \
  --train_listfile data/sabei/list.train \
  --eval_listfile data/sabei/list.eval \
  --max_iterations 10000 \
  --target_error_rate 0.01
Warning: given outputs 13 not equal to unicharset of 12.
Num outputs,weights in Series:
  1,36,0,1:1, 0
Num outputs,weights in Series:
  C3,3:9, 0
  Ft16:16, 160
Total weights = 160
  [C3,3Ft16]:16, 160
  Mp3,3:16, 0
  Lfys48:48, 12480
  Lfx96:96, 55680
  Lrx96:96, 74112
  Lfx256:256, 361472
  Fc12:12, 3084
Total weights = 506988
Built network:[1,36,0,1[C3,3Ft16]Mp3,3Lfys48Lfx96Lrx96Lfx256Fc12] from request [1,36,0,1 Ct3,3,16 Mp3,3 Lfys48 Lfx96 Lrx96 Lfx256 O1c13]
Training parameters:
  Debug interval = 0, weights = 0.1, learning rate = 0.002, momentum=0.5
null char=11
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/30.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/25.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/17.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/15.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/18.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/02.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/21.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/09.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/28.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/36.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/16.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/20.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/31.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/35.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/19.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/14.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/22.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/34.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/24.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/10.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/33.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/29.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/11.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/32.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/01.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/08.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/06.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/12.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/26.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/07.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/00.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/27.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/03.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/04.lstmf
Loaded 1/1 lines (1-1) of document data/sabei-ground-truth/13.lstmf
At iteration 14/100/100, Mean rms=11.122%, delta=1.842%, char train=120.5%, word train=100%, skip ratio=0%,  New worst char error = 120.5 wrote checkpoint.

At iteration 88/200/200, Mean rms=10.953%, delta=4.947%, char train=118.25%, word train=100%, skip ratio=0%,  New worst char error = 118.25 wrote checkpoint.

At iteration 173/300/300, Mean rms=10.82%, delta=6.842%, char train=116.667%, word train=99.333%, skip ratio=0%,  New worst char error = 116.667 wrote checkpoint.

At iteration 267/400/400, Mean rms=10.482%, delta=8.737%, char train=113.25%, word train=95.5%, skip ratio=0%,  New worst char error = 113.25 wrote checkpoint.

At iteration 352/500/500, Mean rms=9.935%, delta=8.895%, char train=107.7%, word train=92.4%, skip ratio=0%,  New worst char error = 107.7 wrote checkpoint.

At iteration 427/600/600, Mean rms=9.388%, delta=8.825%, char train=101.167%, word train=88.333%, skip ratio=0%,  New worst char error = 101.167 wrote checkpoint.

2 Percent improvement time=501, best error was 100 @ 0
At iteration 501/700/700, Mean rms=9.012%, delta=8.857%, char train=96.714%, word train=85%, skip ratio=0%,  New best char error = 96.714 wrote checkpoint.

2 Percent improvement time=58, best error was 96.714 @ 501
At iteration 559/800/800, Mean rms=8.519%, delta=8.329%, char train=90.5%, word train=80%, skip ratio=0%,  New best char error = 90.5 wrote checkpoint.

2 Percent improvement time=59, best error was 90.5 @ 559
At iteration 618/900/900, Mean rms=8.131%, delta=8.094%, char train=85.889%, word train=76.333%, skip ratio=0%,  New best char error = 85.889 wrote checkpoint.

2 Percent improvement time=67, best error was 85.889 @ 618
At iteration 685/1000/1000, Mean rms=7.894%, delta=7.947%, char train=82.15%, word train=73.8%, skip ratio=0%,  New best char error = 82.15 wrote checkpoint.

2 Percent improvement time=49, best error was 82.15 @ 685
At iteration 734/1100/1100, Mean rms=7.236%, delta=8.305%, char train=73.5%, word train=67.2%, skip ratio=0%,  New best char error = 73.5 wrote checkpoint.

2 Percent improvement time=37, best error was 73.5 @ 734
At iteration 771/1200/1200, Mean rms=6.504%, delta=7.858%, char train=64.35%, word train=59.7%, skip ratio=0%,  New best char error = 64.35 wrote best model:data/sabei/checkpoints/sabei64.35_771.checkpoint wrote checkpoint.

2 Percent improvement time=23, best error was 64.35 @ 771
At iteration 794/1300/1300, Mean rms=5.71%, delta=7.037%, char train=54.55%, word train=51.5%, skip ratio=0%,  New best char error = 54.55 wrote best model:data/sabei/checkpoints/sabei54.55_794.checkpoint wrote checkpoint.

2 Percent improvement time=19, best error was 54.55 @ 794
At iteration 813/1400/1400, Mean rms=5.021%, delta=5.874%, char train=45.75%, word train=44.7%, skip ratio=0%,  New best char error = 45.75 wrote best model:data/sabei/checkpoints/sabei45.75_813.checkpoint wrote checkpoint.

2 Percent improvement time=35, best error was 45.75 @ 813
At iteration 848/1500/1500, Mean rms=4.589%, delta=5.258%, char train=40.05%, word train=39.5%, skip ratio=0%,  New best char error = 40.05 wrote best model:data/sabei/checkpoints/sabei40.05_848.checkpoint wrote checkpoint.

2 Percent improvement time=9, best error was 40.05 @ 848
At iteration 857/1600/1600, Mean rms=4.105%, delta=4.495%, char train=33.6%, word train=33.1%, skip ratio=0%,  New best char error = 33.6 wrote best model:data/sabei/checkpoints/sabei33.6_857.checkpoint wrote checkpoint.

2 Percent improvement time=3, best error was 33.6 @ 857
At iteration 860/1700/1700, Mean rms=3.537%, delta=3.626%, char train=26.8%, word train=26.8%, skip ratio=0%,  New best char error = 26.8 wrote best model:data/sabei/checkpoints/sabei26.8_860.checkpoint wrote checkpoint.

2 Percent improvement time=0, best error was 26.8 @ 860
At iteration 860/1800/1800, Mean rms=3.07%, delta=3.163%, char train=22.1%, word train=22.3%, skip ratio=0%,  New best char error = 22.1 wrote best model:data/sabei/checkpoints/sabei22.1_860.checkpoint wrote checkpoint.

2 Percent improvement time=0, best error was 22.1 @ 860
At iteration 860/1900/1900, Mean rms=2.593%, delta=2.542%, char train=17.2%, word train=17.6%, skip ratio=0%,  New best char error = 17.2 wrote best model:data/sabei/checkpoints/sabei17.2_860.checkpoint wrote checkpoint.

2 Percent improvement time=0, best error was 17.2 @ 860
At iteration 860/2000/2000, Mean rms=2.039%, delta=1.879%, char train=12.35%, word train=12.5%, skip ratio=0%,  New best char error = 12.35 wrote best model:data/sabei/checkpoints/sabei12.35_860.checkpoint wrote checkpoint.

2 Percent improvement time=0, best error was 12.35 @ 860
At iteration 860/2100/2100, Mean rms=1.603%, delta=1.337%, char train=8.95%, word train=9.1%, skip ratio=0%,  New best char error = 8.95 Transitioned to stage 1 wrote best model:data/sabei/checkpoints/sabei8.95_860.checkpoint wrote checkpoint.

2 Percent improvement time=0, best error was 8.95 @ 860
At iteration 860/2200/2200, Mean rms=1.275%, delta=0.979%, char train=6.5%, word train=6.6%, skip ratio=0%,  New best char error = 6.5 wrote best model:data/sabei/checkpoints/sabei6.5_860.checkpoint wrote checkpoint.

2 Percent improvement time=0, best error was 8.95 @ 860
At iteration 860/2300/2300, Mean rms=1.029%, delta=0.737%, char train=4.95%, word train=5%, skip ratio=0%,  New best char error = 4.95 wrote best model:data/sabei/checkpoints/sabei4.95_860.checkpoint wrote checkpoint.

2 Percent improvement time=0, best error was 6.5 @ 860
At iteration 860/2400/2400, Mean rms=0.786%, delta=0.458%, char train=3.45%, word train=3.4%, skip ratio=0%,  New best char error = 3.45 wrote best model:data/sabei/checkpoints/sabei3.45_860.checkpoint wrote checkpoint.

2 Percent improvement time=0, best error was 3.45 @ 860
At iteration 860/2500/2500, Mean rms=0.459%, delta=0.121%, char train=0.6%, word train=0.6%, skip ratio=0%,  New best char error = 0.6 wrote best model:data/sabei/checkpoints/sabei0.6_860.checkpoint wrote checkpoint.

2 Percent improvement time=0, best error was 3.45 @ 860
At iteration 860/2600/2600, Mean rms=0.292%, delta=0.037%, char train=0.2%, word train=0.2%, skip ratio=0%,  New best char error = 0.2 wrote best model:data/sabei/checkpoints/sabei0.2_860.checkpoint wrote checkpoint.

2 Percent improvement time=0, best error was 3.45 @ 860
At iteration 860/2700/2700, Mean rms=0.198%, delta=0%, char train=0%, word train=0%, skip ratio=0%,  New best char error = 0 wrote best model:data/sabei/checkpoints/sabei0_860.checkpoint wrote checkpoint.

Finished! Error rate = 0
lstmtraining \
--stop_training \
--continue_from data/sabei/checkpoints/sabei_checkpoint \
--traineddata data/sabei/sabei.traineddata \
--model_output data/sabei.traineddata
Loaded file data/sabei/checkpoints/sabei_checkpoint, unpacking...
`

The ground-truth files can be reviewed [`here`](https://github.com/3epnm/sabei)  
```
