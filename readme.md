# 📘 Estrelas do Amanhã — Formulário de Matrícula

Projeto de **formulário de matrícula escolar** desenvolvido com **HTML e CSS**, focado em **experiência do usuário, acessibilidade, organização de estilos e boas práticas de front-end**.

Este projeto simula o fluxo de inscrição de uma criança em uma escola de educação infantil, priorizando clareza visual, usabilidade e estrutura escalável de código.

## 🎯 Objetivo do Projeto

Criar um formulário completo e funcional que:

* Organize informações complexas de forma clara
* Utilize boas práticas de **HTML semântico**
* Aplique **CSS moderno e modular**
* Trabalhe corretamente com **inputs sensíveis**, como upload de arquivos
* Demonstre domínio de **layout, formulários e estados visuais**

## 🧩 Funcionalidades Implementadas

* 📄 **Formulário completo de matrícula**
* 🧒 Informações da criança
* 🏠 Endereço residencial
* 👤 Dados do responsável legal
* 🕒 Escolha de turno de estudo
* 🏀 Seleção de atividades esportivas
* 📎 Upload de certidão de nascimento
* ✅ Aceite de termos e política de privacidade

## 🧱 Estrutura do Projeto

```
📁 projeto
│
├── index.html
├── readme.md
│
├── 📁 styles
│   ├── index.css
│   ├── global.css
│   ├── layout.css
│   ├── forms.css
│   │
│   ├── 📁 fields
│   │   ├── input.css
│   │   ├── radio.css
│   │   ├── checkbox.css
│   │   ├── buttons.css
│   │   └── droparea.css
│
├── 📁 assets
│   ├── icons
│   ├── images
│   └── illustration.svg
```

## 🎨 Conceitos e Técnicas Aplicadas

### Layout

* Grid layout para dividir a aplicação em **Main + Aside**
* Apenas o conteúdo principal possui **scroll**
* Aside permanece fixo para reforço visual e institucional

```css
#app {
  display: grid;
  grid-template-columns: 51.25% 48.75%;
  height: 100vh;
  overflow: hidden;
}

main {
  overflow: auto;
}
```

### Formulário Seguro com Upload de Arquivos

Uso correto de formulário com upload:

```html
<form method="post" enctype="multipart/form-data">
```

➡️ Evita vazamento de dados e segue boas práticas de segurança.

### Estilização de Inputs e Estados

* Foco visual claro
* Estados de erro e validação
* Inputs desabilitados com feedback visual
* Compatibilidade com **Safari** usando `outline-offset`

```css
input:focus {
  outline: .25rem solid var(--surface-secondary);
  outline-offset: .1px;
}
```

### Customização do Input Date

Estilização do calendário usando pseudo-elemento WebKit:

```css
input[type="date"]::-webkit-calendar-picker-indicator {
  background: url("calendar.svg") center/contain no-repeat;
}
```

### Área de Upload (Drag & Drop)

* Input invisível sobre a área clicável
* Feedback visual ao hover
* Ícones dinâmicos

```css
.dropzone input {
  position: absolute;
  inset: 0;
  opacity: 0;
}
```

### Radio Buttons Personalizados

* Inputs nativos ocultos
* Estado visual controlado por `:has(:checked)`
* Feedback de hover e foco

```css
.radio-inner:has(:checked) {
  border: 2px solid var(--stroke-highlight);
}
```

## ♿ Acessibilidade

* Uso correto de `label for`
* Inputs focáveis
* Estados visuais claros
* HTML semântico
* Placeholder apenas como complemento (não substitui label)

## 🧪 Tecnologias Utilizadas

* **HTML5**
* **CSS3**

  * Grid
  * Flexbox
  * Pseudo-classes modernas
  * Variáveis CSS
* **Google Fonts (Poppins)**

## 📌 Observações Importantes

* Projeto **100% front-end**
* Não possui JavaScript ou backend
* Ideal para estudo, portfólio ou base para evolução futura
* Estrutura CSS preparada para fácil manutenção e escalabilidade

## 🚀 Possíveis Evoluções

* Validação com JavaScript
* Integração com API de CEP
* Persistência dos dados
* Responsividade mobile avançada
* Envio real do formulário

## 👩‍💻 Autoria

Projeto desenvolvido como parte do aprendizado em **Formação Full Stack**, com foco em **qualidade de código, organização e experiência do usuário**.


✨ *Porque cada momento de aprendizado conta.*
