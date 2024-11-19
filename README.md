# DataHandler
# 1. O que é o DataHandler?
É uma ferramenta de software para análise estatística de resultados de fiscalizações de mercadorias pré-embaladas em IPEMs (órgãos executores do INMETRO).
Consiste apenas de um documento no formato notebook Jupiter (.ipynb) para ser executado no Google Colab. Sua utilização tem por base o upload de um relatório de resultados de exames de mercadorias pré-embaladas em PDF obtido do SGI (Sistema de Gestão Integrada do INMETRO). O DataHandler executa as seguintes operações:

- Extrai todos os resultados de exames do PDF
- Classifica todos os produtos reprovados por segmento (material de construção, higiene pessoal, massas alimentícias, produtos têxteis, etc.) utilizando **Google Gemini** (a inteligência artificial da Google)
- Constrói gráficos de Pareto com os dados, exibindo os segmentos que mais causaram reprovações em exames finais

Dessa forma, o DataHandler é capaz de fornecer informações úteis ao planejamento estratégico das ações de fiscalização de mercadorias pré-embaladas, de modo que gestores podem direcionar os recursos disponíveis aos segmentos com maior incidência de reprovação.
Por fim, o DataHandler pode ser utilizado eventualmente para atualizar as informações e contribuir para a tomada de decisões no tocante à otimização dos recursos disponíveis para fiscalização

#  2. Requisitos
- Uma conta Google ativa
- Acesso à internet com um navegador

# 3. Instalação
3.1 Ir para a página
https://github.com/adeiltonmsantos/DataHandler

3.2 Baixar o arquivo **DataHandler.ipynb**, clicando com o botão direito do mouse sobre ele e selecionando **Salvar link como...**. Selecione uma pasta de sua preferẽncia em seu computador
![image](https://github.com/user-attachments/assets/012de3a1-200f-4948-b9c2-4612b27be726)

3.3 Abrir seu navegador de internet e fazer login na sua conta Google (https://accounts.google.com/)

3.4 Acessar a página do **Google Colab** em https://colab.research.google.com/

3.5 Na página do Google Colab, fazer o upload do arquivo DataHandler.ipynb (ver imagem abaixo)
![upload_colab](https://github.com/user-attachments/assets/90b42f84-bf1c-4ad3-926d-b8ddee7a5b24)


3.6 Após fazer o upload, o DataHandler será aberto na página do Google Colab. Clique no botão “play” da seção INICIALIZAÇÃO
![path1254](https://github.com/user-attachments/assets/3894e45c-4ea4-48ef-8c9d-117c2740a80c)

3.7 No decorrer da inicialização será exibida uma tela pedindo permissão para ter acesso ao Google Drive. Selecione sua conta Google e concorde com todas as outras telas que pedirem acesso. Isso vai criar a estrutura de arquivos para a aplicação na sua conta do Google Drive

3.8 Também vai surgir a mensagem informando para acessar a página do **Google AI Studio** e copiar a **chave de API Gemini**. Clique no link exibido da página do **Google AI Studio** e gere a chave (se não houver gerado ainda), copie e cole no campo “Digite ou cole aqui sua chave do API Gemini:” e tecle ENTER
![Captura de tela de 2024-10-06 19-55-30](https://github.com/user-attachments/assets/f7e52790-6aec-4816-ac42-5d376f66bf2a)

3.7 Pronto! O DataHandler foi instalado com sucesso na sua conta Google Drive. Para acessá-lo basta abrir no navegador a url **https://colab.research.google.com/** e procurar por **DataHandler** na aba **Recente** ou na aba **Google Drive**

# 4. Usando o DataHandler
Para usar o DataHandler você vai precisar antes de qualquer coisa clicar o botão PLAY da seção INICIALIZAÇÃO (item 3.6 acima)

Esta é uma célula de código que carrega as bibliotecas necessárias. Como a ferramenta levanta uma máquina virtual na Google que não é permanente, as bibliotecas são excluídas após um tempo de inatividade.

Como na primeira vez que usar não haverá nenhum conjunto de dados carregado, você deverá gerar antes um relatório no SGI na opção 4.3.13 (Produtos Coletados / Coletas x Exames Finais, opção “Coletas x Exames Finais”). Depois, role a tela para baixo até a seção CARREGANDO DADOS. Clique no botão PLAY da opção CLIQUE ABAIXO PARA CARREGAR DADOS NOVOS
![carregando_dados_novos](https://github.com/user-attachments/assets/2dd5d4ae-5c17-42d0-bd52-b159443a2c34)

Vai aparecer um botão pra você fazer o upload do relatório gerado. Clique nele e selecione o PDF que você gerou com o SGI e salvou em seu computador
![carregando_dados_novos_upload](https://github.com/user-attachments/assets/f8e581dd-71f8-46d9-bd50-10aa5c0737ad)

Em seguida vai surgir um campo pra você digitar algum comentário sobre os dados (importante pra identificar o conjunto de dados posteriormente)

![image](https://github.com/user-attachments/assets/6f5a5b75-6f1a-4ae9-835f-ec083f146c76)

Obs.: Você pode baixar um PDF incluído aqui para teste. Baixe o arquivo **data_test.pdf**, abra o DataHandler no Google Colab e faça o upload do PDF no botão PLAY da opção CLIQUE ABAIXO PARA CARREGAR DADOS NOVOS.

Todo PDF que você fizer upload terão os dados armazenados em sua conta Google Drive em “Meu Drive / Colab Notebooks / DataHandler / Analysis”. Você poderá carregá-los clicando no botão PLAY da opção CLIQUE ABAIXO PARA CARREGAR DADOS SALVOS
![image](https://github.com/user-attachments/assets/49691545-2254-4232-842c-34f738a214a9)


# 5. Análise estatística dos dados
Você pode avaliar os dados carregados na seção ESTATÍSTICAS clicando no botão PLAY das opções

CLIQUE ABAIXO PARA ANÁLISE DE PARETO EM TODOS OS SEGMENTOS

CLIQUE ABAIXO PARA ANÁLISE DE PARETO EM UNIDADES DE MASSA

CLIQUE ABAIXO PARA ANÁLISE DE PARETO EM UNIDADES DE VOLUME

CLIQUE ABAIXO PARA ANÁLISE DE PARETO EM N.º DE UNIDADES E UNIDADES DE COMPRIMENTO

CLIQUE ABAIXO PARA UM COMPARATIVO ENTRE UNIDADES DE MASSA, VOLUME, N.º DE UNIDADES E UNID. DE COMPRIMENTO

As quatro primeiras opções exibirão o gráficos de Pareto que mostrarão claramente que cerca de 80% das reprovações de exames são decorrentes provavelmente de um pequeno número de segmentos de mercadorias pré-embaladas. Com estas informações, as ações futuras de fiscalização poderão ser intensificadas nestes segmentos, otimizando assim a força de trabalho do IPEM e consequentemente incrementando a defesa do consumidor.
A última opção exibe um gráfico de barras comparando reprovações entre mercadorias comercializadas em massa, volume, n.º de unidades e unidades de comprimento

# 6. Restrições
Como o DataHandler utiliza a inteligência artificial da Goggle – chamada Gemini – se forem carregados PDFs muito grandes pode-se levantar uma exceção (de número 500) atribuída ao excesso de uso da Gemini gratuitamente. O DataHandler poderá ser usado após algumas horas.

**Observação**: a mesma exceção pode ser levantada também se for carregado um número de PDFs que represente uma quantidade de dados que ultrapasse a cota de uso do Gemini de modo gratuito.

**Importante**: a depender da qualidade de conexão com a internet, pode-se processar PDFs com tamanho em torno de 2 e 3 MB, o que pode equivaler a aproximadamente 4.000 registros ou mais. Contudo, a qualidade de sua conexão com a internet e a estabilidade da Google podem permitir o processamento de quantidades maiores de dados
