![kittycash.io logo](https://avatars1.githubusercontent.com/u/34572254?s=200&v=4)

# kittycash.io

## Setup

1. Install [nvm](https://github.com/creationix/nvm).

2. Install and use the node version specified in `.nvmrc`:

  ```shell
  $ nvm install && nvm use
  ```

3. Install Yarn:

  ```shell
  $ npm install -g yarn
  ```

4. Install dependencies:

  ```shell
  $ yarn
  ```

## Build

```shell
$ yarn build
```

## Development

Start the development server:

```shell
$ yarn start
```

Run tests:

```shell
$ yarn test

# Generate coverage report
$ yarn test -- --coverage
```

## Releasing to production

Commits on the master branch will be automatically deployed to https://staging.kittycash.io.

To deploy in production (https://kittycash.io):

1. Bump version number in `package.json`:

    ```diff
       "name": "kittycash.io",
    -  "version": "0.0.0",
    +  "version": "0.0.1",
       "private": true,
    ```
2. Commit, create a tag, and push:

    ```shell
    $ git commit -am "chore: bump version number"
    $ git tag v0.0.1
    $ git push origin master --tags
    ```