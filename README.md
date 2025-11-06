# Tutorial Shadcn UI

Tutorial to configure:  
Shadcn UI

- IMPORTANTE !

    Esse tutorial é uma continuação da configuração do front-end usando React com TypeScript usando o Vite.  
     Antes deve ser concluído esse outro tutorial, para instalando e configurando o Vite, Prettier, etc:  
     [Tutorial React + Code Format](https://github.com/rramires/fe1_react_code-format/blob/master/README.md)

    Seguido do tutorial para instalação do React Router DOM:  
     [Tutorial React + React Router DOM](https://github.com/rramires/fe2_react-router-dom/blob/master/README.md)

    Por último execute o tutorial para a instalação do Tailwind CSS:  
     [Tutorial React + Tailwind CSS](https://github.com/rramires/fe3_tailwind/blob/master/README.md)

---

### Instalação e configuração do Shadcn-UI

1 - Instale o Shadcn-UI:

```sh
pnpm dlx shadcn@latest init
```

Selecione o tom de cinza preferido:  
[ui.shadcn/colors](https://ui.shadcn.com/colors)

Gostei do mais puxado pro azul:  
✔ Slate

2 - Vá até o arquivo **global.css** e veja que foi adicionado bastante css do ShadcnUI e veja que contém alguns erros na aba PROBLEMS.

Para resolver adicione a extensão de PostCSS no VSCode:  
[PostCSS Language Support](https://marketplace.visualstudio.com/items?itemName=csstools.postcss)

- Com isso os erros devem desaparecer.

3 - Vá até o arquivo **lib/utils.ts** e veja que tem alguns erros, devido ao plugins que instalamos para organizar os imports.
Para resolver basta salvar o arquivo, que o plugin vai formatar.

- Com isso esses erros devem desaparecer.

---

### Instalação de um component para teste

1 - Para testar, instale um component, por exemplo o button:  
[ui.shadcn/button](https://ui.shadcn.com/docs/components/button)

```sh
pnpm dlx shadcn@latest add button
```

- Perceba que foi criado uma pasta, **components** e dentro dela, outra **ui**, e um arquivo **button.tsx**, que é o botão, que acabou de ser instalado.
- Essa é uma das maiores vantagens do Shadcn-UI. Trazer o código do component para dentro do projeto, podendo ser customizado se necessário.

- Abrindo o **button.tsx**, veja os 2 erros na aba PROBLEMS. O primeiro é de organização dos imports.  
   O segundo é na exportação do component que está assim **export { Button, buttonVariants }**.  
  Para o Fast Refresh do React, o correto seria separar em 2 arquivos, um para o component **Button** e outro para **buttonVariants** e fazer a importação do buttonVariants em Button.  
  Mas fica muito trabalhoso, fazer isso em cada component que instalarmos do Shadcn-UI. Então uma solução é desativar essa checagem.

2 - Vamos sobrescrever algumas regras no **eslint.config.js**, para desativar as checagens dentro da pasta **components/ui**:

```js
// depois do array extends:[], adicione
overrides: [
    {
        files: [
            'src/components/ui/**/*.tsx',
            'src/components/ui/**/*.ts',
        ],
        rules: {
            'react-refresh/only-export-components': 'off',
        },
    },
],
```

- Com isso esses erros devem desaparecer.

---

### Uso do component

1 - Adicione na página **dashboard.tsx**, um botão:

```js
// adicione
import { Button } from '@/components/ui/button'
```

```js
// adicione
<Button variant='outline'>Teste</Button>
```

2 - Rode a aplicação:

```sh
pnpm dev
```

- Com isso a instalação e configuração de praticamente tudo para iniciar um projeto FrontEnd está concluída.
- Bastando agora adicionar os components necessários:  
  [Shadcn-UI Components](https://ui.shadcn.com/docs/components)
