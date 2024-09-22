# 1. O que é o DataHandler?
É uma ferramenta de software para análise estatística de resultados de exames finais de mercadorias pré-embaladas em IPEMs (órgãos executores do INMETRO).
Consiste apenas de um documento no formato notebook Jupiter (.ipynb) para ser executado no Google Colab. Sua utilização consiste no upload de um relatório de resultados de exames de mercadorias pré-embaladas em PDF obtido do SGI (Sistema de Gestão Integrada). O DataHandler executa as seguintes operações:
- Extrai todos os resultados de exames do PDF
- Classifica todos os produtos por segmento (material de construção, higiene pessoal, massas alimentícias, produtos têxteis, etc.)
- Constrói gráficos de Pareto com os dados, exibindo os segmentos que mais causam reprovações em exames finais

Dessa forma, o DataHandler é capaz de fornecer informações úteis ao planejamento estratégico das ações de fiscalização de mercadorias pré-embaladas, de modo que gestores podem direcionar os recursos disponíveis aos segmentos com maior incidência de reprovação.
Por fim, o DataHandler pode ser utilizado eventualmente para atualizar as informações e contribuir para a tomada de decisões no tocante à otimização dos recursos disponíveis para fiscalização 
#  2. Requisitos
- Uma conta Google ativa
- Acesso à internet com um navegador, preferencialmente Google Chrome
# 3. Instalação
3.1 Baixar o arquivo DataHandler.ipynb

3.2 Fazer login na conta Google

3.2 Acessar a página do Google Colab em https://colab.research.google.com/

3.3 Na página do Google Colab, fazer o upload do arquivo DataHandler.ipynb

3.4 Após fazer o upload, o DataHandler será aberto na página do Google Colabs. Clique no botão “play” da seção INICIALIZE SUA APLICAÇÃO AQUI

3.5 No decorrer da inicialização será exibida uma tela pedindo permissão para ter acesso ao Google Drive. Selecione sua conta Google e concorde com todas as outras telas que surgirem. Isso vai criar a estrutura de arquivos para a aplicação na sua conta do Google Drive

3.6 Também vai surgir a mensagem informando para acessar a página do **Google AI Studio** e copiar a **chave de API Gemini**. Gere a chave (se não houver gerado ainda), copie e cole no campo “Digite ou cole aqui sua chave do API Gemini:” e tecle ENTER

3.7 Pronto! O DataHandler foi instalado com sucesso na sua conta Google Drive. Para acessá-lo basta abrir no navegador a url **https://colab.research.google.com/** e procurar por **DataHandler** na aba **Recente** ou na aba **Google Drive**

# 4. Usando o DataHandler
Para usar o DataHandler você vai precisar antes de qualquer coisa clicar o botão PLAY em INICIALIZE A APLICAÇÃO AQUI. Esta é uma célula de código que carrega as bibliotecas necessárias. Como a ferramenta levanta uma máquina virtual transiente na Google, as bibliotecas são excluídas após um tempo de inatividade.

Como na primeira vez que usar não haverá nenhum conjunto de dados carregado, você deverá gerar antes um relatório no SGI na opção 4.3.13 (Produtos Coletados / Coletas x Exames Finais, opção “Coletas x Exames Finais”). Depois clique no botão PLAY da opção SE QUISER TRABALHAR COM DADOS NOVOS, EXECUTE ESTA CÉLULA. Vai aparecer um botão pra você fazer o upload do relatório gerado. Depois vai aparecer um campo pra você digitar algum comentário sobre os dados (importante pra identificar o conjunto de dados posteriormente)

Obs.: Você pode baixar um PDF incluído aqui para teste. Baixe o arquivo **data_test.pdf**, abra o DataHandler no Google Colab e faça o upload do PDF no botão PLAY da opção SE QUISER TRABALHAR COM DADOS NOVOS, EXECUTE ESTA CÉLULA.

Todo relatório que você fizer upload terão os dados armazenados em sua conta Google Drive em “Meu Drive / Colab Notebooks / DataHandler / Analysis”. Você poderá carregá-los clicando no botão PLAY da opção SE QUISER USAR DADOS JÁ SALVOS, EXECUTE ESTA CÉLULA

# 5. Análise estatística dos dados
Você pode avaliar os dados carregados clicando no botão PLAY das opções

ANÁLISE DE PARETO PARA OS SEGMENTOS DE PRÉ-EMBALADOS

ANÁLISE DE PARETO EM PRODUTOS COMERCIALIZADOS EM UNID. DE MASSA

ANÁLISE DE PARETO EM PRODUTOS COMERCIALIZADOS EM UNID. DE VOLUME

ANÁLISE DE PARETO EM PRODUTOS COMERCIALIZADOS EM N.º DE UNID. E UNID. DE COMPRIMENTO

Estas opções exibirão o gráficos de Pareto que mostrarão claramente que cerca de 80% das reprovações de exames são decorrentes provavelmente de um pequeno número de segmentos de mercadorias pré-embaladas. Com estas informações, as ações futuras de fiscalização poderão ser intensificadas nestes segmentos, otimizando assim a força de trabalho do IPEM e consequentemente incrementando a defesa do consumidor

# 6. Restrições
Como o DataHandler utiliza a inteligência artificial da Goggle – chamada de Gemini – se forem carregados PDFs muito grandes pode-se levantar uma exceção (de número 500) atribuída ao excesso de uso da Gemini gratuitamente. O DataHandler poderá ser usado após algumas horas. Obs.: a mesma exceção pode ser levantada também se forem carregados um número considerável de PDFs
