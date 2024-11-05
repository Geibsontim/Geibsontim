import random
from datetime import datetime

# Ativos disponíveis
ativos = ["USD/BRL", "EUR/USD", "GBP/USD"]

# Função para gerar sinais
def gerar_sinal(ativo, quantidade_sinais):
    sinais = []
    for _ in range(quantidade_sinais):
        horario = datetime.now().strftime("%H:%M")
        sinal = random.choice(["CHAMADA", "COLOCAR", "VENDER"])
        sinais.append(f"{ativo} - {horario} : {sinal}")
    return sinais

# Exemplo de geração de sinais
ativo_selecionado = ativos[0]  # Seleciona um ativo da lista
numero_sinais = 5  # Quantidade de sinais a serem gerados

sinais_gerados = gerar_sinal(ativo_selecionado, numero_sinais)

# Mostra os sinais
for sinal in sinais_gerados:
    print(sinal)
