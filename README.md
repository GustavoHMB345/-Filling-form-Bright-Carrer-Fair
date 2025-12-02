# Bright Career Fair 2026 - Sistema de Inscrição 🚀

Uma landing page moderna, responsiva e integrada para a feira de carreiras "Bright Career Fair 2026". Este projeto permite que alunos se inscrevam em workshops de diferentes áreas do conhecimento, com controle de vagas em tempo real utilizando o Google Sheets como banco de dados.

## ✨ Funcionalidades

* **Design Responsivo:** Layout fluido que se adapta perfeitamente a celulares, tablets e computadores.
* **Interface Atraente:** Uso de cores vibrantes (tema Laranja/Roxo), animações suaves e Glassmorphism.
* **Controle de Vagas em Tempo Real:** O sistema consulta o Google Sheets para verificar quantas vagas restam para cada área (Limite configurado: 20 alunos).
* **Bloqueio Automático:** Áreas esgotadas ficam visualmente desabilitadas e não permitem novas seleções.
* **Backend Serverless:** Utiliza Google Apps Script e Google Sheets, sem custos de servidor tradicional.
* **Feedback ao Usuário:** Notificações (Toasts) de sucesso ou erro e indicadores de carregamento.

## 🛠️ Tecnologias Utilizadas

* **Frontend:** HTML5, JavaScript (ES6+), Tailwind CSS (via CDN).
* **Backend:** Google Apps Script.
* **Banco de Dados:** Google Sheets.
* **Hospedagem (Sugerida):** GitHub Pages.

---

## ⚙️ Configuração e Instalação

Siga os passos abaixo para colocar o projeto no ar.

### 1. Configurando o Backend (Google Sheets)

1. Crie uma nova **Planilha Google** em branco.
2. Vá no menu **Extensões** > **Apps Script**.
3. Apague qualquer código existente no arquivo `Código.gs` (ou `Code.gs`) e cole o código do backend fornecido no projeto.
4. Clique em **Salvar**.
5. Clique no botão azul **Implantar** (Deploy) > **Nova implantação**.
6. Clique na engrenagem ⚙️ e selecione **App da Web**.
7. Preencha as configurações:
   * **Descrição:** Backend Inscrições.
   * **Executar como:** *Eu* (seu email).
   * **Quem pode acessar:** **Qualquer pessoa** (Isso é essencial para o site funcionar publicamente).
8. Clique em **Implantar** e copie a **URL do App da Web** gerada (ela termina em `/exec`).

### 2. Configurando o Frontend

1. Certifique-se de ter os arquivos `index.html` e `logo.jpg` na mesma pasta.
2. Abra o arquivo `index.html` em um editor de código.
3. Localize a seção de script no final do arquivo e encontre a variável `SCRIPT_URL`.
4. Cole a URL que você copiou no passo anterior:
   ```javascript
   // Cole sua URL aqui dentro das aspas
   const SCRIPT_URL = "[https://script.google.com/macros/s/SEU_ID_DO_SCRIPT/exec](https://script.google.com/macros/s/SEU_ID_DO_SCRIPT/exec)";
