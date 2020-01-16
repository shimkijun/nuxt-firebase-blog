# blog 만들기
 
> Nuxt &amp; Firebase blog  
 https://nuxt-blog-c1774.web.app/

## Build Setup

``` bash
# install dependencies
$ npm run install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

## nuxt.config.js || firebase key
```
apiKey: process.env.FIREBASE_APIKEY,
authDomain: process.env.FIREBASE_AUTHDOMAIN,
databaseURL: process.env.FIREBASE_DATABASEURL,
projectId: process.env.FIREBASE_PROJECTID,
storageBucket: process.env.FIREBASE_STORAGEBUCKET,
messagingSenderId: process.env.FIREBASE_MESSAGINGSENDERID,
appId: process.env.FIREBASE_APPId,
measurementId: process.env.FIREBASE_MEASURENTID
```

## 배포

```
npm run generate
firebase deploy
```