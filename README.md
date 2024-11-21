# Architects Lyrics Corpus
This repository contains a corpus of song lyrics by the British metalcore band Architects. 

### Corpus Description
The Architects Lyrics Corpus is a collection of song lyrics from Architects' discocraphy, 
spanning 9 full albums. It serves as a resource for anyone interested in analysing lyrical themes,
linguistic patterns, stylistic evolution over time, etc., of Architects' lyrics. 

### Text Selection Criteria
Lyrics from all officially released studio albums by Architects as available on major streaming platforms, excluding:
- The album *For Those That Wish To Exist At Abbey Road* (2022),
  since this is a different rendition of the same songs on the original *For Those That Wish To Exist* (2021) album,
  which is already included in the corpus.
- The most recent album *the classic symptoms of a broken spirit* (2022),
  as these lyrics were not readily available online at the time of text collection.
- Instrumental songs, bonus tracks, and deluxe edition songs. 

### Data Collection process
Lyrics were collected per album from two online lyric databases:
- [Dark Lyrics](http://www.darklyrics.com/a/architects.html ) for the first 8 albums.
- [Metal Kingdom](https://www.metalkingdom.net/album/architects-for-those-that-wish-to-exist-144830)
  for the latest album included in the corpus (*For Those That Wish To Exist*, 2021)

### Cleaning and Preprocessing
Since the lyrics were retreived per album, the lyrics were processed so that each individual song lyric
is stored in its own separate text file. Additionally, extra lines in each file were replaced with spaces.

### Annotations
The corpus includes several layers of linguistic annotations processed using [spaCy](https://spacy.io/):
- **Tokens:** A list of individual words and punctuation marks from the original formatted lyrics.
- **Lemmas:** A list of lemmatised tokens, where each word is reduced to its base form.
- **Part-of-Speech (POS) Tags:** Each token is assigned a detailed POS tag indicating its grammatical category.

### File Formats
#### Notebook (.ipynb)
- The file `code.ipynb` contains all code used to realise this corpus.
  
#### Text files (.txt)
- The directory `data/albums` contains individual text files for the lyrics of each album.
- The directory `data/txt_files` contains individual text files for each song's lyrics, named in the format:
  `album_song#.txt`

#### CSV files (.csv)
- The file `metadata.csv` contains metadata included in the corpus.
- The file `Architects_Lyrics_with_spaCy_tags.csv` contains the fully annotated corpus:

    **Rows:** each row contains data on a song lyric.

    **Columns** (variables):

  | Header | Description |
  | ------ | ----------- |
  | `filename` | The filename of the song lyric file |
  | `title` | The songtitle |
  | `album` | The album the song is on|
  | `year` | The year the album with the song was released |
  | `text` | The processed song lyric|
  | `doc` | The doc object of the processed song lyric in its original form|
  | `tokens` | The tokenised version of the song lyrics' doc object |
  | `lemmas` | The lemmatised version of the song lyrics' doc object |
  | `POS` | The Part-of-Speech tags of the song lyrics' doc object |

### Additional Information
This corpus is provided for non-commercial, research purposes only. 
All rights to the lyrics belong to Architects and their publishers.






  
