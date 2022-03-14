# JuegoGrupo8
import random

# 1. Creación de dibujo



UY_TE_QUEMASTES = ['''
      +---+
      |   |
      O   |
     /|\  |
     / \  |
          |   
    🔥🔥       
    =========''', '''
      +---+
      |   |
      O   |
     /|\  |
     /    |
          |
    🔥🔥           
    =========''', '''
      +---+
      |   |
      O   |
     /|\  |
          |
          |
    🔥🔥
    =========''', '''
      +---+
      |   |
      O   |
     /|   |
          |
          |
    🔥🔥
    =========''', '''
      +---+
      |   |
      O   |
      |   |
          |
          |
     🔥🔥
    =========''', '''
      +---+
      |   |
      O   |
          |
          |
          |
     🔥🔥             
    =========''', '''
      +---+
      |   |
          |
          |
          |
          |
     🔥🔥              
    =========''']

# 2. Creación de la lista de conceptos que se utilizaran y la función que entregara uno de estos conceptos de forma aleatoria

conceptos = ["estructura_de_control", "python", "justo_vargas", "ciclos", "variables", "paradigma_procedural", "programacion", "vold", "procedimiento", "condiciones", "control_de_flujo", "if", "while", "else", "elif", "switch", "debugging", "paradigma", "test", "performance", "trust"]


def CONCEPTO(listaConceptos):
    conceptoAleatorio = random.randint(0, len(listaConceptos) - 1)
    return listaConceptos[conceptoAleatorio]
