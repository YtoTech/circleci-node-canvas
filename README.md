# A Node Docker image for CircleCI with Canvas support

A Docker Node image, with [canvas](https://github.com/Automattic/node-canvas) support.

Intended to run tests relying on the canvas module.

The image is based on the pre-built CircleCI [lastest Node image](https://circleci.com/docs/2.0/circleci-images/#nodejs).

We simply add [Canvas dependencies](https://github.com/Automattic/node-canvas#installation) on top of it.

## Usage Example

You can then use the image in your CircleCI v2 configuration file `.circleci/config.yml`:

```
# Javascript Node CircleCI 2.0 configuration file
#
# Check https://circleci.com/docs/2.0/language-javascript/ for more details
#
version: 2
jobs:
  build:
    docker:
      - image: yoant/circleci-node-canvas

    working_directory: ~/repo

    steps:
      - checkout

      - run: yarn install

      # run tests with Canvas support on JSDOM!
      - run: yarn test

      [...]
```

## Credits & Contributions

Image by Yoan Tournade <yoan@ytotech.com>. Reach out on [Github](https://github.com/YtoTech/circleci-node-canvas) to make it better!

Y
