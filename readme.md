# Starting a typescript project

* Assuming node and npm are installed on your operating system.
* Check by typing `node -v` and `npm -v` on console
## Install typescript globally

* On terminal
`sudo npm install -g typescript`

* Initiate a typescript project in a separate directory
`typescript --init`

* The above step should create a `tsconfig.json` file 

* Uncomment these two lines out of the several

```
"sourceMap": true,                     
"outDir": "dist",          // change from default-setting to dist
```

* Install tsLint globally by `sudo npm i tslint --g`
* Initalize your project using `tslint --init`

* Install koa by `npm i koa koa-router @types/koa @types/koa-router`

* create a `server.ts` file and put following contents

```
import Koa from "koa";
import Router from "koa-router";

const app = new Koa();
const router = new Router();

router.get("/*", async (ctx) => {
    ctx.body = "Hello World!";
});

app.use(router.routes());

app.listen(3000);

```

* On terminal `tsc` and then `node ./dist/index.js`
* This should start the server
* Go to browser and check url `localhost:3000` , this should probably say `Hello, World!`