# FioVar

*Software de código aberto para o processamento de dados sociolinguísticos*

O FioVar reúne ferramentas para preparar gravações, transcrever e anotar a fala, revisar os resultados e organizar ocorrências para análise em Sociolinguística Variacionista. O percurso mantém os vínculos entre áudio, anotações e dados tabulados, permitindo voltar à gravação para conferir cada ocorrência.

O projeto surgiu da preparação de uma oficina ministrada a convite da professora Leila Tesch (UFES) no IV Encontro Capixaba de Sociolinguistas, realizado de 3 a 5 de novembro de 2026.

## Versão atual

A **v0.1.1-alpha**, atualizada em 8 de novembro de 2026, é uma revisão corretiva da versão experimental apresentada na oficina. Ela ajusta o envio de arquivos WAV nas etapas de etiquetagem e transcrição para preservar o nome do áudio quando ele é reenviado na mesma sessão do Google Colab. A seção **11.4** do notebook orienta o registro de intercorrências linguísticas em uma trilha de revisão no ELAN.

O percurso atual inclui um protocolo para o estudo da **variação de /r/ em coda**. O notebook localiza contextos candidatos. O pesquisador confere as ocorrências pela escuta, aplica os critérios de codificação e reúne as variantes e os preditores sociais e linguísticos para análise em R.

## Como começar

1. Consulte o livro ou tutorial que acompanha o projeto.
2. Baixe o [notebook FioVar v0.1.1-alpha](FioVar_v0_1_1_alpha.ipynb) e abra-o no Google Colab.
3. Siga as instruções do notebook para preparar o ambiente, autorizar o acesso ao modelo de diarização no Hugging Face e guardar o token nos Segredos do Colab.
4. Execute as etapas na ordem indicada e salve os arquivos gerados. Abra o EAF com o áudio correspondente no ELAN para revisar as anotações antes da codificação e da tabulação.

## Ferramentas integradas

- **WhisperX** — transcrição automática e alinhamento temporal.
- **pyannote.audio** — diarização e atribuição de trechos a falantes.
- **ELAN** — inspeção e revisão das anotações em associação com o áudio.
- **Stanza** — etiquetagem morfossintática.
- **SILAC** — representação fonológica derivada da escrita.
- **`wav2vec2-large-xlsr-53-phoneme-portuguese`** — sugestões de transcrição fonética a partir do áudio.
- **`dmsocio`** — rotinas adaptadas para reunir e tabular ocorrências e preditores.

## Revisão e registro de intercorrências

As saídas automáticas têm caráter preliminar. Durante a revisão, confira a sincronização entre o áudio e o EAF, os limites temporais, a transcrição, a atribuição dos falantes e as anotações linguísticas. Confirme pela escuta as ocorrências selecionadas e aplique os critérios de codificação do estudo.

No ELAN, o pesquisador pode criar uma trilha `REV_linguistica` para anotar a etapa, a unidade linguística afetada, o tipo de intercorrência e a forma revisada. Para calcular proporções, registre também o total de unidades revisadas por categoria, incluindo os acertos. A metodologia do trabalho pode descrever os trechos revisados, os critérios de classificação e a forma de contagem.

## Versão 2.0

Com publicação prevista para **dezembro de 2026**, a versão 2.0 pretende ampliar a anotação no ELAN com dois conjuntos de trilhas:

- **Discursivas** — sugestões de tópicos da conversa e sinalização de possíveis mudanças temáticas.
- **Segmentais** — delimitação de sílabas e segmentos fonéticos no áudio. Os intervalos vocálicos servirão de base para a extração de formantes.

Também estão previstos protocolos para os seguintes fenômenos:

- **Fonético-fonológicos** — vogais médias pretônicas /e/ e /o/, /t/ e /d/ diante de [i] e /S/ em coda silábica.
- **Morfossintáticos** — concordância nominal, formas imperativas e negação sentencial.

## Como citar

Para citar a revisão disponível neste repositório:

SOUZA, Emerson Santos de. **FioVar: um software de código aberto para processamento de dados sociolinguísticos**. Versão v0.1.1-alpha. GitHub, 2026. Software.


## Autoria e contribuições

O FioVar foi idealizado por **Emerson Santos de Souza**, professor do Departamento de Educação e do Programa de Pós-Graduação em Estudos Linguísticos da Universidade Estadual de Feira de Santana (UEFS). [Currículo Lattes](https://lattes.cnpq.br/6006857841226887)

Sugestões e relatos de problemas podem ser enviados pela aba **Issues**. Informe a versão do notebook, a etapa, o comportamento observado e a mensagem de erro, quando houver. Remova tokens e informações que possam identificar participantes antes de compartilhar o relato.

## Licença e proteção dos dados

O código original do FioVar é disponibilizado sob a **licença MIT**. As ferramentas, bibliotecas e modelos de terceiros mantêm suas próprias autorias, licenças e condições de acesso. O compartilhamento de gravações, transcrições e informações sociais deve seguir as autorizações e os compromissos éticos de cada pesquisa.
