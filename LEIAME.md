# Pixel Positions
Projeto final do curso **30 Days to Learn Laravel** do **Laracast**.


## Desenvolvimento 

- Criei subdiretório `images` em `resources`;
- Baixei o arquivo [logo.svg](https://github.com/laracasts/pixel-position/blob/main/resources/images/logo.svg); 
  e o coloquei em `resources/images`;
- Em `resources/js/app.js` eu adicionei referência para o diretório de imagens:
```javascript
// app.js
import './bootstrap';
import.meta.glob(['../images/**']);
```

- No terminal, executei o comando `npm run build` para gerar a pasta `build` (e seus arquivos) dentro de `public`.
- Criei diretório `components` em `resources/views`.
- Em `resources/views/components`, criei o arquivo `layout.blade.php`.
- Em `resources/views`, criei arquivo `home.blade.php` com `<x-layout>Home Page</x-layout>`.
- Em `routes/web.php`: 
  * alterei a rota da página `welcome` para `/welcome`;
  * adicionei a rota da página `home` para `/`.
- Acessei a página inicial da aplicação pela URL fornecida pelo Laravel Herd 
  `http://laracasts-laravel-pixel-positions.test/`.

![Image-01-LaravelHerd](./images/Image-01-LaravelHerd.png)

![Image-02-Home-v1](./images/Image-02-Home-v1.png)

- Verifiquei se o Tailwind está instalado conforme o 
  [guia](https://tailwindcss.com/docs/installation/framework-guides/laravel/vite):
  * Em `vite.config.js` deve ter `tailwindcss` importado no início e chamado em plugins:
```javascript
// ...
import tailwindcss from '@tailwindcss/vite';
export default defineConfig({
    plugins: [
        // ...
        tailwindcss(),
    ],
});
```
  * Em `resources/css/app.css` deve ter `@import 'tailwindcss';`.
  * Em `layout.blade.php` deve ter `@vite('resources/css/app.css')` ou 
    `@vite(['resources/js/app.js', 'resources/css/app.css'])`.


## Referências
Laracast - 30 Days to Learn Laravel
https://laracasts.com/series/30-days-to-learn-laravel-11

Laracast - From Design to Blade
https://laracasts.com/series/30-days-to-learn-laravel-11/episodes/27

Laracast - Blade and Tailwind Techniques for Your Laravel Views
https://laracasts.com/series/30-days-to-learn-laravel-11/episodes/28

Laracast - Jobs, Tags, TDD, Oh My!
https://laracasts.com/series/30-days-to-learn-laravel-11/episodes/29

Laracast - The Everything Episode
https://laracasts.com/series/30-days-to-learn-laravel-11/episodes/30

Tailwind - Docs - Installation - Framework guides - Laravel
https://tailwindcss.com/docs/installation/framework-guides/laravel/vite
