# Script de Backup Oracle

1. `Para que possamos utilizar o script em primeiro lugar precisamos saber qual o usuário e senha do nosso Banco de Dados.`

2. `Segundo, caso você utilize um HD externo ou que esteja conectado no interior da sua máquina recomendo que se utilize o mountvol para que ele possa montar a unidade enquanto o script estiver em execução e após a execução ele irá desmontar por questões de segurança e evitar acesso indevido ao conteúdo de backup.`

   [Imgur](https://i.imgur.com/jIksjjk.png)
  

3. `Obtido os dados iremos editar o usuário e senha nos campos acima circulados.`

   [Imgur](https://i.imgur.com/Ufjay5R.png)

4. `Lembrando que o diretório onde será feito no comando exdp o usuário que irá definir. No meu caso na criação do banco o diretório "COPIA" fica no C:\COPIA.`

5. `O programa que iremos utilizar para compactar nosso backup é o 7zip, mas caso queira usar o WINZIP ou WINRAR fica a critério do usuário.`

6. `As demais etapas são para verificar a existência das pastas e se os arquivos de log e de backup tem mais de 7 dias. Caso você queira extender ou encutar o prazo você irá alterar o "D -7" pela quantidade de dias que o arquivo foi criado, ou seja caso você queria que seja deletado arquivos com mais de 15 dias substitua o "D -7" por "D -15".`

7. `Após todo o processo de backup ter sido finalizado o script irá deletar os arquivos que foram gerados na pasta temporária de backup, pois após a gerão do arquivo DMP e compactação o mesmo será copiado para a unidade de backup e não haverá mais a necessidade dele estar na pasta temporária.`

8. `Incuí o arquivo chama_backup.bat pois ele chama o script de backup e realiza a geração do log no qual podemos acompanhar se o processo de backup está sendo realizado corretamente, caso não esteja podemos identificar os erros e procurar as soluções para o mesmo.`

   [Imgur](https://i.imgur.com/SXilqYa.png)

9. `Agora segue o passo a passo de como criar a tarefa para que ela possa ser executada de forma automatizada, sem a necessidade de ficarmos executando ela manualmente.`

   [Imgur](https://i.imgur.com/jgXwyCP.png)

   [Imgur](https://i.imgur.com/oCIc4Y1.png)

   [Imgur](https://i.imgur.com/uSX3xWI.png)

   [Imgur](https://i.imgur.com/arAsvsO.png)

   [Imgur](https://i.imgur.com/OuIZ2IC.png)

   [Imgur](https://i.imgur.com/sbLXWoB.png)

   `Aqui iremos olhar a primeira janela das propriedades da nossa tarefa, marquem as mesmas caixas que estão marcadas nessa imagem.`

   [Imgur](https://i.imgur.com/arAsvsO.png)

   `Iremos definir quantas vezes o script irá executar em nosso sistema, aqui coloquei 3x ao dia em horários de menor pico.`



## Agradecimentos

- [Frederico Fávaro](https://github.com/FredericoFavaro)

- [Grupo GNU/LINUX Brasil](http://gnulinuxbrasil.com.br/)
- Grupo TecnoLoucos
