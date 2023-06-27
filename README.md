# Parent

Parent for all of Viskans Java projects.

**NOTE:** This project has been ardhived and is no longer used.


## Usage
```xml
<parent>
    <groupId>com.viskan</groupId>
    <artifactId>parent</artifactId>
    <version>6</version>
</parent>
```


## Examples

### Checkstyle

A failing checkstyle build is automatically bound to the lifecycle (`verify` phase). By running `mvn verify -DskipTests`, a checkstyle check will be performed and the build will fail if any violations are found.

When processing projects by CI, you would want to run the checks without failing the build, so you can process the reports before actually triggering a failure. This can be done using `mvn checkstyle:checkstyle@checkstyle-main-report checkstyle:checkstyle@checkstyle-test-report`. Reports are then found here:
 * `${project.build.directory}/checkstyle-result-main.xml`
 * `${project.build.directory}/checkstyle-result-test.xml`


## License
Apache License 2.0 © [Viskan System AB](http://viskan.com/)
