# Basic Docz example

## Using `create-docz-app`

```sh
npx create-docz-app docz-app-basic
# or
yarn create docz-app docz-app-basic
```

## Download manually

```sh
curl https://codeload.github.com/doczjs/docz/tar.gz/master | tar -xz --strip=2 docz-master/examples/basic
mv basic docz-basic-example
cd docz-basic-example
```

## Setup

```sh
yarn # npm i
```

## Run

```sh
yarn dev # npm run dev
```

## Build

```sh
yarn build # npm run build
```

## Serve built app

```sh
yarn serve # npm run serve
```

## deploy to heroku

1. create as a git repo and push the master branch

- `git init`
- `git add .`
- `git commit -m "initial commit"`
- `git remote add origin git@github.com:dunatron/docz-test.git`
- `git push -u origin master`

2. Create the App on heroku

- `heroku apps:create docz-test` which will output a git remote:
  - https://docz-test.herokuapp.com/ | https://git.heroku.com/docz-test.git
- take the new remote and run the following
- `git remote add heroku-docz-test https://git.heroku.com/docz-test.git`
- `git subtree push --prefix ./docz/dist heroku-docz-test master`
