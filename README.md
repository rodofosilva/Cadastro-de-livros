# 📚 Cadastro de Livros — Supabase + Lovable

Projeto desenvolvido para demonstrar o uso do **Supabase** como backend e **Lovable** (ou Lovable) como front-end visual, implementando um CRUD completo de **livros** com categorias e autores.

---

## 🚀 Funcionalidades
- Cadastro, edição e exclusão de livros
- Relacionamento entre livros e categorias
- View agregada com informações de autor, status e preço
- Funções e procedures em PL/pgSQL
- Conexão do front-end com Supabase
- Interface visual criada no Lovable

---

## 🗃️ Estrutura do Banco de Dados

Tabelas principais:
- **categorias** → id, nome, descrição  
- **livros** → id, título, autor, ano_publicacao, preço, categoria_id  

Relacionamento:  
`livros.categoria_id → categorias.id`

---

## 🧩 Scripts SQL

1. **`01_schema.sql`** – Criação das tabelas  
2. **`02_inserts.sql`** – Dados iniciais de exemplo  
3. **`03_functions.sql`** – Funções e procedures  
4. **`04_views.sql`** – Views agregadas

Todos os arquivos podem ser executados diretamente no **SQL Editor do Supabase**.

---

## 💾 Configuração no Supabase

1. Crie um novo projeto no [Supabase](https://supabase.com).  
2. Acesse a aba **SQL Editor** e cole o conteúdo de `01_schema.sql`.  
3. Execute também `02_inserts.sql`, `03_functions.sql` e `04_views.sql`.  
4. Copie a **URL do projeto** e a **anon key**.  
5. No Lovable, conecte usando essas credenciais para consumir os dados.

---

## 💻 Interface (Lovable)

- Página **Listagem de Livros** – mostra todos os livros com título, autor, categoria e preço.  
- Página **Cadastro/Edição** – formulário para adicionar ou atualizar livros.  
- Página **Detalhes** – exibe dados completos do livro.  

Use a **view** ou os **endpoints REST do Supabase** para preencher os componentes.

---

## 📷 Prints do Sistema
| Tela | Imagem |
|------|--------|
| Listagem | ![Listagem](docs/print_tela_listagem.png) |
| Cadastro | ![Cadastro](docs/print_tela_cadastro.png) |
| Detalhes | ![Detalhes](docs/print_tela_detalhes.png) |

---

## 🧮 Exemplo de View e Função
**View:** `vw_livros_categorias`  
**Função:** `sp_insert_livro(p_titulo, p_autor, p_categoria_id, p_preco)`

Essas estruturas permitem exibir dados combinados e inserir registros de forma programática via RPC.

---

## 📹 Vídeo de Apresentação
Demonstração das telas e do banco de dados:  
🎥 [Assista aqui](video/apresentacao.mp4)

---

## 👨‍💻 Autor
Desenvolvido por [Seu Nome].  
Projeto acadêmico — Banco de Dados / Desenvolvimento Web.
