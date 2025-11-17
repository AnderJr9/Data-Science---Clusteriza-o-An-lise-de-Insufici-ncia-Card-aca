# Data-Science---Clusteriza-o-An-lise-de-Insufici-ncia-Card-aca
Este projeto de Data Science utiliza o algoritmo de clusterização K-Means para identificar perfis de pacientes a partir do dataset "Heart Failure Clinical Records".  O objetivo é agrupar pacientes com características semelhantes, permitindo uma análise dos diferentes perfis encontrados.

# Pipeline de Execução
Os scripts devem ser executados na seguinte ordem para garantir o funcionamento correto do pipeline:

# normalizar.py

Lê o dataset bruto (heart_failure_clinical_records_dataset.csv).
Remove a coluna alvo (DEATH_EVENT).
Aplica a normalização MinMaxScaler nos dados.
Salva: dados_preprocessados_heart.csv e modelo_normalizador_heart.model.
clusterizar.py

# Carrega os dados pré-processados.
Calcula o número ótimo de clusters (K) usando o Método do Cotovelo (Elbow Method).
Treina o modelo KMeans com o número ótimo de clusters.
Salva: cluster_heart.model (o modelo treinado) e distorcoes_heart.jpg (o gráfico do cotovelo).
descrever_centroides_simplificado.py

# Carrega os modelos cluster_heart.model e modelo_normalizador_heart.model.
Reverte a normalização dos centroides para "traduzir" os grupos em valores legíveis.
Exibe no terminal a descrição de cada cluster.
processar_paciente_desconhecido.py

# Simula a chegada de um novo paciente (definido em um dicionário).
Carrega os modelos e aplica o mesmo pré-processamento (normalização).
Utiliza o modelo treinado para prever a qual cluster o novo paciente pertence.
