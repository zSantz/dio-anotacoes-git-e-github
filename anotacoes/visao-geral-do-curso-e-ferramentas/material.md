# 👨‍🎓 Visão Geral do Curso e Ferramentas
Olá, aqui vou está deixando minhas anotações sobre a Sessão Inicial do Curso. Espero que gostem.

![](https://media.tenor.com/Pm4S40MGsIQAAAAC/hacker-hackerman.gif)

# 👨🏻‍💻 Versionamento de Código e VCS
![](https://www.darede.com.br/wp-content/uploads/2022/09/versonamento-de-codigo-blog-1.jpg)
### Versionamento de Códigos

Vamos ilustrar uma história em que você e seu amigo estão estudando programação, e então seu amigo chega e diz:

- Amigo: Tive uma ideia que vai nos deixar milionários.
- Você: Não coloca muita fé nas palavras dele, mas aceita, pois, no pior dos casos, terá mais um projeto para adicionar ao portfólio.

Então, vocês criam um arquivo base. Para que cada um possa trabalhar de casa quando não estiverem juntos, você cria uma pasta compartilhada no drive e vão inserindo aquela primeira versão. A cada nova versão, vocês vão renomeando: "versão 1, versão 2". Chega um momento em que vocês se desorganizam na forma como estão nomeando os arquivos e percebem que vão demorar muito tempo esperando para que um de vocês edite o arquivo para que o outro possa baixar aquela versão e criar uma nova.

Vocês decidem dividir o trabalho, para que, no final, possam mesclar tudo em um arquivo só. No entanto, na hora de juntar esses dois arquivos, percebem que terão mais trabalho do que imaginavam. Para piorar, seu amigo estava utilizando uma versão desatualizada, o que gerou um erro.

Nessa história, fica evidente a importância do versionamento de código, em que a cada alteração no código, uma nova versão é gerada. Percebemos alguns problemas relacionados, principalmente se feito manualmente:

1. No início, tiveram problemas de organização, começaram de uma maneira e mudaram a forma como estavam nomeando as versões. Imagine se precisassem resgatar algum trecho de código, mas não lembrassem em qual versão estava. Seriam obrigados a verificar versão por versão até encontrar o trecho desejado.
2. Outro problema seria o armazenamento, pois a cada versão, eles tinham que fazer o upload de todos os arquivos, incluindo as alterações feitas. Por exemplo, se uma versão tinha 200 linhas e o amigo adicionava mais 50 linhas, ele precisaria fazer o upload dessas 200 linhas mais as 50 que ele adicionou.

### Sistemas de Controle de Versão

Então para resolver esse e outros problemas, foi aí que surgiu os **Sistemas de Controle de Versão**, que eles *são softwares que controlam as versões de um arquivo ao longo do tempo.*

- Registrando o histórico de atualizações de um arquivo;
- Ele gerencia ali, quais as alterações foram feitas, a data, autor, etc.;
- Então nisso, a gente acaba eliminando alguns problemas, quanto a relação à busca daquele trecho em que vocês estavam procurando, tanto como o armazenamento, já que ele não vai subir todo o código novamente e sim **apenas aquele trecho que você alterou** e isso trás para gente uma **melhor organização, controle, além da segurança** pois você pode gerenciar quem pode estar contribuindo com aquele projeto.

### Tipos de Sistemas de Controle de Versão

Dentre os tipos de Sistema de Controle de Versão **(CVCS)**, temos:

- **VCS CENTRALIZADO(CVCS)**: *EXP: CVS. SUBVERSION.*
    
    Aqui a gente tem apenas um servidor que vai conter todos os arquivos responsáveis pelo controle de versão, ali você vai ter as áreas de trabalho conectadas nesse servidor, no caso, você e seu amigo, mas ele tem como desvantagem, caso ele saia do ar, você não consegue salvar ou fazer alterações no servidor, da mesma forma se um arquivo for corrompido ou houver alguma perca de dados, se você não tiver um backup adequando, você acaba também perdendo todo o seu projeto.
    
    ![](https://uploaddeimagens.com.br/images/004/604/330/full/Screenshot_2023-09-11-23-22-23_1440x900.png?1694485563)
    

- **VCS DISTRIBUÍDOS(DVCS)**: *EXP: GIT, MERCURIAL.*
    
    Aqui, cada repositório, cada banco de versão, ele é duplicado localmente, então você e seu amigo, vão ter uma copia, do que está no servidor de vocês principal, e isso permite que você e seu amigo possa editar aquele arquivo, mesmo que o servidor esteja fora do ar. Então ele clona o **repositório** completo, o que inclui o histórico de versões.
    
    Cada clone é como se fosse um **Backup**, o que possibilita um **fluxo de trabalho** mais flexível, já que cada um pode trabalhar de um lugar, mesmo que não esteja conectado no servidor
    
    ![](https://i.imgur.com/xzJVddD.png)
    

# 👨🏻‍💻 Git
### O Que é o Git?
![Alt text](image-1.png) 
Como mencionado anteriormente, o Git é um **Sistema de Controle de Versão Distribuído**, e é um dos sistemas mais amplamente utilizados atualmente, o que se deve a vários fatores:

- É gratuito e de código aberto (open source).
- Possui ramificações (branching) e fusões (merging) eficientes.
- É leve e rápido.

> Para obter mais informações sobre o assunto, visite o **[site oficial do Git](https://git-scm.com/)**.
> 

### Breve Histórico do Git

No ano de 2002, a história do Git está ligada ao projeto do **Núcleo (kernel) do Linux**, um projeto de código aberto. Antes de criar o Linux, Linus Torvalds começou a utilizar o **BitKeeper**, um **DVCS Proprietário** (sistema de controle de versão distribuído proprietário) para armazenar as versões do Kernel.

No ano de 2003, devido a conflitos com a comunidade relacionados à **Engenharia Reversa**, o BitKeeper **revogou a licença gratuita**. Isso levou Linus Torvalds, o criador do Linux, e sua equipe a desenvolverem sua própria ferramenta, o **Git**.

### Fluxo Básico no Git

Se desejamos **clonar nosso repositório remoto**, no seu repositório local, utilizamos o comando:

**`git clone -> Clona um repositório existente para um novo diretório local`**

Suponhamos que você decidiu fazer uma alteração. Como você faz para salvar essa alteração? Utilizamos o comando:

**`git commit -> Grava as alterações em nosso repositório`**

Para enviar essas alterações para o servidor remoto, antes de tudo, você precisa verificar se seu amigo já não enviou alguma alteração. Para atualizar seu repositório local a partir do repositório remoto, utilize o comando:

**`git pull -> "Puxa" as alterações do repositório remoto para o repositório local, buscando e mesclando com os arquivos em que você está trabalhando`**

Para enviar as alterações, utilize o comando:

**`git push -> "Empurra" as alterações do repositório local para o repositório remoto`**


# 👨🏻‍💻 GitHub
### O Que é o GitHub
![Alt text](image.png)
Apesar de ter um nome parecido com Git, eles são ferramentas distintas. Enquanto o Git é um sistema de controle de versão distribuído, o **GitHub** é uma **plataforma de hospedagem de código para controle de versão com Git**.

O GitHub proporciona um ambiente colaborativo, permitindo o acesso ao código de diversos desenvolvedores e a contribuição em projetos. Além disso, possui uma comunidade ativa e é utilizado globalmente.

> Para mais informações, visite o [GitHub](https://github.com/).


### Breve Histórico do GitHub

- **2008** - Desenvolvido por Chris Wanstrath, J. Heytt, Tom Preston e Scott Chacon.
- **2018** - Dez anos depois, foi vítima de um dos maiores **ataques de DDoS** de todos os tempos. Nesse mesmo ano, foi adquirido pela **Microsoft Corporation** por **US$ 7,5 bilhões**.

### Diferença entre Git e GitHub

- O **Git** atua na gestão de versões de código, fazendo o gerenciamento de todas as versões do seu código.
- Já o **GitHub** age como um servidor, armazenando remotamente todo o seu repositório de versões.

## Recomendação de Leituras

[Sobre Controle de Versão](https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Sobre-Controle-de-Vers%C3%A3o)

[Uma Breve História do Git](https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Uma-Breve-Hist%C3%B3ria-do-Git)