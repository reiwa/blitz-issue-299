# blitz-issue-299

```
$ npx blitz -v
You are using alpha software - if you have any problems, please open an issue here:
  https://github.com/blitz-js/blitz/issues/new/choose

macOS Catalina | darwin-x64 | Node: v12.11.1

blitz: 0.7.0 (global)
blitz: 0.7.0 (local)

$ node -v
v12.11.1

$ which node
/Users/reiwa/.nodebrew/current/bin/node

$ yarn -v
1.19.1

$ npx -v
6.12.0
```

Run on termial:

```
$ npx blitz new blitz-issue-299
$ cd blitz-issue-299
```

Edit `db/schema.prisma`

```
model Project {
  id        Int      @default(autoincrement()) @id
  name      String
}
```

Run on terminal:

```
$ yarn blitz db migrate
$ yarn start
```

Edit `app/pages/index.tsx`

```
import { Head, Link } from "blitz"
import db from 'db'

console.log(db)
```

Get the error message:

```
[ error ] /Users/reiwa/GitHub/blitz-issue-299/node_modules/@prisma/client/runtime/index.js
Module not found: Can't resolve 'child_process' in '/Users/reiwa/GitHub/blitz-issue-299/node_modules/@prisma/client/runtime'
```
