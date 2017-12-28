# window-api-models
Protobuf models for APIs

## Developing

### Publish

#### Java 9 issues
Gradle doesn't work with Java 9 properly:

```
$ gradle publish --stacktrace
...
Caused by: org.gradle.api.GradleException: Cannot publish to S3 since the module 'java.xml.bind' is not available. Please add "-addmods java.xml.bind '-Dorg.gradle.jvmargs=-addmods java.xml.bind'" to your GRADLE_OPTS.
```

So set `JAVA_HOME` to 1.8 first (for now):
`set -x JAVA_HOME /Library/Java/JavaVirtualMachines/jdk1.8.0_152.jdk/Contents/Home`