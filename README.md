# BookVerse-web

O BookVerse é uma aplicação web para leitores. As páginas permitem criar uma conta, explorar a apresentação do projeto, consultar avaliações e manter os livros cadastrados.

## Páginas do projeto

### Página inicial — `index.html`

É a página de apresentação do BookVerse. Ela reúne links para as áreas de livros, resenhas e comunidade, além de uma seção com avaliações da comunidade. O botão “Explorar livros” leva à seção “Livros”, que apresenta o convite para explorar e compartilhar leituras; essa seção não exibe uma lista de livros.

### Cadastro de usuário — `cadastro.html`

Permite criar uma conta para acessar o BookVerse. A pessoa informa nome, e-mail, senha e confirmação da senha. O formulário verifica os dados, exige senha com pelo menos oito caracteres e letras e números, e não permite cadastrar novamente um e-mail já usado neste navegador.

Depois do cadastro, a conta é salva no armazenamento local do navegador e uma sessão é iniciada. Assim, os dados não são enviados a um serviço de cadastro central.

### Catálogo e cadastro de livros — `cadastro_livro.html`

O projeto não possui uma página independente de catálogo para visitantes. A tela `cadastro_livro.html` reúne o formulário de cadastro e a lista dos livros já cadastrados. Nessa lista, é possível consultar título, autor, gênero, ISBN e, quando informadas, descrição e capa. Também há opções para editar e excluir livros.

Para cadastrar uma obra, são informados título, autor, gênero e ISBN. A descrição é opcional, assim como a imagem da capa. O formulário valida o ISBN e impede que o mesmo ISBN seja cadastrado mais de uma vez. Ao salvar, o livro passa a aparecer na lista dessa tela e é armazenado no navegador, contribuindo para manter o catálogo local.

Essa página é destinada a administradores e solicita uma confirmação de acesso. O armazenamento de livros é local ao navegador, portanto os registros não formam um catálogo compartilhado entre diferentes pessoas ou dispositivos.

### Login — `login.html`

Permite entrar com o e-mail e a senha de uma conta cadastrada. Também oferece acesso à página de recuperação de senha.

### Recuperação de senha — `esqueci_senha.html`

Localiza uma conta pelo e-mail informado e permite definir uma nova senha na própria tela. O fluxo atual não envia e-mail: os dados da conta ficam no armazenamento local do navegador.

### Resenhas — `reviews.html`

Apresenta avaliações da comunidade. A tela permite consultar e filtrar avaliações, escolher um livro do catálogo e publicar uma nota e um texto sobre a leitura.

## Observação sobre os dados

As contas, sessões e livros são mantidos no `localStorage` do navegador. Isso serve para o funcionamento local da interface, mas não sincroniza os dados entre usuários ou dispositivos. A tela de resenhas utiliza a integração configurada no módulo de resenhas para carregar livros e avaliações.
