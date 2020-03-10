# maven-repo
An untrusted deserialization (CVE-2019-17570) was found in Apache XML-RPC (aka ws-xmlrpc) library.
Given Apache XML-RPC is no longer maintained, I pick the patch from https://bugzilla.redhat.com/show_bug.cgi?id=1775193,
bump up version to `3.1.3-2` and upload the private build.

## Usage
pom.xml:
```xml
<repositories>
    <repository>
        <id>fillzero-maven-repo</id>
        <url>https://raw.githubusercontent.com/fillzero/apache-xmlrpc/master/maven-repo/repository</url>
    </repository>
</repositories>
```


build.gradle:
```xml
repositories {
    maven { url "https://raw.githubusercontent.com/fillzero/apache-xmlrpc/master/maven-repo/repository" }
}


compile group: 'org.apache.xmlrpc', name: 'xmlrpc-server', version: '3.1.3-2'
Compile group: 'org.apache.xmlrpc', name: 'xmlrpc-client', version: '3.1.3-2'
```
