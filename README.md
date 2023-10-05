# Questao_05_AV1
# Prova de Álgebra Linear
    import numpy as np

    def norm_p_matriz_2por2(matriz, p):
    
        # Teste se a matriz de entrada é 2x2
        if matriz.shape != (2, 2):
            raise ValueError("A matriz deve ser 2x2")
    
        # Teste se a ordem p da norma é maior ou igual a 1
        if p < 1:
            raise ValueError("O valor de p deve ser maior ou igual a 1")
    
        # Cálculo da norma-p da matriz 2x2 de entrada
        norma = 0
        for i in range(0, 2):
            for j in range(0, 2):
                norma = norma + abs(matriz[i, j]) ** p
        norma = norma ** (1/p)

        return norma

    # Teste
        matriz = np.array([[1, 2], [3, 4]])
        p = 2

        resultado = norm_p_matriz_2por2(matriz, p)

        print("A norma-{} da matriz 2x2 de entrada é".format(p), resultado)
