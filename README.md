SERVE.JS

Multer: Biblioteca usada para lidar com uploads de arquivos, especialmente imagens.
storage: Define o local onde as imagens serão armazenadas e como serão nomeadas.
fileFilter: Controla o tipo de arquivos permitidos (neste caso, apenas imagens jpeg, png, e gif).
Rota /produtos/cadastrar: Insere um produto no banco de dados MySQL com campos como nome, preço, imagem e descrição.
Rota /produtos/listar: Faz uma consulta SQL para obter todos os produtos cadastrados na tabela produtos.
Se houver produtos, eles serão retornados no formato JSON, junto com uma mensagem de sucesso. Se nenhum produto for encontrado, uma mensagem de erro será retornada.
Rota /produto/editar/:id: Atualiza os dados de um produto, podendo ou não alterar a imagem.
Caso uma nova imagem seja fornecida, ela também será atualizada. Caso contrário, apenas o nome, preço e descrição serão alterados.
Rota /produto/excluir/:id: Exclui um produto da tabela produtos com base no seu id.
Se o produto não for encontrado, uma mensagem de erro será retornada.

Front.js

Formulário de Cadastro: Ao submeter o formulário, ele envia os dados (incluindo o arquivo de imagem) via fetch para o servidor, que processa e cadastra o produto.
Em caso de sucesso, o formulário é limpo e uma mensagem de sucesso é exibida. Caso contrário, uma mensagem de erro é exibida.

