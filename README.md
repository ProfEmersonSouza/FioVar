# **FioVar**
 *Software de código aberto para o processamento de dados sociolinguísticos*

O FioVar é um software de código aberto, em desenvolvimento, que integra ferramentas computacionais para organizar gravações, produzir transcrições e anotações linguísticas e preparar ocorrências para análise. Seu percurso articula processamento automático e revisão humana, buscando preservar os vínculos entre áudios, transcrições, anotações e dados tabulados.
O projeto surgiu da preparação de uma oficina a convite da professora Leila Tesch (UFES), no IV Encontro Capixaba de Sociolinguistas, realizado de 3 a 5 de novembro de 2026. Inspirado na metáfora do fio que orienta o percurso por um labirinto, o FioVar propõe uma estrutura modular, adaptável às necessidades de cada pesquisa.

## **Versão atual**
v0.1.0-alpha — experimental
O funcionamento integrado das ferramentas e a qualidade dos resultados ainda estão em avaliação. Transcrições, alinhamentos, atribuições de falantes e anotações automáticas são resultados preliminares e podem apresentar erros.
As sugestões de transcrição fonética e a identificação automática de candidatos exigem conferência auditiva e revisão humana. A identificação e a codificação das variantes devem seguir os critérios definidos para cada pesquisa.

## **Recursos integrados**
O percurso de processamento reúne:
- WhisperX: transcrição automática e alinhamento temporal.
- pyannote.audio: diarização, ou identificação dos segmentos atribuídos a diferentes falantes.
- Stanza: anotação morfossintática.
- SILAC: representação fonológica derivada da escrita.
- wav2vec2-large-xlsr-53-phoneme-portuguese: sugestões de transcrição fonética a partir do áudio.
- ELAN: inspeção e revisão das anotações em associação com a gravação.
- dmsocio: identificação, extração e tabulação de ocorrências.
As ferramentas e os modelos integrados mantêm suas respectivas autorias, condições de acesso e licenças.

## **Como começar**
1. Leia o livro/tutorial que acompanha o projeto.
2. Abra o arquivo FioVar_v0_1_0_alpha.ipynb no Google Colab.
2. Siga as orientações de preparação do ambiente e de acesso aos modelos.
3. Execute as etapas na ordem indicada, salvando os arquivos produzidos.
4. Revise os resultados no ELAN antes da codificação e da tabulação final.
5. O tutorial apresenta as orientações para acessar o notebook, utilizar o Google Colab, configurar o acesso ao modelo de diarização pelo Hugging Face e armazenar o token nos Segredos do Colab. Também explica como organizar os arquivos e conservar os resultados.
6. O link para o livro/tutorial será incluído nesta seção.

## **Percurso de trabalho**
O pipeline compreende a preparação do áudio, a identificação do participante e o registro dos preditores sociais, seguidos da instalação das bibliotecas e da verificação do ambiente.
Em seguida, realiza a transcrição automática, o alinhamento temporal e a diarização, com procedimentos para salvar, recuperar e exportar os resultados para revisão no ELAN. As etapas posteriores incluem a anotação morfossintática, a representação fonológica derivada da escrita e as sugestões de transcrição fonética.
Nesta versão, as etapas finais se concentram no estudo de /r/ em coda, com identificação de candidatos, revisão e codificação das ocorrências e geração de uma planilha com informações sociais e linguísticas.

## **Revisão e validação**
- A revisão humana faz parte do percurso de trabalho. Antes de utilizar os dados na análise, confira:
- A correspondência entre o áudio e a linha do tempo do EAF.
- Os limites temporais e o conteúdo das transcrições.
- A atribuição dos segmentos aos falantes.
- As anotações morfossintáticas e as representações fonológicas e fonéticas.
- A seleção e a codificação das ocorrências.
- O áudio e o EAF utilizados em cada etapa devem compartilhar a mesma linha do tempo. Cortes ou deslocamentos exigem a atualização correspondente dos arquivos.

## **Desenvolvimento**
Os próximos passos incluem testar a integração das ferramentas, avaliar os resultados em diferentes condições de gravação e perfis de fala e aperfeiçoar a documentação e os procedimentos de revisão.
Também se pretende desenvolver protocolos para outras variáveis fonético-fonológicas, morfossintáticas e discursivo-pragmáticas, considerando o envelope de variação e os critérios de seleção, codificação e validação próprios de cada fenômeno.
Sugestões e relatos de problemas podem ser registrados na seção Issues deste repositório. Ao relatar um problema, informe a etapa, a mensagem de erro e o comportamento observado, sem divulgar tokens ou dados identificáveis dos participantes.

## **Ciência aberta e proteção dos dados**
O FioVar busca tornar os procedimentos examináveis, reproduzíveis e passíveis de aperfeiçoamento coletivo, com reconhecimento das autorias e respeito às licenças.
A disponibilização do software não implica autorização para publicar os dados processados. O compartilhamento de áudios, transcrições e informações sociais deve observar as autorizações e os compromissos éticos de cada pesquisa.

## **Licença**
Consulte o arquivo de licença disponível neste repositório. As condições dos componentes de terceiros devem ser observadas separadamente.
