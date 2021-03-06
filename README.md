![header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=200&section=header&text=DJ%20Event%20Page%20With%20NEXT.JS&fontSize=60&animation=fadeIn)

# ๐ DJ Events Page with Next.js & Strapi

## ๐น Project Function

> - ๋ก๊ทธ์ธ / ํ์๊ฐ์
> - ์ด๋ฒคํธ ํ์ด์ง ์ถ๊ฐ / ์ด๋ฏธ์ง ์๋ก๋
> - ์ด๋ฒคํธ ํ์ด์ง ์์  / ์ญ์  (์ฌ์ฉ์ ์ผ ๊ฒฝ์ฐ)
> - JWT ํ ํฐ ํด๋ ์ถ๊ฐ & ๊ฒ์ฆ
> - ํ์ด์ง๋ค์ด์
> - google map์ผ๋ก ์ด๋ฒคํธ ์ฅ์ ๋ธ์ถ

## ๐น Packages

```javascript
  "name": "dj-event-page-width-next",
  "dependencies": {
    "axios": "^0.26.1",
    "cookie": "^0.4.2",
    "lodash": "^4.17.21",
    "mapbox-gl": "^2.7.1",
    "moment": "^2.29.1",
    "next": "12.1.0",
    "qs": "^6.10.3",
    "react": "17.0.2",
    "react-dom": "17.0.2",
    "react-geocode": "^0.2.3",
    "react-icons": "^4.3.1",
    "react-map-gl": "^7.0.10",
    "react-toastify": "^8.2.0",
    "sass": "^1.49.9"
  },
    "devDependencies": {
    "eslint": "8.11.0",
    "eslint-config-next": "12.1.0"
  }
```

## ๐น Directory Config

- `components`
- `config`
- `context`
- `helpers`
- `pages`
- `public`
- `styles`

### โผ Directory Rules

#### โฝ Components

**example) Header Component**

- `components`
  - `Header`
    - `index.js`
    - `Header.module.scss`

#### โฝ CSS

CSS๋ SCSS ์ ์ฒ๋ฆฌ๊ธฐ๋ฅผ ์ฌ์ฉํ์ผ๋ฉฐ, ์ปดํฌ๋ํธ์ ๊ฒฝ์ฐ `Directory_name.module.scss` ๋ก ๋ชจ๋ scss๋ฅผ ์ฌ์ฉํ์ผ๋ฉฐ, input, btn์ ํ๋ก์ ํธ์ ํฌ๊ธฐ๊ฐ ํฌ์ง ์์ `global.scss`, ํ์ด์ง์ ๊ฒฝ์ฐ `pages.scss`๋ฅผ ์์ฑํด `_app.js`์์ import ํ์.

## ๐น ์ ์ญ state

### โผ useContext ์ฌ์ฉ

` context/AuthContext.js` ์์ฑํด์, App์ ๊ฐ์ธ์ ์ฌ์ฉํจ.
์ปดํฌ๋ํธ props๋ฅผ ๋ง์ด ํ๊ณ  ๋ค์ด๊ฐ๋ ๋ก๊ทธ์ธ / ํ์๊ฐ์ / user ์ ๋ณด๋ฅผ state์ ์ ์ฅํจ.

```javascript
const { user, error, login, logout, checkUser, register } = useContext(AuthContext);
```

## ๐นBackend ์ฒ๋ฆฌ

### โผ Strapi CMS ํ๋ ์์ํฌ ์ฌ์ฉ

<a  href="https://strapi.io/">๐ Strapi ๊ณต์ ํํ์ด์ง </a>

> **Strapi๋?**
>
> - Bootstrap + API๋ฅผ ์ค์ฌ์ Strapi๋ผ๊ณ  ํ๋ค. Strapi๋ Node.js ์น ํ๋ ์์ํฌ ์ค ํ๋์ธ Koa ๊ธฐ๋ฐ์ผ๋ก ๊ตฌํ๋์์ผ๋ฉฐ, ํ ์ปค์คํฐ๋ง์ด์ง์ด ๊ฐ๋ฅํ ๊ฐ๋ฐ์ ์ฐ์ (Developer-first) ์คํ์์ค Headless CMS์ด๋ค.

### โผ Heroku ๋ฐฐํฌ

<a  href="https://dashboard.heroku.com/apps">๐ช๐ป Heroku ๊ณต์ ํํ์ด์ง </a>

> **Heroku๋?**
>
> - Heroku๋ Java, Node.js, Python๋ฑ ์ฌ๋ฌ ์ธ์ด๋ฅผ ์ง์ํ๋ ํด๋ผ์ฐ๋ Paas(Platform as a Service, PaaS). ํด๋ผ์ฐ๋ ์ปดํจํ ์๋น์ค ๋ถ๋ฅ ์ค ํ๋์.

### โผ Cloudinary Image Upload

<a  href="https://cloudinary.com/">๐ผ Cloudinary ๊ณต์ ํํ์ด์ง </a>

> **Cloudinary๋ ?**
>
> - Cloudinary๋ ํด๋ผ์ฐ๋ ๊ธฐ๋ฐ์ ์ด๋ฏธ์ง ๋ฐ ๋น๋์ค ๊ด๋ฆฌ ์๋น์ค.
