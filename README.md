# NLTK-Data-Cleaning

Text cleaning data source is the book Metamorphosis by Franz Kafka which is available for free from Project Gutenberg. Task Specific entails:

Manual Tokenization
Tokenization and Cleaning with NLTK
Additional Text Cleaning Considerations
Tips for Cleaning Text for Word Embedding
More to follow. Started with manual way the plugged in NLTK.

The file contains header and footer information that we are not interested in, specifically copyright and license information.

First, Split into words by white space -This means converting the raw text into a list of words and saving it again. Now stored (word variable) followed by spliting by Whitespace and removing punctuation in which we split the document into words by white space (as in “2. Split by Whitespace“), then use string translation to replace all punctuation with nothing (e.g. remove it). Python provides a constant called string.punctuation that provides a great list of punctuation characters.

Then Working with NLTK

Inflected Language.
"In grammar, inflection is the modification of a word to express different grammatical categories such as tense, case, voice, aspect, person, number, gender, and mood. An inflection expresses one or more grammatical categories with a prefix, suffix or infix, or another internal modification such as a vowel change" [Wikipedia]

Techniques Used
Stemming and Lemmatization are widely used in tagging systems, indexing, SEOs, Web search results, and information retrieval. For example, searching for fish on Google will also result in fishes, fishing as fish is the stem of both words.

    1. Stemming
Stem Words Stemming is the process of reducing inflection in words to their root forms such as mapping a group of words to the same stem even if the stem itself is not a valid word in the Language. Ie “fishing,” “fished,” “fisher” all reduce to the stem “fish.”

Some applications, like document classification, may benefit from stemming in order to both reduce the vocabulary and to focus on the sense or sentiment of a document rather than deeper meaning. There are many stemming algorithms, although a popular and long-standing method is the Porter Stemming algorithm. This method is available in NLTK via the PorterStemmer class. After stemming, words like [ 'morning', 'troubled'] converted to ['morn','troubl'] by PorterStemmer hence making it not viable and bringing need for lemmatization.

    2. Lemmatization
Lemmatization is a more effective option than stemming because it converts the word into its root word, rather than just stripping the suffices. It makes use of the vocabulary and does a morphological analysis to obtain the root word. Therefore, we usually prefer using lemmatization over stemming.
