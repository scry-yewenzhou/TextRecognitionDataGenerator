Text Run with Basic functions

## With Arabic and Punctuations dictionary
- random fonts with all fonts in useful_fonts
- only 1 word per image
- -r variable length
- -b 1 background plain white
- --na 2 name format 2, with labels.txt
- -ws word split, split on words
- --dict define dictionary with letters 

```
cd /home/PaddleOCR/arabic-recognition-training/
conda activate paddle
trdg -l ar \
     -t 8 \
     -c 200 \
     -w 1 \
     -r \
     -b 1 \
     -na 2 \
     -ws \
     --dict ./gen_dictionaries/arabic_and_punc.txt \
     --font_dir ./useful_fonts/ \
     --output_dir ./synthetic_data/ar-text-200/
```

## With Eastern Arabic numbers dictionary

- random fonts with all fonts in useful_fonts
- only 1 word per image
- -r variable length
- -b 1 background plain white
- --na 2 name format 2, with labels.txt
- -ws word split, split on words
- --dict define dictionary with letters 

```
cd /home/PaddleOCR/arabic-recognition-training/
conda activate paddle
trdg -l ar \
     -t 8 \
     -c 100 \
     -w 1 \
     -r \
     -b 1 \
     -na 2 \
     -ws \
     --dict ./gen_dictionaries/eastern_ar_nums.txt \
     --font_dir ./useful_fonts/ \
     --output_dir ./synthetic_data/ar-eastern-100/
```

## With Arabic words dictionary

- random fonts with all fonts in useful_fonts
- only 1 word per image
- -b 1 background plain white
- --na 2 name format 2, with labels.txt
- -ws word split, split on words
- --dict define dictionary with letters 

Do not set -r

```
cd /home/PaddleOCR/arabic-recognition-training/
conda activate paddle
trdg -l ar \
     -t 8 \
     -c 100 \
     -w 1 \
     -b 1 \
     -na 2 \
     -ws \
     --dict ./gen_dictionaries/combined_cleaned.txt \
     --font_dir ./useful_fonts/ \
     --output_dir ./synthetic_data/ar-words-100/
```

## English

```
cd /home/PaddleOCR/arabic-recognition-training/
conda activate paddle
trdg -l en \
     -t 8 \
     -c 100 \
     -w 1 \
     -r \
     -b 1 \
     -na 2 \
     -ws \
     --dict ./gen_dictionaries/latin_numbers_other_improved.txt \
     --font_dir ./useful_fonts/ \
     --output_dir ./synthetic_data/en-words-100/
```

## Generate Eastern Arabic numbers
```
conda activate paddle
cd /home/PaddleOCR/arabic-recognition-training/
git checkout eastern-numbers
trdg -t 8 \
     -c 20 \
     -b 1 \
     -na 2 \
     -ws \
     -k 15 -rk \
     -bl 1 -rbl \
     --random \
     --language ar \
     -tc '#000000,#888888' \
     --random_fontsize \
     --random_margin \
     --dict ./gen_dictionaries/eastern_ar_nums.txt \
     --font_dir ./latin_fonts/ \
     --output_dir ./synthetic_data/eastern-0830/
```
