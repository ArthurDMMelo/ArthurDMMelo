# Importar bibliotecas necessárias
import random
import nltk
from nltk.tokenize import word_tokenize
from nltk.stem import WordNetLemmatizer
from nltk.corpus import stopwords

# Criar uma classe para o chat boot
class ChatBoot:
    # Inicializar o chat boot com um nome e um arquivo de dados
    def __init__(self, name, data_file):
        self.name = name
        self.data_file = data_file
        self.lemmatizer = WordNetLemmatizer()
        self.stop_words = stopwords.words('portuguese')
        self.intents = self.load_intents()
        self.responses = self.load_responses()

  
