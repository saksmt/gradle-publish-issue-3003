## Gradle issue with publishing through uploadArchives

[Issue in gradle](https://github.com/gradle/gradle/issues/3003)

### Description

`uploadArchives` task tries to publish generated POM (maybe not only POM) twice

### Steps to reproduce

```bash
git clone https://github.com/saksmt/gradle-publish-issue-3003.git gradle-uploadArchives-issue
cd gradle-uploadArchives-issue
./gradlew build publish \
    -Preleases-repo=https://artifactory-or-nexus-repository \
    -Psnapshots-repo=https://artifactory-or-nexus-repository \
    -Partifactory.username=ARTIFACTORY_OR_NEXUS_USERNAME \
    -Partifactory.token=ARTIFACTORY_OR_NEXUS_PASSWORD_OR_TOKEN
```
