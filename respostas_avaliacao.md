# Mundos de Patas: respostas da avaliação

Projeto do bimestre (Núcleo Comum) · Trilha 3: Diário de Pets e Enciclopédia de Raças

> Os pontos marcados com ✏️ dependem do que o grupo viver ao testar o app. Completem com o que aconteceu de verdade antes de apresentar.

## 1. Quais foram os comandos (prompts) usados pelo grupo? O primeiro funcionou de primeira?

**Prompt usado (resumo):** usamos o modelo do cardápio de projetos, adaptado para o nosso app:

> Atue como um desenvolvedor web front-end sênior e professor de programação para o Ensino Médio. Quero criar uma aplicação web chamada **Mundos de Patas**, que funciona como um diário de cuidados de pets (vacina, banho, controle de ração) com uma enciclopédia ilustrada de raças de cães e gatos, para donos de pets. Regras: arquivo único HTML; design moderno e responsivo; fetch() com async/await na TheDogAPI, TheCatAPI e Dog CEO API, com loading e tratamento de erros; FullCalendar via CDN; localStorage para salvar pets, agenda e favoritos; código comentado em português.

**Funcionou de primeira?** O primeiro comando gerou um app completo e organizado em três abas (Diário, Agenda e Enciclopédia). Mesmo assim, é preciso abrir no navegador e testar cada função. ✏️ Anotem aqui o que precisou ser corrigido ou detalhado depois (por exemplo: "pedimos para deixar o botão de favoritar mais visível").

## 2. O que a IA errou durante a criação? Como o grupo descobriu e consertou?

Pontos em que uma IA costuma errar nesse tipo de projeto, e que o grupo deve **verificar na prática**:

- **Endereços e formato das APIs.** A IA escreve endereços e nomes de campos de memória. Conferimos na documentação oficial (thedogapi.com, thecatapi.com, dog.ceo/dog-api) e no console do navegador (F12 → Console/Rede). Exemplo: cães trazem a foto em `image.url`, mas gatos trazem apenas `reference_image_id`, e a foto precisa ser montada a partir dele.
- **Dados incompletos.** Algumas raças vêm sem foto, sem peso ou sem origem. O código precisa mostrar "Não informado" em vez de quebrar.
- **Biblioteca e idioma.** O FullCalendar aparece em inglês se o arquivo de idiomas não for carregado. Conferir se o calendário está em português.
- **Segurança do código.** Textos digitados pelo usuário e textos vindos de APIs não podem ser inseridos no HTML sem tratamento, por isso o código usa a função `esc()`.
- **Não testado ao vivo pela IA.** A IA que gerou o código não conseguiu abrir o app com internet. Por isso, o teste final com as APIs reais é responsabilidade do grupo. ✏️ Anotem qualquer erro que aparecer e como o grupo descobriu (console do navegador, dado faltando, botão que não respondia) e como corrigiu.

## 3. Quais cuidados éticos são necessários? Notamos padrões, estereótipos ou vieses?

**Cuidados éticos**

- **Não confiar cegamente.** O código e os textos da IA precisam ser revisados e testados antes de serem apresentados como nossos.
- **Transparência.** Informar que a IA ajudou a criar o projeto e citar as fontes dos dados (TheDogAPI, TheCatAPI, Dog CEO API) e da biblioteca (FullCalendar).
- **Saúde do animal.** O app é um organizador, **não substitui o veterinário**. Datas de vacina, quantidade de ração e cuidados devem seguir a orientação de um profissional.
- **Privacidade.** Os dados ficam somente no navegador do usuário (localStorage) e nada é enviado a servidor próprio. Evitar pedir dados pessoais do tutor.
- **Direitos de imagem.** As fotos vêm das próprias APIs e não são armazenadas nem revendidas.
- **Bem-estar animal.** Incentivar adoção e posse responsável, não a compra por aparência.

**Padrões, estereótipos e vieses**

- **Raças populares ganham mais destaque.** As bases de dados tendem a ter mais fotos e informações de raças famosas, enquanto cães sem raça definida (vira-latas) e gatos comuns quase não aparecem.
- **Estereótipos de temperamento.** Descrever uma raça inteira com adjetivos como "agressivo" ou "dócil" generaliza: cada animal tem personalidade própria e depende de criação e socialização.
- **Viés geográfico.** As descrições vêm de bases majoritariamente em inglês e do Hemisfério Norte, com pouca presença de raças brasileiras (como o Fila Brasileiro).
- ✏️ Acrescentem exemplos que o grupo notou ao usar a enciclopédia (por exemplo, quais raças ficaram sem foto ou sem informação).
