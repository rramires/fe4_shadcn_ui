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


