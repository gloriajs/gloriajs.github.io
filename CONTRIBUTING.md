---
url: /contributing/
---
# CONTRIBUTING

Contributions in the form of ideas, designs, and code are always welcome no matter how large or small. If you want to help but are not sure where to start, you can check out our project's [Issues](https://github.com/gloriajs/gloria/issues).

## Setup

We do use Yarn in this project, so:

> Install yarn: https://yarnpkg.com/en/docs/install

Afterward, clone our repository:

```sh
$ git clone https://github.com/gloriajs/gloria.git
$ cd gloria/
$ yarn
```

When adding a new dependency to our project, we use `yarn add [package name]` rather than `npm install [--save or --save-dev] [package name]`. It keeps our `yarn.lock` file (and therefore our dependencies) consistent across all our contributors.

## Running locally

Run `npm link` inside the root folder to use your local development `gloria` instead of the globally installed one.

or just use `node`:

```sh
$ node bin/gloria [command]
```

## Testing

```sh
$ npm test
```

## Pull Requests

We actively welcome any pull requests that are backed up by current issues or by some small summary explaining what it is you're contributing.

1. Fork the repo and create a branch from your fork's `master`. Name the branch after what it is you're doing, like `fixing-server` or `adding-voice-support`.
2. If you've added code that should be tested, add tests to the `test/` directory.
3. If you've changed APIs, update the documentation.
4. Ensure the test suite passes.
5. Make sure your code lints.

## License

By contributing to Gloria, you agree that your contributions will be licensed
under its [Apache license](LICENSE).

#Branchin Strategies

We recommend using the git flow method, to know what type of code is going in every branch.

Installing the addon [git flow](https://github.com/nvie/gitflow) will facilitate this.

#Code styles

We use jsc to make sure the style in the code is similar across every developer.

Arbitrarily we decided to use the airbnb style guide. You can learn more about it
[in their github repo](https://github.com/airbnb/javascript).

Look at our [.jscrc file](https://github.com/gloriajs/gloria/blob/master/.jscsrc).

Pull requests that don't adhere to the code style will probably get rejected, or commented with
some advice.

The code style includes things like how to do indentation, how to declare variables, allowed
capitalization, etc.

#Testing Pull Requests

A great way to contribute too is to look at the pull requests opened by other contributors.

To check out locally the code pushed by others, look at this
[guide put together by github](https://help.github.com/articles/checking-out-pull-requests-locally/).
