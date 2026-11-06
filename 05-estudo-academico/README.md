# Estudo acadêmico: segurança no uso de redes Wi-Fi públicas

Caderno Jupyter (`.ipynb`) com um estudo exploratório completo, no formato do *Guia Mackenzie de trabalhos acadêmicos* (2. ed. rev., 2021): capa, folha de rosto, resumo e *abstract*, listas, sumário, introdução, referencial teórico, metodologia, resultados e discussão, considerações finais, referências e apêndices. Os textos, os gráficos, as tabelas e as estatísticas são gerados a partir das bases CSV da pasta `dados/`.

> **Atenção:** o estudo usa **dados secundários** (inclusive valores lidos em reportagens que citam o Anuário do FBSP e as estatísticas do CERT.br) e **ainda não inclui resultados do teste com pessoas**. Veja a seção "Antes de entregar".

## Conteúdo da pasta

| Caminho | Descrição |
|---|---|
| `estudo-wifi-publico.ipynb` | Estudo completo, já executado (com gráficos e tabelas) |
| `estudo-wifi-publico.html` | Versão HTML do caderno, para leitura sem Jupyter (as equações usam MathJax e pedem internet) |
| `dados/` | Bases em CSV, dicionário de dados e modelo do teste com pessoas |
| `figuras/` | Gráficos em PNG (300 dpi) e logotipo usado na capa |
| `requirements.txt` | Dependências Python |

Bases em `dados/`: `cert_br_incidentes_anual.csv`, `cert_br_tipos_incidentes.csv`, `fbsp_estelionato.csv`, `indicadores_pesquisas.csv`, `estimativas_parametros.csv`, `referencias.csv` (59 referências com ABNT e estado de verificação), `resultados_teste_pessoas_modelo.csv`, `dicionario_de_dados.md` e três arquivos gerados pelo próprio caderno (`metricas_material.csv`, `cobertura_material.csv`, `itens_avaliacao.csv`).

## Como executar

1. Mantenha esta pasta na raiz do repositório, ao lado de `01-material-educativo/` a `04-infografico/` (o caderno lê esses textos).
2. Python 3.10 ou superior: `pip install -r requirements.txt`.
3. Abra `estudo-wifi-publico.ipynb` (Jupyter, VS Code ou Google Colab) e use **Executar tudo**. O caderno não acessa a internet.

Se a pasta for aberta fora do repositório, o caderno usa os CSV já gerados (`metricas_material.csv`, `cobertura_material.csv` e `itens_avaliacao.csv`) e continua funcionando.

## Como atualizar

- **Dados novos ou corrigidos:** edite os CSV em `dados/` e execute o caderno. O **Apêndice D** recalcula os números citados no texto; se algum valor mudar, a execução para com uma mensagem indicando qual número do texto precisa ser atualizado.
- **Resultados do teste com pessoas:** copie `resultados_teste_pessoas_modelo.csv` para `resultados_teste_pessoas.csv`, apague a linha de exemplo, preencha com dados reais (uma linha por participante, sem nome nem e-mail) e execute o caderno. As Tabelas 14 e 15 e a análise (diferença média, IC por *bootstrap*, Wilcoxon, d<sub>z</sub>) são geradas automaticamente. Depois, atualize o resumo, a seção 4.6 e as considerações finais com os resultados.
- **Textos dos materiais (01 a 04):** ao alterar o quiz ou o teste final, reexecute o caderno para atualizar cobertura temática e análise dos itens.

## Antes de entregar

1. Preencher o nome do(a) orientador(a) na folha de rosto (campo `[preencher ...]`).
2. Conferir nos documentos originais os valores lidos em reportagens (Anuário do FBSP 2026 e estatísticas do CERT.br). A coluna `status_verificacao` de `referencias.csv` indica o que foi verificado.
3. Resolver a **data da pesquisa de vitimização do FBSP** (15,8%; 26,3 milhões; 83,2%): uma reportagem indica março de 2026 e outra, março de 2023.
4. Confirmar com a coordenação a edição vigente das normas da ABNT (o Guia Mackenzie de 2021 cita edições que podem ter sido substituídas).
5. Aplicar o teste com pessoas (meta de 34 participantes de 18 anos ou mais; mínimo de 15) ou manter o texto como está, que já informa que o teste não foi aplicado.
6. Revisar os itens do quiz e do teste final: em todos os 15 itens a alternativa correta é a mais longa, e o pré e o pós-teste previstos compartilham um único tema.
7. Para a versão final em PDF ou Word, aplicar a apresentação gráfica do Guia (A4; margens 3/3/2/2 cm; fonte 12; espaçamento 1,5; seções primárias em página nova; paginação) e inserir os números de página nas listas.

## Limitações

Nenhuma fonte encontrada mede golpes originados em Wi-Fi público no Brasil; os dados de fraude são contexto. As pesquisas de fornecedores de segurança têm interesse comercial, datas e países diferentes. A estimativa de cerca de 54 milhões de pessoas expostas é um **cenário ilustrativo**, e não deve ser citada como medição. A classificação temática é automática (expressões regulares) e mede presença, e não profundidade.
