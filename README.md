# WordTonize
import nltk
#nltk.download('stopwords')
#nltk.download('punkt')
from nltk.tokenize import word_tokenize as wt
from nltk.tokenize import sent_tokenize as st
from nltk.corpus import stopwords as sw

sentence = "A paragraph is a self-contained unit of discourse in writing dealing with a particular point or idea. A paragraph consists of one or more sentences. Though not required by the syntax of any language, paragraphs are usually an expected part of formal writing, used to organize longer prose"
wordTokens = wt(sentence)
sentenceTokens = st(sentence)
print(wordTokens)
print(sentenceTokens)
print(sw.fields())
englishCollection= set(sw.words('english'))
words = [['A', 'paragraph', 'is', 'a', 'self-contained', 'unit', 'of', 'discourse', 'in', 'writing', 'dealing', 'with', 'a', 'particular', 'point', 'or', 'idea', '.', 'A', 'paragraph', 'consists', 'of', 'one', 'or', 'more', 'sentences', '.', 'Though', 'not', 'required', 'by', 'the', 'syntax', 'of', 'any', 'language', ',', 'paragraphs', 'are', 'usually', 'an', 'expected', 'part', 'of', 'formal', 'writing', ',', 'used', 'to', 'organize', 'longer', 'prose']]

result = [words for words in words if words not in englishCollection]
print(result)
