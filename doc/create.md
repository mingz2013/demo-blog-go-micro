```bash

cd demo-go-micro

touch Makefile
touch docker-compose.yaml

mkdir srv api fnc web

mkdir doc
touch doc/create.md
touch doc/doc.md

micro new -h

cd srv
micro new post --gopath=false
micro new user --gopath=false

cd ..
cd api
micro new post --gopath=false --type="api"
micro new user --gopath=false --type="api"

cd ..
cd web
micro new blog --gopath=false --type="web"
micro new dashboard --gopath=false --type="web"
micro new super --gopath=false --type="web"
```


