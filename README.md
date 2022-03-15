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

# 3. Creación de interfaz
 
def TABLERO(UY_TE_QUEMASTES, letraIncorrecta,   letraCorrecta, conceptoSecreto):
    print(UY_TE_QUEMASTES[len(letraIncorrecta)])
    print ("")
    fin = " "
    print ('Letras incorrectas:', fin)
    for letra in letraIncorrecta:
        print (letra, fin)
    print ("")
    espacio = '_' * len(conceptoSecreto)
    for i in range(len(conceptoSecreto)): 
        if conceptoSecreto[i] in letraCorrecta:
            espacio = espacio[:i] + conceptoSecreto[i] + espacio[i+1:]
    for letra in espacio: 
        print (letra, fin)
    print ("")
  
def INTENTOS(algunaLetra):
    # Devuelve la letra que el jugador ingreso. Esta función hace que el jugador ingrese una letra y no cualquier otra cosa
    while True:
        print ('Adivina una letra:')
        letra = input()
        letra = letra.lower()
        if len(letra) != 1:
            print ('Introduce una sola letra.') 
        elif letra in algunaLetra:
            print ('Ya has elegido esa letra ¿Qué tal si pruebas con otra?')
        elif letra not in 'abcdefghijklmnopqrstuvwxyz_':
            print ('Elije una letra.')
        else:
            return letra
      # 4. Función para reiniciar el juego
 
def START():
    print ('Quieres jugar de nuevo? (Si o No)')
    return input().lower().startswith('s')

# 4. Función para reiniciar el juego
 
def START():
    print ('Quieres jugar de nuevo? (Si o No)')
    return input().lower().startswith('s')
    
            

