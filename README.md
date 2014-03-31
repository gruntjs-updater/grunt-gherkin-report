# grunt-gherkin-report

> It saves your gherking features in a html format

Node version: **0.8.0** required

Build status: [![Build Status](https://secure.travis-ci.org/opentable/logstash-redis.png?branch=master)](http://travis-ci.org/opentable/grunt-gherkin-report)

[![NPM](https://nodei.co/npm/grunt-gherkin-report.png?downloads=true)](https://npmjs.org/package/grunt-gherkin-report)

## Getting Started
This plugin requires Grunt `~0.4.2`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-gherkin-report --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-gherkin-report');
```

## The "gherkin_report" task

### Overview
In your project's Gruntfile, add a section named `gherkin_report` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  gherkin_report: {
    my_project: {
      // Target-specific file lists and/or options go here.
      options: {
        title: 'My project\'s features',
        subtitle: 'Generated on ' + (new Date()).toISOString() + ', version: ' + grunt.option('versionNumber') || 'unknown',
        destination: 'path-to-output/report.html'
      },
      files: [{
        cwd: 'path/to/my/features',
        src: ['**/*.feature']
      }]
    },
  },
});
```

### Options

#### options.title
Type: `String`

The title of your report.

#### options.subtitle
Type: `String`

A string that is saved during the generation and placed on the top of the generated document. Cool to place a date and a version here. Look at the example.

#### options.destination
Type: `String`

The destination of your html report and its filename.

#### files
Type: `Object`

The features to import.
