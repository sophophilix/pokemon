## Vite + React + JavaScript + Linters

## Summary

This project uses several powerful tools and libraries to streamline development and improve code quality.

To quickly build and optimize the application, Vite is used as a fast and flexible build tool. It supports hot module replacement and optimized builds, making the development process smooth and efficient.

To ensure consistent code style and catch potential errors, the project also employs ESLint, and eslint-airbnb-config. Additionally, Prettier is utilized for automatic code formatting, improving code readability and maintainability.

To perform unit testing, the project utilizes Vitest, jsdom, and @testing-library, allowing for thorough and efficient testing of the application.

Finally, for declarative routing, React Router v6 is utilized, simplifying the navigation process and enhancing user experience. Overall, these tools combine to create a robust and efficient development environment.

## Setting up Vite for ReactJS Development

Vite is a powerful and efficient build tool that streamlines development for modern web applications. The following guide will walk you through how the project utilizes Vite to take advantage of its lightning-fast build times and advanced features.

### Prerequisites

Before starting, make sure you have Node.js installed on your system. You can download and install Node.js from the official website here.

#### Step 1: Creating a New React Project with Vite

To create a new React project with Vite, use the following command:

```bash
npm create vite@latest test0002 -- --template react --framework react --variant js
```

The command `npm create vite@latest test0002 -- --template react --framework react --variant js` creates a new project using the latest version of Vite with the React template.

- The `create` command is used to create a new package or project, and in this case, we're creating a new Vite project with the name test0002.
- The vite@latest argument specifies that we want to use the latest version of Vite.
- The --template react argument tells Vite to use the React template.
- The --framework react argument specifies that we're using React as our framework, and
- the --variant js argument specifies that we're using JavaScript as our language.

#### Step 2: Starting the Development Server

After creating the project, navigate to the project directory and start the development server with the following commands:

```bash

cd my-react-app
npm install
npm run dev
```

This will install any dependencies and start the development server.

## How to Disable a Linter Rule in Your React Code

Linter rules help maintain consistent and error-free code by analyzing your code for common mistakes and enforcing coding standards. However, there may be situations where you want to disable a specific linter rule for a certain piece of code. This can be done using the following steps:

- Identify the Linter Rule to Disable

To disable a linter rule, you first need to know its name. You can usually find this by hovering over the squiggly line in your code editor that indicates an issue with your code. The tooltip that appears should display the name of the linter rule.

- Use Inline Rule Disabling

Once you have identified the name of the linter rule you want to disable, you can use inline rule disabling to turn off the rule for a specific line or block of code. To do this, add the following comment above the line or block of code where you want to disable the rule:

```java

// eslint-disable-next-line <rule-name>
```

Replace <rule-name> with the name of the linter rule you want to disable. For example, if you want to disable the react/react-in-jsx-scope rule, your comment should look like this:

```java

// eslint-disable-next-line react/react-in-jsx-scope
```

- Add Rule to .eslintrc.cjs File

If you need to disable the same linter rule across multiple files, you can add the rule to your .eslintrc.cjs file instead of using inline rule disabling. To do this, add the rule to the rules section of the file, setting its value to 0. For example, to disable the react/react-in-jsx-scope rule, your .eslintrc.cjs file should look like this:

```java

module.exports = {
  // other config options
  rules: {
    'react/react-in-jsx-scope': 0,
    // other rules
  },
};
```

**Note** that this will disable the rule for your entire project, so use with caution.

By following these steps, you can disable specific linter rules as needed to improve the readability and maintainability of your code.

Steps

- npm i -D eslint
- npx eslint --init
- npx install-peerdeps --dev eslint-config-airbnb
- npm i -D prettier eslint-config-prettier eslint-plugin-prettier

Clone the repository:

```bash

git clone https://github.com/your-username/your-project.git
```

## Install the dependencies:

### eslint

```bash

npm i -D eslint

added 96 packages, and audited 180 packages in 6s

32 packages are looking for funding
  run `npm fund` for details


```

```json
{
  "name": "react-template",
   ..truncated
  },
  "dependencies": {
     ..truncated

  },
  "devDependencies": {
    ..truncated

    "eslint": "^8.36.0",

  }
}


```

```bash

npx eslint --init

You can also run this command directly using 'npm init @eslint/config'.
✔ How would you like to use ESLint? · problems
✔ What type of modules does your project use? · esm
✔ Which framework does your project use? · react
✔ Does your project use TypeScript? · No / Yes
✔ Where does your code run? · browser
✔ What format do you want your config file to be in? · JavaScript
The config that you've selected requires the following dependencies:

eslint-plugin-react@latest
✔ Would you like to install them now? · No / Yes
✔ Which package manager do you want to use? · npm
Installing eslint-plugin-react@latest

added 62 packages, and audited 247 packages in 7s

82 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
A config file was generated, but the config file itself may not follow your linting rules.
Successfully created .eslintrc.cjs file in /Users/donsantmajor/code/github.com/sophophilix/vite-starter/react-template001

```

```bash

cd your-project
npm install

    Start the development server:
```

```bash

npm run dev

    Open your web browser and navigate to http://localhost:3000. You should see your React app running!
```

### Install airbnb

- https://www.npmjs.com/package/eslint-config-airbnb-base

```bash

npx install-peerdeps --dev eslint-config-airbnb

Need to install the following packages:
  install-peerdeps@3.0.3
Ok to proceed? (y) y
npm WARN deprecated @babel/polyfill@7.12.1: 🚨 This package has been deprecated in favor of separate inclusion of a polyfill and regenerator-runtime (when needed). See the @babel/polyfill docs (https://babeljs.io/docs/en/babel-polyfill) for more information.
npm WARN deprecated core-js@2.6.12: core-js@<3.23.3 is no longer maintained and not recommended for usage due to the number of issues. Because of the V8 engine whims, feature detection in old core-js versions could cause a slowdown up to 100x even if nothing is polyfilled. Some versions have web compatibility issues. Please, upgrade your dependencies to the actual version of core-js.
install-peerdeps v3.0.3
Installing peerdeps for eslint-config-airbnb@latest.
npm install eslint-config-airbnb@19.0.4 eslint@^8.2.0 eslint-plugin-import@^2.25.3 eslint-plugin-jsx-a11y@^6.5.1 eslint-plugin-react@^7.28.0 eslint-plugin-react-hooks@^4.3.0 --save-dev

SUCCESS eslint-config-airbnb
  and its peerDeps were installed successfully.


```

### Why use Eslint-config-airbnb

Eslint-config-airbnb is a popular JavaScript style guide that helps developers maintain consistent coding styles and avoid common mistakes in their code. The Airbnb style guide is one of the most popular style guides for JavaScript, and the corresponding eslint configuration package makes it easy to enforce this style guide in any codebase.

Using a popular style guide like eslint-config-airbnb can be beneficial for several reasons. First, it can help improve the readability and maintainability of code by enforcing consistent formatting and organization practices. This can make it easier for developers to understand and work with the code, reducing confusion and errors.

Second, using a popular style guide can also help developers avoid common mistakes and best practices in their code. The Airbnb style guide, for example, provides guidelines for error handling, variable naming, and many other coding practices that can help write cleaner, more efficient code.

Finally, using a popular style guide can help developers stay up-to-date with best practices and trends in the industry. Because these style guides are frequently updated and maintained by a community of developers, they can help stay on top of new features and changes in the language, ensuring that code stays modern and relevant.

#### update .eslintrc.json to include airbnb

To make use of the Airbnb style guide, we add it to the `.eslintrc.json`

```bash
    ...truncated
    "extends": [
        "airbnb",
        "airbnb/hooks",
        "plugin:react/recommended"
    ],
```

#### install eslint extension to vscode

Name: ESLint
Id: dbaeumer.vscode-eslint
Description: Integrates ESLint JavaScript into VS Code.
Version: 2.4.0
Publisher: dbaeumer
VS Marketplace Link: https://open-vsx.org/vscode/item?itemName=dbaeumer.vscode-eslint

### install prettier

```bash
npm i -D prettier eslint-config-prettier eslint-plugin-prettier

added 5 packages, and audited 286 packages in 2s

93 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```

The command npm i -D prettier eslint-config-prettier eslint-plugin-prettier installs three packages as devDependencies in your project:

- `prettier`: Prettier is a code formatter that automatically formats your code to ensure consistency in style, formatting, and readability.

- `eslint-config-prettier`: This package provides a configuration for ESLint that disables all rules that conflict with Prettier, so that ESLint doesn't report any errors or warnings that conflict with Prettier's formatting rules.

- `eslint-plugin-prettier`: This package provides a plugin for ESLint that adds a new rule to ESLint, called prettier/prettier, which checks your code against Prettier's formatting rules and reports any formatting errors or warnings.

By installing these packages and configuring ESLint to use them (which we did in step 4 of the setup), you can ensure that your code is formatted consistently and without any conflicts between ESLint and Prettier.

## prettierr config file

### Setting up Prettier Configuration for a Project

Prettier is a code formatting tool that ensures consistent code style and formatting across a project. To maintain a clean and readable codebase, Prettier configuration is utilized in the project. Follow these steps to set it up:

#### Step 1: Install Prettier

Install Prettier as a development dependency in the project by running the following command:

```bash

npm install --save-dev prettier
```

#### Step 2: Configure Prettier

Create a prettier.config.cjs file in the root of the project directory and add the desired configuration. For example:

```js
module.exports = {
  trailingComma: 'es5',
  tabWidth: 2,
  semi: true,
  singleQuote: true,
};
```

This configuration specifies that code should have a trailing comma in object literals, use 2 spaces for indentation, use semicolons, and single quotes instead of double quotes for strings.

#### Step 3: Integrate Prettier with Your Code Editor

Integrate Prettier with the code editor to streamline the development workflow. Many popular code editors such as Visual Studio Code and Sublime Text have extensions that integrate Prettier.

### Difference between .prettierrc.json and .prettierrc.cjs

The main difference between .prettierrc.json and .prettierrc.cjs is the file format and how it is loaded by Prettier.

.prettierrc.json is a JSON file and is loaded by Prettier in a synchronous manner. It is a simple way to configure Prettier's formatting options using a JSON file.

On the other hand, .prettierrc.cjs is a CommonJS module file and is loaded by Prettier in an asynchronous manner. This allows you to write more complex configuration code, using JavaScript and Node.js modules, to customize Prettier's behavior.

Using .prettierrc.cjs is particularly useful when you need to dynamically generate Prettier configuration based on environment variables or other runtime values. It also allows you to write custom functions to manipulate the output of Prettier, such as using prettier.format to format code snippets in your application.

In summary, .prettierrc.json is a simple and straightforward way to configure Prettier, while .prettierrc.cjs provides more flexibility and advanced customization options.

<!-- ## Testing

This starter template includes a few testing tools to help you write robust and reliable code. Here are some resources to help you get started:

Using Testing Library + Jest DOM with Vitest
About Testing Library Queries
Common Mistakes with React Testing Library

This setup includes:

- [eslint](https://eslint.org/), [typescript-eslint](https://typescript-eslint.io/), [eslint-airbnb-config](https://github.com/airbnb/javascript), [prettier](https://prettier.io/)
- [vitest](https://vitest.dev/), [jsdom](https://github.com/jsdom/jsdom), [@testing-library](https://testing-library.com/)
- [react-router v6](https://reactrouter.com/en/main)


### Setup vitest

`npm install -D vitest`

```json
added 48 packages, and audited 334 packages in 22s

107 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

```
vitest is our test run , it will run and find all our tests in our project directories
we specifically need some utilites that will help us write test that will help test react components and [testing library](https://testing-library.com/docs/react-testing-library/intro/) is great for that.
jsdom helps us do things with dom with out a browser

the expectation that come with vite are not the best hence we will install jest-dom

### Setup testing library

```bash
npm install -D @testing-library/react

added 11 packages, and audited 345 packages in 6s

107 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```

#### Setup jest dom

```bash
npm install --save-dev @testing-library/jest-dom

added 86 packages, and audited 431 packages in 6s

109 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```

### setup tests

```bash

/* eslint-disable import/no-extraneous-dependencies */
import matchers from '@testing-library/jest-dom/matchers';
import { expect } from 'vitest';

expect.extend(matchers);

```

### rules for writing test

The test should sit next to the file we want to test example

if we want to test App.jsx
we will create App.test.jsx
by doing this we dont have to look all over for where the test file exists.

### example test

```js
import { describe, it } from 'vitest';
import { render, screen } from '@testing-library/react';
import { MemoryRouter } from 'react-router-dom';

import { WrappedApp, App } from './App';

describe('App', () => {
  it('Renders hello world', () => {
    // ARRANGE
    render(<WrappedApp />);
    // ACT
    // EXPECT
    expect(
      screen.getByRole('heading', {
        level: 1,
      })
    ).toHaveTextContent('Hello World');
  });
  it('Renders not found if invalid path', () => {
    render(
      <MemoryRouter initialEntries={['/this-route-does-not-exist']}>
        <App />
      </MemoryRouter>
    );
    expect(
      screen.getByRole('heading', {
        level: 1,
      })
    ).toHaveTextContent('Not Found');
  });
});

``` -->

## Testing

The project utilizes various testing tools to ensure reliable and robust code. These include:

- vitest,
- @testing-library/jest-dom, and
- @testing-library/react

To set up vitest, run the following command:

```bash
npm install -D vitest
```

This installs the necessary utilities to run tests in your project directories. The project utilizes the [testing library](https://testing-library.com/docs/react-testing-library/intro/) to help test React components. Additionally, jsdom allows for DOM manipulation without the use of a browser.

To install the @testing-library/react package, use the following command:

```bash
npm install -D @testing-library/react
```

The project also uses [@testing-library/jest-dom](https://github.com/testing-library/jest-dom#installation) to extend Jest's matchers.

To install, use the following command:

```bash

npm install --save-dev @testing-library/jest-dom
```

To use jest-dom matchers, add the following code snippet to your test file:

```js
/* eslint-disable import/no-extraneous-dependencies */
import matchers from '@testing-library/jest-dom/matchers';
import { expect } from 'vitest';

expect.extend(matchers);
```

To ensure consistency and maintainability, the project follows these rules when writing tests:

- The test file should sit next to the file being tested. For example, to test App.jsx, create a App.test.jsx file in the same directory.
- Follow the testing library queries for better test reliability and maintainability.

Here is an example test file:

```js
import { describe, it } from 'vitest';
import { render, screen } from '@testing-library/react';
import { MemoryRouter } from 'react-router-dom';

import { WrappedApp, App } from './App';

describe('App', () => {
  it('Renders hello world', () => {
    // ARRANGE
    render(<WrappedApp />);
    // ACT
    // EXPECT
    expect(
      screen.getByRole('heading', {
        level: 1,
      })
    ).toHaveTextContent('Hello World');
  });
  it('Renders not found if invalid path', () => {
    render(
      <MemoryRouter initialEntries={['/this-route-does-not-exist']}>
        <App />
      </MemoryRouter>
    );
    expect(
      screen.getByRole('heading', {
        level: 1,
      })
    ).toHaveTextContent('Not Found');
  });
});
```

This test file uses the describe and it functions from vitest and render and screen functions from @testing-library/react. The MemoryRouter component from react-router-dom is also utilized for routing.

## Contributing

If you find a bug or have an idea for a new feature, feel free to contribute to this project! Here's how:

Fork this repository.
Make your changes.
Open a pull request.

## License

This project is licensed under the MIT License.
