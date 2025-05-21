+++
date = '2025-02-09T12:53:24+03:00'
title = 'Basics of the SASS preprocessor'
categories = [ "css" ]
+++

SCSS/SASS are CSS preprocessors that extend the capabilities of standard styles. They allow you to use variables, nested selectors, mixins, functions, and other convenient tools, making the code more structured and easier to maintain. SCSS is a syntax similar to CSS, while SASS is a more concise, indented version. Both versions are compiled into regular CSS that browsers understand. These technologies significantly speed up development and simplify work with large projects.

I'll choose SASS for myself, I liked its syntax better.

### Installing the SCSS/SASS preprocessor

I didn't really like the option of installing a third-party application
to work with preprocessors, I'll go the old-fashioned way and do everything
through the console, especially since I'm on Linux;)

On windows, everything is installed via choco, on OS X via brew,
and on Linux via npm packages.

```js
npm install -g sass
```

You need to remember to write `sudo`, if you have Linux, you
know this perfectly well without me.

After installation, we'll check how everything went with the `sass --version` command
if everything is in order, it will give the version for example `1.85.0`.

After installing Sass, you can easily convert your code to CSS using the `sass` command. To do this, it is enough to specify Sass where the source file with the extension `.scss` or `.sass` is located, and where to save the compiled CSS. 

For example, by executing the command `sass input.scss output.css` in the terminal, you instruct Sass to take the file `input.scss`, process it and create a ready-made CSS file named `output.css'. This allows you to quickly generate styles that browsers can correctly interpret.

```json
sass input.scss output.css
```

We can track changes in specific files or folders using the '--watch` flag. This flag tells Sass to automatically recompile CSS each time changes occur in the monitored files. For example, to monitor changes in the input.scss file and automatically update output.css, just run the command:

```bash
sass --watch input.scss output.css
```

This eliminates the need to manually recompile the code after each change, which significantly speeds up the development process.

We can also track changes in entire folders by specifying the paths to the source directory and the folder for saving compiled CSS files. To do this, separate the paths with a colon. For example:

```bash
sass --watch app/sass:public/stylesheets
```

This command will force Sass to monitor all files in the `app/sass` folder and automatically compile them into CSS, saving the result to the `public/stylesheets` directory. This is especially useful when working with large projects where style files are divided into many components.