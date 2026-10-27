# Informações e procedência dos datasets

Registro da origem imediata, da atribuição de fonte e das limitações documentais dos arquivos usados em notebooks/Analise_Exploratoria.ipynb.

## Resumo

| Arquivo local | Formato e estrutura | Fonte imediata identificada | Observações |
|---|---|---|---|
| data/raw/missile_attacks_daily.csv | CSV; 4.285 linhas e 22 colunas na cópia analisada | [Massive Missile Attacks on Ukraine](https://www.kaggle.com/datasets/piterfm/massive-missile-attacks-on-ukraine), publicado por piterfm no Kaggle | Dados diários de ataques com mísseis e drones. A coluna source contém referências textuais, mas nem todas são URLs completas. |
| data/raw/equipments and personal losses_daily.json | JSON; 1.705 datas e 15 categorias na cópia analisada | [russian-casualties.in.ua](https://russian-casualties.in.ua) | A página informa a atribuição “Джерело даних: Генеральний штаб ЗСУ · minfin.com.ua” (Estado-Maior das Forças Armadas da Ucrânia · minfin.com.ua). |

Os números acima descrevem as cópias locais analisadas e podem mudar quando os arquivos forem atualizados.

## Catálogo de recursos

[Simon Huwiler — Russo-Ukrainian War Data Sources](https://github.com/simonhuwiler/russo-ukrainian-data-ressources) reúne links para bases relacionadas à guerra e aponta para o dataset do Kaggle e para russian-casualties.in.ua. O próprio README descreve o catálogo como incompleto. Portanto, ele é uma referência de descoberta, não a fonte produtora dos arquivos locais nem uma lista exaustiva de todas as fontes existentes.

## Atribuição e limites

- CSV: o Kaggle é a fonte imediata identificada para a cópia diária usada. Os valores na coluna source são mantidos como aparecem no arquivo; sem URLs completas e documentação adicional, não se deve atribuir uma origem específica a cada linha.
- JSON: o site de origem declara que os dados vêm do Estado-Maior das Forças Armadas da Ucrânia e do minfin.com.ua. Esta é a atribuição publicada pelo provedor e não uma verificação independente.
- Mapa em tempo real: foi mencionado como curiosidade, mas o link não veio na mensagem com as fontes. O mapa não é usado como entrada ou evidência nesta análise. Se for incluído como contexto, seu endereço deve ser registrado separadamente.
- Atualização: fontes e contagens foram verificadas em 2026-10-27. Os arquivos podem ser atualizados; ao atualizar as cópias locais, conferir novamente dimensões, datas, campos e metadados.

## Referências

- [Kaggle — Massive Missile Attacks on Ukraine](https://www.kaggle.com/datasets/piterfm/massive-missile-attacks-on-ukraine)
- [russian-casualties.in.ua](https://russian-casualties.in.ua)
- [Simon Huwiler — Russo-Ukrainian War Data Sources](https://github.com/simonhuwiler/russo-ukrainian-data-ressources)
