# Dicionário de dados

Todos os arquivos são CSV em UTF-8, com cabeçalho na primeira linha. Cada linha de dados traz `fonte_id`, que remete a `referencias.csv`.

| Arquivo | Coluna(s) | Descrição |
|:---|:---|:---|
| `cert_br_incidentes_anual.csv` | `ano` | Ano da série (inteiro). |
| `cert_br_incidentes_anual.csv` | `periodo` | “ano completo” ou período parcial (jan-jun). |
| `cert_br_incidentes_anual.csv` | `total_notificacoes` | Total de notificações de incidentes recebidas pelo CERT.br no período. |
| `cert_br_incidentes_anual.csv` | `tipo_dado_total` | “publicado” (valor lido de fonte) ou “derivado” (calculado pelos autores). |
| `cert_br_incidentes_anual.csv` | `fraude_notificacoes` | Notificações da categoria fraude (vazio quando não localizado). |
| `cert_br_incidentes_anual.csv` | `tipo_dado_fraude` | Natureza do valor de fraude. |
| `cert_br_incidentes_anual.csv` | `fonte_id` | Identificador da(s) fonte(s) em referencias.csv. |
| `cert_br_incidentes_anual.csv` | `observacao` | Notas sobre o valor. |
| `cert_br_tipos_incidentes.csv` | `periodo` | Ano ou semestre ao qual se refere a composição. |
| `cert_br_tipos_incidentes.csv` | `tipo` | Tipo de incidente (Scan, DoS, Fraude, Web, Worm, Invasão, Outros, Demais categorias) ou subtipo de fraude. |
| `cert_br_tipos_incidentes.csv` | `notificacoes` | Contagem de notificações (vazio quando só há percentual publicado). |
| `cert_br_tipos_incidentes.csv` | `percentual` | Percentual publicado sobre o total do período. |
| `cert_br_tipos_incidentes.csv` | `tipo_dado, fonte_id, observacao` | Natureza do valor, fonte e notas. |
| `fbsp_estelionato.csv` | `ano` | Ano do registro. |
| `fbsp_estelionato.csv` | `estelionato_total` | Ocorrências de estelionato (todas as modalidades) registradas no ano. |
| `fbsp_estelionato.csv` | `estelionato_eletronico` | Ocorrências de estelionato por meio eletrônico (vazio quando não localizado). |
| `fbsp_estelionato.csv` | `variacao_eletronico_pct_publicada` | Variação percentual do eletrônico divulgada pela fonte. |
| `fbsp_estelionato.csv` | `tipo_dado, fonte_id, observacao` | Natureza do valor, fonte e notas. |
| `indicadores_pesquisas.csv` | `id` | Identificador do indicador. |
| `indicadores_pesquisas.csv` | `fonte_id` | Identificador da fonte em referencias.csv. |
| `indicadores_pesquisas.csv` | `pais, ano` | País e ano da coleta da pesquisa. |
| `indicadores_pesquisas.csv` | `n_amostra, populacao_ou_base` | Tamanho da amostra (quando informado) e universo pesquisado. |
| `indicadores_pesquisas.csv` | `indicador, valor, unidade` | Descrição do indicador, valor e unidade (%, milhões etc.). |
| `indicadores_pesquisas.csv` | `natureza_da_fonte` | Tipo de fonte (pesquisa de fornecedor, estudo de campo, telemetria etc.). |
| `indicadores_pesquisas.csv` | `valor_aproximado` | “sim” quando o valor foi lido de forma aproximada. |
| `estimativas_parametros.csv` | `parametro, valor, unidade` | Nome, valor e unidade do parâmetro. |
| `estimativas_parametros.csv` | `tipo, derivacao_ou_fonte, observacao` | “entrada” (dado), “premissa” (escolha dos autores), origem e notas. |
| `referencias.csv` | `id, categoria, chave_ordenacao` | Identificador, categoria e chave de ordenação alfabética. |
| `referencias.csv` | `referencia_abnt` | Referência completa em formato ABNT/Guia Mackenzie, com título em negrito. |
| `referencias.csv` | `data_acesso, status_verificacao, uso_no_estudo` | Data de acesso, estado de verificação e uso no estudo. |
| `resultados_teste_pessoas_modelo.csv` | `id_participante` | Código anônimo do participante (não usar nome nem e-mail). |
| `resultados_teste_pessoas_modelo.csv` | `faixa_etaria, frequencia_wifi_publico` | Perfil do participante. |
| `resultados_teste_pessoas_modelo.csv` | `pre_q1 a pre_q5; pos_q1 a pos_q5` | Acerto (1) ou erro (0) em cada item do pré-teste e do pós-teste. |
| `resultados_teste_pessoas_modelo.csv` | `clareza_1a5, utilidade_1a5` | Notas de 1 a 5. |
| `resultados_teste_pessoas_modelo.csv` | `compartilharia, comentario` | “sim”, “talvez” ou “nao”; comentário aberto opcional. |
| `metricas_material.csv, cobertura_material.csv, itens_avaliacao.csv` | `(gerados pelo caderno)` | Métricas descritivas, matriz de cobertura temática e análise dos itens de avaliação. |
