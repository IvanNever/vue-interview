# test

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur).

## Type Support for `.vue` Imports in TS

TypeScript cannot handle type information for `.vue` imports by default, so we replace the `tsc` CLI with `vue-tsc` for type checking. In editors, we need [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) to make the TypeScript language service aware of `.vue` types.

1. Для авторизованого користувача в header має відображатись
   компонент AppLogout, а для неавторизованого - AppLogin.

2. При авторизації користувач вводить своє ім’я, яке має
   зберігатись між сесіями та відображатись в компоненті Logout.

3. При logout відповідно ім’я видаляється та користувач стає неавторизованим.

4. В main секції не авторизованому користувачу виводиться повідомлення
   про необхідність авторизації, а авторизованому - відображаються
   компоненти UsersControls та UsersList

5. Компонент UsersControls завантажує список usersList з відкритого API
   https://jsonplaceholder.typicode.com/users та відображає кількість
   завантажених користувачів. (використати store pinia)

6. В компоненті UsersList отримані дані користувачів відображаються
   в готовій таблиці.

7. При logout цей список користувачів має видалятись.
