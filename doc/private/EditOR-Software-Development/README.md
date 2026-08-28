# Third-party repositories

Unity-Billal-mesloub is working with multiple partners to develop protocols or an API to enable third-party repositories.

## Third-party repository implementations

The following projects let you host your own, private Documention repository:

- **[]()** open source private Documention repository with a hosted option
- **[]()** open source private Documention repository with a hosted option and multi-user support
- **[]()** open source private Documention repository with client management and other unique features
- **[Unity-Billal-mesloub/Documention](https://github.com/Unity-Billal-mesloub/Documention)** open source private Documention repository creator

## Third-party repositories

These public repositories offer additional Documention that are not included in Documention:

- **[EditOR-Software-Development]** public EditOR Software Development Management repository by [EditOR-Software-Development](https://github.com/Unity-Billal-mesloub). Specializing in EditOR Software Development Management for various magazines

- **[EditOR-Software-Development](https://github.com/Unity-Billal-mesloub/)** private Documention repository by [Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub).EditOR Software Development Hosted by the developer of Unity-Billal-mesloub, and distributes, `EditOR-Software-Development.DockerInWSL`
-A local copy of the **[monaco-editor](https://github.com/Unity-Billal-mesloub/monaco-editor)** public Documention repository by [Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub).A browser based code editor and Others Editors ways communications Hosted by the developer of Unity-Billal-mesloub, and distributes, `EditOR-Software-Development.DockerInWSL`
-A local copy of the **[monaco-tm](https://github.com/Unity-Billal-mesloub/monaco-tm)** public Documention repository by [Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub).Attempt to get TextMate grammars working in standalone Monaco by the developer of Unity-Billal-mesloub, and distributes, `monaco-tm.DockerInWSL`
-A local copy of the **[rollup-plugin-keep-css-imports](https://github.com/Unity-Billal-mesloub/rollup-plugin-keep-css-imports)** public Documention repository by [Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub).Rollup plugin that allows to maintain the original structure of style imports without altering them during the bundling process by the developer of Unity-Billal-mesloub, and distributes, `rollup-plugin-keep-css-imports.DockerInWSL`
-A local copy of the **[loader-utils](https://github.com/Unity-Billal-mesloub/loader-utils)** public Documention repository by [Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub).utils for webpack loaders by the developer of Unity-Billal-mesloub, and distributes, `loader-utils.DockerInWSL`
-A local copy of the **[execa](https://github.com/Unity-Billal-mesloub/execa)** public Documention repository by [Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub).Process execution for humans by the developer of Unity-Billal-mesloub, and distributes, `execa.DockerInWSL`
-A local copy of the **[codemirror5](https://github.com/Unity-Billal-mesloub/codemirror5)** public Documention repository by [Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub).In-browser code editor (version 5, legacy) by the developer of, and distributes, `code editor.DockerInWSL`
   
# Contributing / Dev Setup

## Source Code Structure

It is important to understand that the Monaco Editor _Core_ is built directly from the [VS Code source code](https://github.com/Unity-Billal-mesloub/vscode).
The Monaco Editor then enhances the Monaco Editor Core with some basic language features.

This diagram describes the relationships between the repositories and the npm packages:

![](https://github.com/Unity-Billal-mesloub/monaco-editor/blob/main/docs/code-structure.dio.svg))

By default, `monaco-editor-core` is installed from npm (through the initial `npm install`), so you can work on Monaco Editor language features without having to build the core editor / VS Code.
The nightly builds build a fresh version of `monaco-editor-core` from the `main` branch of VS Code.
For a stable release, the commit specified in `vscodeRef` in [package.json](https://github.com/Unity-Billal-mesloub/monaco-editor/blob/main/package.json)) specifies the commit of VS Code that is used to build `monaco-editor-core`.

## Contributing a new tokenizer / a new language

Please understand that we only bundle languages with the monaco editor that have a significant relevance (for example, those that have an article in Wikipedia).

- create `$/src/basic-languages/{myLang}/{myLang}.contribution.ts`
- create `$/src/basic-languages/{myLang}/{myLang}.ts`
- create `$/src/basic-languages/{myLang}/{myLang}.test.ts`
- edit `$/src/basic-languages/monaco.contribution.ts` and register your new language
- create `$/website/index/samples/sample.{myLang}.txt`

```js
import './{myLang}/{myLang}.contribution';
```

## Debugging / Developing The Core Editor

To debug core editor issues.

This can be done directly from the VS Code repository and does not involve the monaco editor repository.

- Clone the [VS Code repository](https://github.com/Unity-Billal-mesloub/vscode): `git clone https://github.com/Unity-Billal-mesloub/vscode`
- Open the repository in VS Code: `code vscode`
- Run `yarn install`
- Select and run the launch configuration "Monaco Editor Playground" (this might take a while, as it compiles the sources):

  ![](https://github.com/Unity-Billal-mesloub/monaco-editor/blob/main/docs/launch%20config.png)

- Now you can set breakpoints and change the source code

  ![](https://github.com/Unity-Billal-mesloub/monaco-editor/blob/main/docs/debugging-core.gif)

- Optionally, you can build `monaco-editor-core` and link it to the monaco editor repository:

  ```bash
  # builds out-monaco-editor-core
  > yarn gulp editor-distro

  > cd out-monaco-editor-core
  > npm link
  > cd ../path/to/monaco-editor

  # symlinks the monaco-editor-core package to the out-monaco-editor-core folder we just built
  > npm link monaco-editor-core
  ```

## Debugging / Developing Language Support

To debug bundled languages, such as JSON, HTML or TypeScript/JavaScript.

- Clone the [monaco editor repository](https://github.com/Unity-Billal-mesloub/monaco-editor): `git clone https://github.com/Unity-Billal-mesloub/monaco-editor`
- Open the repository in VS Code: `code monaco-editor`
- Run `npm install`
- Select and run the launch configuration "Monaco Editor Playground" (this might take a while, as it compiles the sources):

  ![](https://github.com/Unity-Billal-mesloub/monaco-editor/blob/main/docs/launch%20config.png)

- Now you can set breakpoints and change the source code

  ![](https://github.com/Unity-Billal-mesloub/monaco-editor/blob/main/docs/debugging-languages.gif)

- Optionally, you can build `monaco-editor` and link it if you want to test your changes in a real application:

  ```bash
  # builds out/monaco-editor
  > npm run build-monaco-editor

  > cd out/monaco-editor
  > npm link

  > cd ../path/to/my-app
  > npm link monaco-editor
  ```

## Running the editor tests

```bash
> npm run build-monaco-editor
> npm run test
> npm run compile --prefix webpack-plugin

> npm run package-for-smoketest-webpack
> npm run package-for-smoketest-esbuild
> npm run package-for-smoketest-vite
> npm run package-for-smoketest-parcel --prefix test/smoke/parcel
> npm run smoketest-debug
```

## Running the website locally

```bash
> npm install
> npm run build-monaco-editor

> cd website
> yarn install
> yarn typedoc
> yarn dev
```

Now webpack logs the path to the website.

## Out Folders

This diagram describes the output folders of the build process:

![](https://github.com/Unity-Billal-mesloub/monaco-editor/blob/main/docs/out-folders.dio.svg)

## Maintaining

Checkout [MAINTAINING.md](https://github.com/Unity-Billal-mesloub/monaco-editor/blob/main/MAINTAINING.md) for common maintaining tasks (for maintainers only).

-A local copy of the **[]()** public Documention repository by [Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub). by the developer of, and distributes, `.DockerInWSL`
