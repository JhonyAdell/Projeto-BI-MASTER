# Test Grader

#### Aluno: Jhony Adell Fernandes de Carvalho (jhonyadell@gmail.com)
#### Aluno: Anderson Nascimento (prof.anderson@ica.ele.puc-rio.br)
A aplicação final se encontra conteneirizada. Para utiliza-la, primeiro certifique-se de que possui o Docker em conjunto com docker-compose instalado na máquina.

Trabalho apresentado ao Curso [BI MATER] (https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".
Respositório Git: https://github.com/JhonyAdell/Projeto-Final-BI-MASTER.git

### Resumo
  A ideia do Test Grader surgiu com a observação do processo de bolsão da escola Elite - Santa Cruz. Os candidatos realizavam as provas no dia do bolsão enquanto seu responsável ficava em uma sala assinando alguns documentos necessários, após a realização da prova, o candidato e o responsável ainda tinham que aguardar o tempo de correção e cálculo do desempenho naquela prova, para saber então em que bolsa ele se encaixava.
  Esse processo era bastante demorando, uma vez que em dias de bolsão, haviam diversos candidatos e o tempo de correção de suas provas impactavam negativamente necesse processo. O responsável era submetido à um tempo de espera muito maior do que o necessário.
  Analisando tal situação, surgiu a ideia de automatizar esse processo. Contei com a ajuda de um amigo de trabalho então desenvolvi um algoritimo que se mostrou bastante promissor na resolução desse problema.
  O test Grader foi desenvolvido com o auxilio da Biblioteca OpenCV(https://docs.opencv.org/master/). Basicamente, ele é um algoritimo de processamento de imagem que consegue identificar um cartão resposta e capturar as questões marcadas nele. Após todo o seu processamento, o algoritimo retorna um dataset que informa a quantidade de pixels em cada linha de questão. 
  ##### Ex: Q1> 110,17,107,115,98.
  Esses números representam a quantidade de pixels capturados pelo algoritimo na questão 1, nas opções de A até a E. A opção que apresenta uma menor quantidade de pixel é a questão marcada pelo candidato ou aluno.
  Esse dataset então, após ser gerado, é submetido á um modelo treinado, que informa dentre todas as opções, quais são as opções válidas. O Test Grader no momento se limita a informar a quantidade de questões válidas nas provas dos alunos, porém, uma vez que tivermos os gabaritos dos simulados ou provas, conseguiremos afirmar com bastante facilidade, quais questões estão válidas e corretas, resultando assim em uma correção de aproximadamente 10ms por prova.
  Com o amadurecimento da ideia, colocaremos essa solução em um dispositivo móvel, onde o professor com o auxilio da câmera, poderá fotografar um cartão resposta e processa-lo em tempo real, diminuindo então um tempo de correção de quase 1 minutor por prova para menos de 1 segundo. Esse algoritimo também será disponibilizado dentro da empresa como um micro-serviço, onde poderá realizar a leitura de cartões em lote e ter integração com outras aplicações da empresa.


### Setup
  Abra o Prompt de Comando
  No diretorio ...\Projeto-Final-BI-MASTER, execute o código
  ```
  virtualenv venv
  ```
  Após Instalar o Ambiente Virtual, você deve ativa-lo
  ```
  venv\Scripts\activate.bat 
  ```
  Após Ativar o Ambiente virtual, instale os requirements.
  ```
  pip install -r app/requirements.txt
  ```
  Agora basta executar a aplicação
  ```
  python app\main.py
  ```
  
  
  
  
