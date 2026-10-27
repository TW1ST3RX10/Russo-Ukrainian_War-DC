# Análise Exploratória de Dados da Guerra Russo-Ucraniana

Projeto acadêmico de Ciência de Dados I. O notebook documenta a identificação, preparação e análise exploratória de dois conjuntos de dados relacionados à guerra: registros de ataques com mísseis e drones em CSV e registros diários de perdas por categoria em JSON.

A análise é descritiva. Ela resume os arquivos locais e não verifica independentemente os acontecimentos, não estima causalidade e não combina os dois datasets.

## Objetivos

- Identificar a procedência imediata e a estrutura dos arquivos.
- Examinar tipos, dimensões, ausências e consistência.
- Preparar cópias de trabalho sem modificar os arquivos brutos.
- Explorar distribuições, frequências e padrões temporais.
- Comunicar os resultados em tabelas e gráficos, explicitando limitações.

## Fontes dos dados

| Dataset no projeto | Fonte imediata | Conteúdo |
|---|---|---|
| data/raw/missile_attacks_daily.csv | [Massive Missile Attacks on Ukraine — Kaggle](https://www.kaggle.com/datasets/piterfm/massive-missile-attacks-on-ukraine), publicado por piterfm | Registros diários de ataques com mísseis e drones; a cópia local contém a coluna source com referências textuais. |
| data/raw/equipments and personal losses_daily.json | [russian-casualties.in.ua](https://russian-casualties.in.ua) | Registros diários por categoria de perdas. A página atribui os dados ao Estado-Maior das Forças Armadas da Ucrânia e ao minfin.com.ua. |

O catálogo [Russo-Ukrainian War Data Sources](https://github.com/simonhuwiler/russo-ukrainian-data-ressources) reúne links úteis para localizar dados relacionados ao conflito. O próprio catálogo declara ser incompleto; ele não é o produtor dos arquivos usados aqui.

### Mapas de contexto

Os mapas abaixo servem apenas para consulta visual. Eles não são datasets deste projeto e não alimentam os cálculos do notebook.

- [DeepStateMap](https://deepstatemap.live): mapa interativo para acompanhar posições e evolução territorial.
- [GeoConfirmed — mapa da Ucrânia](https://geoconfirmed.org/map/ukraine): mapa de incidentes geolocalizados; a iniciativa é descrita pelo catálogo de recursos como baseada em vídeos e incidentes geoconfirmados.

## Estrutura do repositório

- data/raw/: cópias locais dos arquivos CSV e JSON.
- notebooks/Analise_Exploratoria.ipynb: relatório executável da análise.
- dataset_info.md: procedência, atribuições e limitações das fontes.
- requirements.txt: dependências Python utilizadas pelo notebook.

## Como executar

1. Instale as dependências listadas em requirements.txt com o comando: **python -m pip install -r requirements.txt**.
2. Abra notebooks/Analise_Exploratoria.ipynb no Jupyter Notebook, JupyterLab ou VS Code.
3. Execute as células na ordem apresentada. Os gráficos da seção de visualização dependem de Matplotlib.

O notebook usa caminhos relativos a partir do diretório notebooks. Se a execução for iniciada com outro diretório de trabalho, ajuste o diretório de trabalho do Jupyter para notebooks ou atualize os caminhos de dados.

## Limitações e interpretação

- As contagens e estatísticas descrevem as cópias locais analisadas e podem mudar quando as fontes forem atualizadas.
- A atribuição apresentada por russian-casualties.in.ua é a declaração do provedor; este projeto não realiza auditoria independente dos dados.
- A coluna source do CSV contém referências textuais que nem sempre são URLs completas.
- Valores ausentes não são automaticamente convertidos em zero.
- Os dois conjuntos permanecem separados porque suas unidades de observação são diferentes.
- A coluna is_shahed requer documentação adicional antes de receber interpretação semântica.

Para detalhes sobre estrutura, etapas e referências, consulte o notebook e dataset_info.md.
