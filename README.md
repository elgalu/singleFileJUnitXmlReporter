## singleFileJUnitXmlReporter

Write a single XML file for JUnitXmlReporter

### Usage

```
require('./jasmine.single_file_junit_reporter.js');
var junitPath = path.join('junitXMLReport/', '0001');
jasmine.getEnv().addReporter(new jasmine.singleFileJUnitXmlReporter(
    junitPath, true, true)
);
```

#### You can add an xslt transformation

I use this to convert the xml to html.

You will need to install a few things:

```
npm install execSync
sudo apt-get install xsltproc
```

Then add the **xslt** argument:

```
jasmine.getEnv().addReporter(new jasmine.singleFileJUnitXmlReporter(
    junitPath, true, true, './nosetests.xslt')
);
```
