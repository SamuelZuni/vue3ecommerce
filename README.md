# vue-ecommerce

Tienda Online

## Entities

### Product

- name
- description
- price
- image

### Category

- name
- description

### Cart

- products: `[{productId: 1, quantity: 3}, {productId: 7, qantity: 5}]`

## Components

### ProductCard

## Pages

- / -> Todos los productos
- /category/5 -> Productos solo de categoría 5
- /cart -> Ver carrito de compras

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Type-Check, Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```
