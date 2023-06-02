# AplicacaoWeb_criptoanalise_Nodejs
Trabalho universitário sobre criptoanálise usando Node.js
O objetivo dessa aplicação web é fazer transferências de arquivos entre utilizadores de forma segura. Para isso, foram utilizadas cifras AES-CBC e o protocolo de chaves públicas e privadas RSA, além de garantir a integridade dos arquivos com códigos HASH. A transferência dos arquivos é feita utilizando base de dados, onde todos os usuários podem acessar os arquivos presentes nela, entretanto, somente o dono da respectiva chave privada pode fazer o download do arquivo decifrado. Abaixo encontram-se representações da aplicação em funcionamento.
</br>

<h4>1. Criação de um token</h4>
Ao criar um token, um arquivo .zip é baixado contendo uma chave pública e uma chave privada RSA. Ademais, o token e sua respectiva chave pública ficam salvos na base de dados MySQL.
<img src="https://github.com/enriconunes/AplicacaoWeb_criptoanalise_Nodejs/assets/75801762/0139ad1d-60fb-45de-8166-81c3b41ffda4" />

<h4>2. Enviar arquivo</h4>
Para enviar um arquivo, basta digitar o token de quem irá o receber. Dessa forma, o arquivo será enviado para a base de dados cifrado com a chave pública do token selecionado. Além disso, pode-se definir se o arquivo será cifrado e/ou compactadado (zip) antes do envio ser efetuado.
<img src="https://github.com/enriconunes/AplicacaoWeb_criptoanalise_Nodejs/assets/75801762/7ff8e473-cdc3-4b5a-8af5-33db051792e4" />

<h4>3. Receber arquivo</h4>
Na primeira parte dessa seção, é possível digitar o seu token para listar todos os arquivos que estão associados à ele, para que, dessa forma, seja possível obter o ID do arquivo desejado, assim como sugere a seguinte imagem: </br>
<img src="https://github.com/enriconunes/AplicacaoWeb_criptoanalise_Nodejs/assets/75801762/48a45eeb-d90e-47c2-a27c-495ee27eb96c" width="400px"/> </br>
Após identificar o ID do arquivo desejado, basta digitá-lo na segunda seção deste collapse e selecionar o arquivo .pem que contém a chave privada válida para fazer o download do arquivo já decifrado (caso ele tenha sido cifrado).
<img src="https://github.com/enriconunes/AplicacaoWeb_criptoanalise_Nodejs/assets/75801762/e97dab11-f0ed-40a9-9453-e91b772e70e4" />
