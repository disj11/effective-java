# 시작하기
---

If you are getting started with Spring Boot, or “Spring” in general, start by reading this section.  
스프링 부트나 "스프링"을 시작한다면 먼저 이 섹션을 읽어주세요.

It answers the basic “what?”, “how?” and “why?” questions.  
이 섹션은 "무엇?", "어떻게?" 그리고 "왜?" 라는 질문에 대한 답을 줄 것입니다.

It includes an introduction to Spring Boot, along with installation instructions. We then walk you through building your first Spring Boot application, discussing some core principles as we go.  
스프링 부트의 소개와 함께 설치 지침을 제공합니다. 그 후, 스프링 부트를 사용한 첫번째 어플리케이션을 만들고, 몇 가지의 핵심 원칙에 대하여 논의할 것입니다.

## 1. 스프링 부트 소개
Spring Boot makes it easy to create stand-alone, production-grade Spring-based Applications that you can run.  
스프링 부트를 사용하면 단독 실행 가능한 프로덕션급의 스프링 어플리케이션을 쉽게 만들 수 있습니다.

We take an opinionated view of the Spring platform and third-party libraries, so that you can get started with minimum fuss.  
우리는 스프링 플랫폼과 서드 파티 라이브러리의 다양한 정보를 갖고 있습니다. 때문에 최소한의 노력으로 시작할 수 있습니다.

Most Spring Boot applications need very little Spring configuration.  
대부분의 스프링 부트 어플리케이션은 아주 조금의 설정만을 필요로 합니다.


You can use Spring Boot to create Java applications that can be started by using `java -jar` or more traditional war deployments.  
당신은 `java -jar` 또는 좀 더 전통적인 방식의 war 배치를 통해 실행되는 자바 어플리케이션을 만들기 위해 스프링 부트를 사용할 수 있습니다.

We also provide a command line tool that runs “spring scripts”.  
또한 우리는 "스프링 스크립트"를 실행하는 커맨드 라인 툴을 제공합니다.

Our primary goals are:  
우리의 주요 목표는 다음과 같습니다

- Provide a radically faster and widely accessible getting-started experience for all Spring development.  
스프링 개발을 위한 빠르고 폭넓은 시작 경험을 제공합니다.

- Be opinionated out of the box but get out of the way quickly as requirements start to diverge from the defaults.  
기본적인 틀을 제공하지만, 요구사항이 기본적인 틀을 벗어났을 때 빠르게 수정할 수 있습니다.

- Provide a range of non-functional features that are common to large classes of projects (such as embedded servers, security, metrics, health checks, and externalized configuration).  
대규모 프로젝트의 공통적인 비기능적 기능을 제공합니다 (이러한 기능에는 내장 서버, security, metrics, health checks 와 외부 설정 등이 있습니다. )

- Absolutely no code generation and no requirement for XML configuration.  
당연히 코드 생성과 XML 설정을 요구하지 않습니다.

## 2. 시스템 요구사항
Spring Boot 2.2.0.RELEASE requires [Java 8](https://www.java.com) and is compatible up to Java 13 (included).  
Spring Boot 2.2.0.RELEASE은 java 8 이상부터 java 13 이하까지 호환 가능합니다.

[Spring Framework 5.2.0.RELEASE](https://docs.spring.io/spring/docs/5.2.0.RELEASE/spring-framework-reference/) or above is also required.  
Spring Framework 5.2.0.RELEASE 또는 상위의 버전도 필요합니다.

Explicit build support is provided for the following build tools:  
다음 빌드 도구에 대한 명시적 지원이 제공됩니다.

| Build | Version |
|:--|:--|
|Maven|3.3+|
|Gradle|5.x (4.10 is also supported but in a deprecated form)|

## 2.1. 서블릿 컨테이너
Spring Boot supports the following embedded servlet containers:  
스트링 부트는 다음의 내장 서블릿 컨테이너를 지원합니다.

| Name | Servlet Version |
|:--|:--|
|Tomcat 9.0|4.0|
|Jetty 9.4|3.1|
|Undertow 2.0|4.0|

You can also deploy Spring Boot applications to any Servlet 3.1+ compatible container.  
또한 스프링 부트 어플리케이션은 서블릿 3.1 이상과 호환되는 모든 컨테이너에 배포할 수 있습니다.

---

## 3. 스프링 부트 설치
Spring Boot can be used with “classic” Java development tools or installed as a command line tool.  
스트링 부트는 "classic" 자바 개발 도구와 함께 사용되거나, 커맨드 라인 도구로 설치할 수 있습니다.

Either way, you need [Java SDK v1.8](https://www.java.com) or higher. Before you begin, you should check your current 
Java installation by using the following command:  
어느쪽이든 자바 1.8 버전 또는 그 이상의 버전이 필요합니다. 시작에 앞서, 아래의 명령어를 통해 현재 설치된 자바의 버전을 확인해야합니다.

`java -version`

If you are new to Java development or if you want to experiment with Spring Boot, you might want to try the Spring Boot CLI (Command Line Interface) first.  
만약 당신이 자바 개발을 처음 시작하거나 스프링 부트를 경험하고 싶다면 먼저 [Spring Boot CLI](#3.2.-Spring-Boot-CLI-설치)를 사용해보세요.

Otherwise, read on for “classic” installation instructions.  
그렇지 않으면 "classic" 설치 지침을 읽으세요.

## 3.1. 자바 개발자를 위한 설치 지침
You can use Spring Boot in the same way as any standard Java library.  
스프링 부트는 다른 표준 자바 라이브러리와 동일한 방식으로 사용할 수 있습니다.

To do so, include the appropriate `spring-boot-*.jar` files on your classpath.  
그렇게 하려면, 적절한 `spring-boot-*.jar` 파일을 classpath에 포함해야합니다.

Spring Boot does not require any special tools integration, so you can use any IDE or text editor.  
스프링 부트는 특별한 통합 도구를 필요로 하지 않습니다. 따라서 어떠한 IDE나 텍스트 에디터라도 사용할 수 있습니다.

Also, there is nothing special about a Spring Boot application, so you can run and debug a Spring Boot application as you would any other Java program.  
또한 스트링 부트 어플리케이션은 어떠한 특별한 것도 필요로 하지 않습니다. 따라서 다른 자바 프로그램과 마찬가지로 스트링 부트 어플리케이션을 실행할 수 있고 디버그 할 수 있습니다.

Although you could copy Spring Boot jars, we generally recommend that you use a build tool that supports dependency management (such as Maven or Gradle).  
당신은 Spring Boot jars을 복사할 수 있지만, 의존성 관리를 지원하는 빌드 툴을 사용하는 것을 추천합니다. (maven 또는 gradle과 같은 도구)

## 3.1.1. Maven 설치
Spring Boot is compatible with Apache Maven 3.3 or above. If you do not already have Maven installed, you can follow the instructions at [maven.apache.org.](https://maven.apache.org/)  
스프링 부트는 Maven 3.3 혹은 그 이상의 버전과 호환됩니다. 아직 Maven이 설치되지 않았다면 [maven.apache.org.](https://maven.apache.org/)의 치침을 따르세요.

> On many operating systems, Maven can be installed with a package manager. If you use OSX Homebrew, try `brew install maven`. Ubuntu users can run `sudo apt-get install maven`. Windows users with [Chocolatey](https://chocolatey.org/) can run `choco install maven` from an elevated (administrator) prompt.

> Maven은 패키지 매니저를 통해 많은 OS에 설치될 수 있습니다.
OSX Homebrew를 사용한다면 `brew install maven`를 사용해보세요.
우분투 사용자라면 `sudo apt-get install maven`을 사용할 수 있습니다.
[Chocolatey](https://chocolatey.org/)를 사용하는 윈도우 사용자라면
관리자 권한 프롬프트를 통해 `choco install maven`를 사용할 수 있습니다.

Spring Boot dependencies use the `org.springframework.boot` `groupId`.  
스프링 부트 의존성은 `org.springframework.boot` `groupId`를 사용합니다.

Typically, your Maven POM file inherits from the `spring-boot-starter-parent` project and declares dependencies to one or more [“Starters”](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-starter).  
일반적으로 Maven POM 파일은 `spring-boot-starter-parent` 를 상속한고, 하나 이상의 “Starters”를 의존 관계로 선언합니다.

Spring Boot also provides an optional [Maven plugin](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins.html#build-tool-plugins-maven-plugin) to create executable jars.  
또한 스프링 부트는 실행 가능한 jar를 만들기 위한 [Maven plugin](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins.html#build-tool-plugins-maven-plugin)을 제공합니다.

The following listing shows a typical `pom.xml` file:   
다음의 리스트는 일반적인 `pom.xml` 파일을 보여줍니다.

```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>myproject</artifactId>
    <version>0.0.1-SNAPSHOT</version>

    <!-- Inherit defaults from Spring Boot -->
    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>2.2.0.RELEASE</version>
    </parent>

    <!-- Add typical dependencies for a web application -->
    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
    </dependencies>

    <!-- Package as an executable jar -->
    <build>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
            </plugin>
        </plugins>
    </build>

</project>
```

> The `spring-boot-starter-parent` is a great way to use Spring Boot, but it might not be suitable all of the time. Sometimes you may need to inherit from a different parent POM, or you might not like our default settings. In those cases, see [using-spring-boot.html](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-maven-without-a-parent) for an alternative solution that uses an `import` scope.

> `spring-boot-starter-parent`는 스프링 부트를 사용하기 위한 좋은 방법이지만, 이것이 모든 상황에 적합하지는 않습니다. 가끔씩 당신은 다른 부모 POM 파일을 상속해야 할 수도 있고, 기본 설정을 따르고 싶지 않을수도 있습니다. 이러한 경우 [using-spring-boot.html](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-maven-without-a-parent) 에서 `import` 스코프를 사용하는 대안법을 읽으세요.

## 3.1.2. Gradle 설치
Spring Boot is compatible with 5.x. 4.10 is also supported but this support is deprecated and will be removed in a future release.  
스프링 부트는 Gradle 5.x 버전과 호환 가능합니다. 4.10 버전 또한 지원하지만 권장하지 않고 향후 릴리즈에서 제거될 것 입니다.

If you do not already have Gradle installed, you can follow the instructions at [gradle.org](https://gradle.org/).
만약 Gradle이 설치되어 있지 않다면 [gradle.org](https://gradle.org/)의 지침을 따라주세요.

Spring Boot dependencies can be declared by using the `org.springframework.boot` `group`.  
스프링 부트 의존성은 `org.springframework.boot` `group`을 사용하여 선언할 수 있습니다.

Typically, your project declares dependencies to one or more [“Starters”](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-starter).  
일반적으로, 프로젝트는 하나 이상의 [“Starters”](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-starter) 의존성이 선언됩니다.

Spring Boot provides a useful [Gradle plugin](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins.html#build-tool-plugins-gradle-plugin) that can be used to simplify dependency declarations and to create executable jars.  
스프링 부트는 의존성 선언을 단순화하고 실행가능한 jar 파일을 만들기 위한 유용한 [Gradle plugin](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins.html#build-tool-plugins-gradle-plugin)을 제공합니다.

> **Gradle Wrapper**  
The Gradle Wrapper provides a nice way of “obtaining” Gradle when you need to build a project. It is a small script and library that you commit alongside your code to bootstrap the build process. See [docs.gradle.org/current/userguide/gradle_wrapper.html](https://docs.gradle.org/current/userguide/gradle_wrapper.html) for details.

> **Gradle Wrapper**  
Gradle Wrapper는 프로젝트를 빌드해야할 때 Gradle을 “얻는” 좋은 방법을 제공합니다.
자세한 내용은 [docs.gradle.org/current/userguide/gradle_wrapper.html](https://docs.gradle.org/current/userguide/gradle_wrapper.html)를 참조하세요.

More details on getting started with Spring Boot and Gradle can be found in the [Getting Started section](https://docs.spring.io/spring-boot/docs/2.2.0.RELEASE/gradle-plugin/reference/html//#getting-started) of the Gradle plugin’s reference guide.  
스프링 부트와 Gradle 시작에 대한 자세한 정보는 Gradle 플러그인 레퍼런스 가이드의 [Getting Started section](https://docs.spring.io/spring-boot/docs/2.2.0.RELEASE/gradle-plugin/reference/html//#getting-started)에서 확인할 수 있습니다.

## 3.2 Spring Boot CLI 설치
The Spring Boot CLI (Command Line Interface) is a command line tool that you can use to quickly prototype with Spring.  
Spring Boot CLI는 스프링 프로토타입을 빠르게 만들 수 있는 커맨드 라인 도구입니다.

It lets you run [Groovy](http://groovy-lang.org/) scripts, which means that you have a familiar Java-like syntax without so much boilerplate code.
이 도구는 많은 상용구 코드없이, java와 비슷한 문법을 갖고 있는 [Groovy](http://groovy-lang.org/) scripts를 실행할 수 있습니다.

You do not need to use the CLI to work with Spring Boot, but it is definitely the quickest way to get a Spring application off the ground.  
스프링 부트를 위해 반드시 CLI를 사용해야하는 것은 아니지만, 스프링 어플리케이션을 시작하는 가장 빠른 방법입니다.

## 3.2.1 수동 설치
You can download the Spring CLI distribution from the Spring software repository:  
Spring software repository에서 Spring CLI 배포판을 다운받을 수 있습니다.

* [spring-boot-cli-2.2.0.RELEASE-bin.zip](https://repo.spring.io/release/org/springframework/boot/spring-boot-cli/2.2.0.RELEASE/spring-boot-cli-2.2.0.RELEASE-bin.zip)
* [spring-boot-cli-2.2.0.RELEASE-bin.tar.gz](https://repo.spring.io/release/org/springframework/boot/spring-boot-cli/2.2.0.RELEASE/spring-boot-cli-2.2.0.RELEASE-bin.tar.gz)

Cutting edge [snapshot distributions](https://repo.spring.io/snapshot/org/springframework/boot/spring-boot-cli/) are also available.  
최신 스냅샷 배포판도 사용 가능합니다.

Once downloaded, follow the [INSTALL.txt](https://raw.githubusercontent.com/spring-projects/spring-boot/v2.2.0.RELEASE/spring-boot-project/spring-boot-cli/src/main/content/INSTALL.txt) instructions from the unpacked archive.  
다운로드 받은 후, 압축을 해제하고 [INSTALL.txt](https://raw.githubusercontent.com/spring-projects/spring-boot/v2.2.0.RELEASE/spring-boot-project/spring-boot-cli/src/main/content/INSTALL.txt) 지침을 따르세요.

In summary, there is a `spring` script (`spring.bat` for Windows) in a `bin/` directory in the `.zip` file.  
요약하자면, `.zip` 파일의 `bin/` 폴더 안에 있는 `spring` 스크립트 (윈도우용 `spring.bat`)가 있습니다.

Alternatively, you can use `java -jar` with the `.jar` file (the script helps you to be sure that the classpath is set correctly).  
다른 방법으로는 `java -jar` 을 사용하여 `.jar` 파일을 실행할 수 있습니다. (이 스크립트는 당신이 올바른 classpath를 설정했는지 확인하는데 도움을 줍니다.)

## 3.2.2 SDKMAN! 으로 설치
SDKMAN! (The Software Development Kit Manager) can be used for managing multiple versions of various binary SDKs, including Groovy and the Spring Boot CLI.  
SDKMAN은 Groovy와 Spring Boot CLI를 포함한 여러 버전의 SDK를 관리하는데 사용할 수 있습니다.

Get SDKMAN! from [sdkman.io](https://sdkman.io/) and install Spring Boot by using the following commands:  
[sdkman.io](https://sdkman.io/)에서 SDKMAN을 다운로드 받고, 다음의 명령어를 통해 스트링 부트를 설치하세요.

```
$ sdk install springboot
$ spring --version
Spring Boot v2.2.0.RELEASE
```

If you develop features for the CLI and want easy access to the version you built, use the following commands:  
당신이 CLI를 위한 기능을 개발하고, 빌드한 버전에 쉽게 접근하고 싶다면 다음의 명령어를 사용하세요.

```
$ sdk install springboot dev /path/to/spring-boot/spring-boot-cli/target/spring-boot-cli-2.2.0.RELEASE-bin/spring-2.2.0.RELEASE/
$ sdk default springboot dev
$ spring --version
Spring CLI v2.2.0.RELEASE
```

The preceding instructions install a local instance of `spring` called the `dev` instance.  
위의 지침은 `dev` 인스턴스라고 하는 로컬 `spring` 인스턴스를 설치합니다.

It points at your target build location, so every time you rebuild Spring Boot, spring is up-to-date.
그것은 당신의 타겟 빌드 위치를 가리키기 때문에, 스프링 부트를 다시 빌드할 때마다 항상 최신 상태를 유지합니다.

You can see it by running the following command:  
다음의 명령어를 통해 확인할 수 있습니다.

```
$ sdk ls springboot

================================================================================
Available Springboot Versions
================================================================================
> + dev
* 2.2.0.RELEASE

================================================================================
+ - local version
* - installed
> - currently in use
================================================================================
```

## 3.2.3. OSX Homebrew 설치
If you are on a Mac and use [Homebrew](https://brew.sh/), you can install the Spring Boot CLI by using the following commands:  
당신이 Mac과 [Homebrew](https://brew.sh/)를 사용하고 있다면, 아래의 다음의 명령어를 통해 Spring Boot CLI를 설치할 수 있습니다.

```
$ brew tap pivotal/tap
$ brew install springboot
```

Homebrew installs `spring` to /usr/local/bin.  
Homebrew는 `spring`을 /usr/local/bin 경로에 설치합니다.

> If you do not see the formula, your installation of brew might be out-of-date. In that case, run `brew update` and try again.

> 만약, 설치가 진행되지 않는다면 당신의 brew가 오래된 버전일수도 있습니다. 이러한 경우, `brew update` 명령을 실행하고 다시 시도해보세요.

## 3.2.4. MacPorts 설치
If you are on a Mac and use [MacPorts](https://www.macports.org/), you can install the Spring Boot CLI by using the following command:  
당신이 Mac과 [MacPorts](https://www.macports.org/)를 사용하고 있다면, 다음의 명령어를 통해 Spring Boot CLI를 설치할 수 있습니다.

```
$ sudo port install spring-boot-cli
```

## 3.2.5. 명령줄 완성
The Spring Boot CLI includes scripts that provide command completion for the [BASH](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) and [zsh](https://en.wikipedia.org/wiki/Z_shell) shells.  
Spring Boot CLI는 [BASH](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)와 [zsh](https://en.wikipedia.org/wiki/Z_shell) 쉘을 위한 자동 완성 기능을 제공하는 스크립트가 포함되어 있습니다.

You can `source` the script (also named `spring`) in any shell or put it in your personal or system-wide bash completion initialization.  
어떤 쉘 에서든지 그 스크립트(`spring` 으로 불린다.)를 `source` 하거나, 시스템 공통 bash 자동 완성 초기화 경로에 넣을 수 있습니다.

On a Debian system, the system-wide scripts are in `/shell-completion/bash` and all scripts in that directory are executed when a new shell starts.  
데비안 시스템에서 시스템 공통 스크립트는 `/shell-completion/bash`에 존재합니다.
그리고 그 디렉토리 안에 있는 모든 스크립트는  새로운 쉘이 시작될 때 실행됩니다.

For example, to run the script manually if you have installed by using SDKMAN!, use the following commands:  
예를들어, SDKMAN!을 사용하여 설치한 경우, 스크립트를 수동으로 실행하려면 다음의 명령을 사용하세요.

```
$ . ~/.sdkman/candidates/springboot/current/shell-completion/bash/spring
$ spring <HIT TAB HERE>
  grab  help  jar  run  test  version
```

> If you install the Spring Boot CLI by using Homebrew or MacPorts, the command-line completion scripts are automatically registered with your shell.

> 만약 Spring Boot CLI를 Homebrew 또는 MacPorts를 통해 설치했다면, 명령줄 자동완성 스크립트는 자동으로 쉘에 등록됩니다.

## 3.2.6. Windows Scoop 설치
If you are on a Windows and use [Scoop](https://scoop.sh/), you can install the Spring Boot CLI by using the following commands:  
Windows와 [Scoop](https://scoop.sh/)를 사용하고 있다면, 다음의 명령을 통해 Spring Boot CLI를 설치할 수 있습니다.

```
> scoop bucket add extras
> scoop install springboot
```

Scoop installs `spring` to `~/scoop/apps/springboot/current/bin`.  
Scoop는 `~/scoop/apps/springboot/current/bin` 경로에 `spring`을 설치합니다.

> If you do not see the app manifest, your installation of scoop might be out-of-date. In that case, run `scoop update` and try again.

> 설치가 되지 않는다면 오래된 버전의 `scoop`가 설치되어 있을수도 있습니다.
이러한 경우는 `scoop update` 명령을 실행한 후 다시 시도해보세요.

## 3.2.7. Spring CLI 빠른 시작
You can use the following web application to test your installation. To start, create a file called `app.groovy`, as follows:  
설치를 테스트하기 위한 다음의 웹 에플리케이션을 사용할 수 있습니다.
시작하시려면 다음과 같은 `app.groovy` 파일을 만들어주세요.

```
@RestController
class ThisWillActuallyRun {

    @RequestMapping("/")
    String home() {
        "Hello World!"
    }

}
```

Then run it from a shell, as follows:  
그 후 다음과 같이 쉘에서 파일을 실행해주세요.

```
$ spring run app.groovy
```

> The first run of your application is slow, as dependencies are downloaded. Subsequent runs are much quicker.  
어플리케이션을 처음 실행하면 의존성이 다운로드 될 때 느릴 수 있습니다.
이후의 실행은 훨씬 빠릅니다.

Open [localhost:8080](http://localhost:8080/) in your favorite web browser. You should see the following output:  
웹 브라우저에서 [localhost:8080](http://localhost:8080/)에 접속해보세요. 다음과 같은 화면을 볼 수 있습니다.

```
Hello World!
```

## 3.3. 이전 버전의 Spring Boot 업데이트
If you are upgrading from the `1.x` release of Spring Boot, check the [“migration guide” on the project wiki](https://github.com/spring-projects/spring-boot/wiki/Spring-Boot-2.0-Migration-Guide) that provides detailed upgrade instructions.  
`1.x` 버전의 스프링 부트 릴리즈를 업데이트 하려면 [“migration guide” on the project wiki](https://github.com/spring-projects/spring-boot/wiki/Spring-Boot-2.0-Migration-Guide)를 확인하세요. 자세한 업그레이드 지침을 제공합니다.

Check also the [“release notes”](https://github.com/spring-projects/spring-boot/wiki) for a list of “new and noteworthy” features for each release.  
각 릴리즈의 "새롭고 주목할만한" 기능들을 확인하려면 [“release notes”](https://github.com/spring-projects/spring-boot/wiki)를 확인해보세요.

When upgrading to a new feature release, some properties may have been renamed or removed.  
새로운 릴리즈로 업데이트시, 몇몇의 속성의 이름이 변경되거나 제거될 수 있습니다.

Spring Boot provides a way to analyze your application’s environment and print diagnostics at startup, but also temporarily migrate properties at runtime for you.  
스프링 부트는 시작시 어플리케이션의 환경을 분석하고 진단을 출력하는 법을 제공하지만,
런타임시 속성들을 일시적으로 마이그레이션합니다.

To enable that feature, add the following dependency to your project:  
해당 기능을 활성화하려면 프로젝트에 다음의 의존성을 추가하세요.

```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-properties-migrator</artifactId>
    <scope>runtime</scope>
</dependency>
```

> Properties that are added late to the environment, such as when using `@PropertySource`, will not be taken into account.

> `@PropertySource`와 같이 환경에 늦게 추가된 속성들은 고려되지 않습니다.

> Once you’re done with the migration, please make sure to remove this module from your project’s dependencies.

> 마이그레이션이 완료되면, 프로젝트의 종속성에서 이 모듈을 반드시 제거해주세요.

To upgrade an existing CLI installation, use the appropriate package manager command (for example, `brew upgrade`).  
현재 설치된 CLI 업데이트하려면, 적당한 패키지 관리자 명령을 사용하세요 (예: `brew upgrade`)

If you manually installed the CLI, follow the [standard instructions](https://docs.spring.io/spring-boot/docs/2.2.0.RELEASE/reference/html/getting-started.html#getting-started-manual-cli-installation), remembering to update your `PATH` environment variable to remove any older references.  
CLI를 수동으로 설치했다면 [표준 지침](https://docs.spring.io/spring-boot/docs/2.2.0.RELEASE/reference/html/getting-started.html#getting-started-manual-cli-installation)을 따르세요.
`PATH` 환경변수를 업데이트하여 이전 참조를 제거하십시오.

---

## 4. 첫번째 스프링 부트 어플리케이션 개발
This section describes how to develop a simple “Hello World!” web application that highlights some of Spring Boot’s key features. We use Maven to build this project, since most IDEs support it.  
이 섹션에서는 스프링의 주요 기능의 일부를 강조하는 "Hello Word!" 웹 어플리케이션을 만드는 방법을 설명합니다. 대부분의 IDE에서 메이븐을 지원하기 때문에, 이 프로젝트의 빌드를 위해 메이븐을 사용할 것입니다.

> The [spring.io](https://spring.io/) web site contains many “Getting Started” [guides](https://spring.io/guides) that use Spring Boot. If you need to solve a specific problem, check there first.    
You can shortcut the steps below by going to [start.spring.io](https://start.spring.io/) and choosing the "Web" starter from the dependencies searcher. Doing so generates a new project structure so that you can [start coding right away](https://docs.spring.io/spring-boot/docs/current/reference/html/getting-started.html#getting-started-first-application-code). Check the [Spring Initializr documentation](https://docs.spring.io/initializr/docs/current/reference/html//#user-guide) for more details.

> [spring.io](https://spring.io/) 사이트는 스트링 부트를 사용하는 많은 "시작하기" [guides](https://spring.io/guides)를 포함하고 있습니다. 특별한 문제에 대한 해결책이 필요하다면, 먼저 이 사이트를 확인해보세요.    
[start.spring.io](https://start.spring.io/)로 이동하고, 의존성 검색기에서 "Web" starter를 선택하여 아래의 단계를 줄일 수 있습니다. 그렇게 하면 새로운 프로젝트가 생성되고, [바로 코딩을 시작](https://docs.spring.io/spring-boot/docs/current/reference/html/getting-started.html#getting-started-first-application-code)할 수 있습니다. 자세한 내용을 보려면 [Spring Initializr documentation](https://docs.spring.io/initializr/docs/current/reference/html//#user-guide) 사이트를 확인하세요.

Before we begin, open a terminal and run the following commands to ensure that you have valid versions of Java and Maven installed:  
시작하기 전에, 터미널을 열고 자바와 메이븐이 유효한 버전인지 확인하기 위해 다음의 명령을 입력해주세요.

```
$ java -version
java version "1.8.0_102"
Java(TM) SE Runtime Environment (build 1.8.0_102-b14)
Java HotSpot(TM) 64-Bit Server VM (build 25.102-b14, mixed mode)
```

```
$ mvn -v
Apache Maven 3.5.4 (1edded0938998edf8bf061f1ceb3cfdeccf443fe; 2018-06-17T14:33:14-04:00)
Maven home: /usr/local/Cellar/maven/3.3.9/libexec
Java version: 1.8.0_102, vendor: Oracle Corporation
```

> This sample needs to be created in its own folder. Subsequent instructions assume that you have created a suitable folder and that it is your current directory.

> 이 샘플은 자체 폴더 안에 생성되어야 합니다. 후속 지침은 적합한 폴더를 생성하였으며, 그 폴더가 현재 디렉토리라고 가정합니다.

## 4.1 POM 파일 생성
We need to start by creating a Maven `pom.xml` file. The `pom.xml` is the recipe that is used to build your project. Open your favorite text editor and add the following:  
`pom.xml` 파일을 생성합니다. `pom.xml` 파일은 프로젝트를 빌드하기 위해 사용합니다. 텍스트 에디터를 열고 다음의 내용을 추가하세요.

```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>myproject</artifactId>
    <version>0.0.1-SNAPSHOT</version>

    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>2.2.0.RELEASE</version>
    </parent>

    <!-- Additional lines to be added here... -->

</project>
```

The preceding listing should give you a working build. You can test it by running `mvn package` (for now, you can ignore the “jar will be empty - no content was marked for inclusion!” warning).  
위의 코드는 작업 빌드를 제공합니다. 그것을 `mvn package`를 명령어를 실행하여 테스트할 수 있습니다. ( “jar will be empty - no content was marked for inclusion!” 라는 경고 메시지는 무시해주세요.)

> At this point, you could import the project into an IDE (most modern Java IDEs include built-in support for Maven). For simplicity, we continue to use a plain text editor for this example.

> 이제 프로젝트를 IDE에 추가할 수 있습니다. (대부분의 최신 Java IDE는 메이븐을 지원합니다.) 이 예제를 간단히 테스트하기 위해 저희는 일반 텍스트 편집기를 사용할 것입니다.

## 4.2 클래스 패스 의존성 추가
Spring Boot provides a number of “Starters” that let you add jars to your classpath.  
스프링 부트는 클래스 패스에 jar 파일을 추가하는 많은 "Starters"를 제공합니다.

Our applications for smoke tests use the `spring-boot-starter-parent` in the `parent` section of the POM.
우리의 스모크 테스트 어플리케이션은 POM 파일의 `parent` 섹션 안에 있는 `spring-boot-starter-parent`를 사용합니다.

The `spring-boot-starter-parent` is a special starter that provides useful Maven defaults.  
`spring-boot-starter-parent`는 메이븐의 유용한 기능을 제공하는 특별한 starter입니다.

It also provides a `dependency-management` section so that you can omit `version` tags for “blessed” dependencies.  
또한 그것은 "blessed" 의존성에 대한 `version` 태그를 생략할 수 있도록 `dependency-management` 섹션을 제공합니다.

Other “Starters” provide dependencies that you are likely to need when developing a specific type of application.  
다른 "Starters"는 특정 유형의 어플리케이션 개발에 필요할 수도 있는 의존성을 제공합니다.

Since we are developing a web application, we add a `spring-boot-starter-web` dependency. Before that, we can look at what we currently have by running the following command:  
우리가 웹 어플리케이션을 개발하는 중이므로 `spring-boot-starter-web` 의존성을 추가합니다. 그에 앞서 우리가 현재 갖고 있는 의존성을 다음의 명령어를 통해 확인할 수 있습니다.

```
$ mvn dependency:tree

[INFO] com.example:myproject:jar:0.0.1-SNAPSHOT
```

The `mvn dependency:tree` command prints a tree representation of your project dependencies. You can see that `spring-boot-starter-parent` provides no dependencies by itself.  
`mvn dependency:tree` 명령어는 프로젝트 의존성을 트리 형태로 출력합니다.
`spring-boot-starter-parent`는 자체적으로 의존성을 제공하지 않는다는 것을 알 수 있습니다.

To add the necessary dependencies, edit your `pom.xml` and add the `spring-boot-starter-web` dependency immediately below the `parent` section:  
필요한 의존성을 추가하려면, `pom.xml` 파일을 수정하고 `spring-boot-starter-web`을 `parent` 섹션 바로 아래 부분에 추가하세요.

```
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
</dependencies>
```

If you run `mvn dependency:tree` again, you see that there are now a number of additional dependencies, including the Tomcat web server and Spring Boot itself.  
`mvn dependency:tree` 명령을 다시한번 실행하면, 톰캣, 스프링 부트 등을 포함한 많은 추가 의존성들을 확인할 수 있습니다.

## 4.3 코드 작성
To finish our application, we need to create a single Java file.  
어플리케이션의 마무리를 위해 하나의 java 파일을 생성해야합니다.

By default, Maven compiles sources from `src/main/java`, so you need to create that folder structure and then add a file named `src/main/java/Example.java` to contain the following code:  
기본적으로 메이븐은 `src/main/java`에 있는 파일을 컴파일합니다.
따라서 당신은 이 폴더 구조를 만들어야합니다. 그 후 `src/main/java/Example.java`라는 파일을 생성하여 다음의 내용을 작성하세요.

```
import org.springframework.boot.*;
import org.springframework.boot.autoconfigure.*;
import org.springframework.web.bind.annotation.*;

@RestController
@EnableAutoConfiguration
public class Example {

    @RequestMapping("/")
    String home() {
        return "Hello World!";
    }

    public static void main(String[] args) {
        SpringApplication.run(Example.class, args);
    }

}
```

Although there is not much code here, quite a lot is going on. We step through the important parts in the next few sections.  
비록 많은 코드는 아니지만, 많은 일이 진행되고 있습니다.
다음 섹션에서는 중요한 부분을 단계별로 살펴볼 것입니다.

## 4.3.1 @RestController와 @RequestMapping 어노테이션
The first annotation on our `Example` class is `@RestController`. This is known as a *stereotype* annotation.  
첫번째 어노테이션은 `Example` 클래스의 `@RestController` 입니다. 이 어노테이션은 *stereotype* 어노테이션이라고 합니다.

It provides hints for people reading the code and for Spring that the class plays a specific role.  
이것은 코드를 읽는 사람들과 스프링에게 이 클래스가 특정 역할을 한다는 힌트를 제공합니다.

In this case, our class is a web `@Controller`, so Spring considers it when handling incoming web requests.  
이 경우, 이 클래스는 웹 `@Controller` 입니다. 그래서 스프링은 웹 요청을 처리할 때 이를 고려합니다.

The `@RequestMapping` annotation provides “routing” information. It tells Spring that any HTTP request with the `/` path should be mapped to the `home` method.  
`@RequestMapping` 어노테이션은 "라우팅" 정보를 제공합니다. 이는 `/` 경로가 있는 모든 HTTP 요청은 `home` 메소드에 매핑되도록 합니다.

The `@RestController` annotation tells Spring to render the resulting string directly back to the caller.
`@RestController` 어노테이션은 처리 결과를 호출자에게 직접 렌더링하도록 지시합니다.

> The `@RestController` and `@RequestMapping` annotations are Spring MVC annotations (they are not specific to Spring Boot). See the [MVC section](https://docs.spring.io/spring/docs/5.2.0.RELEASE/spring-framework-reference/web.html#mvc) in the Spring Reference Documentation for more details.

> `@RestController`와 `@RequestMapping` 어노테이션은 스프링 MVC의 어노테이션입니다. (스프링 부트만의 어노테이션이 아닙니다.) 좀 더 자세한 정보는 스트링 부트 문서의 [MVC section](https://docs.spring.io/spring/docs/5.2.0.RELEASE/spring-framework-reference/web.html#mvc)를 참고하세요.

## 4.3.2 @EnableAutoConfiguration 어노테이션
The second class-level annotation is `@EnableAutoConfiguration.`  
두번째로, 클래스 레벨 어노테이션인 `@EnableAutoConfiguration.` 입니다.

This annotation tells Spring Boot to “guess” how you want to configure Spring, based on the jar dependencies that you have added.  
이 어노테이션은 추가된 jar 의존성에 기초하여 스프링 부트가 어떻게 스프링 설정을 할 것인지 "추측"하도록 합니다.

Since `spring-boot-starter-web` added Tomcat and Spring MVC, the auto-configuration assumes that you are developing a web application and sets up Spring accordingly.  
`spring-boot-starter-web`에는 톰캣과 Spring MVC가 추가되어있기 때문에 auto-configuration은 이것이 웹 어플리케이션이라 추측하고, 그에 적절한 Spring 설정을 합니다.

> **Starters and Auto-configuration**  
Auto-configuration is designed to work well with “Starters”, but the two concepts are not directly tied. You are free to pick and choose jar dependencies outside of the starters. Spring Boot still does its best to auto-configure your application.

> **Starters and Auto-configuration**  
Auto-configuration은 "Starters"와 잘 작동되도록 설계되었습니다. 하지만 두 개념이 직접적으로 관계되어있지는 않습니다. 당신은 스터터 이외의 jar 의존성을 자유롭게 고르고 선택할 수 있습니다. 스프링 부트는 최선의 설정을 당신의 어플리케이션에 적용해 줄 것입니다.

## 4.3.3 "main" 메서드
The final part of our application is the `main` method. This is just a standard method that follows the Java convention for an application entry point.  
이 어플리케이션의 마지막 파트는 메인 메서드입니다. 메인 메서드는 어플리케이션의 진입점을 나타내는 자바 표준 메서드입니다.

Our main method delegates to Spring Boot’s `SpringApplication` class by calling `run`. SpringApplication bootstraps our application, starting Spring, which, in turn, starts the auto-configured Tomcat web server.  
메인 메서드는 `SpringApplication`의 `run`을 실행합니다. `SpringApplication`은 스프링과 자동 설정된 톰캣 웹서버를 차례로 실행시킵니다.

We need to pass `Example.class` as an argument to the `run` method to tell `SpringApplication` which is the primary Spring component. The `args` array is also passed through to expose any command-line arguments.  
우리는 `SpringApplication`을 스프링의 기본 컴포넌트라고 알리기 위해 `Example.class`를 `run` 메서드의 매개변수로 전달해야합니다.

## 4.4 예제 실행
At this point, your application should work. Since you used the `spring-boot-starter-parent` POM, you have a useful `run` goal that you can use to start the application.  
이 지점에서, 어플리케이션은 실행 가능해야합니다. `spring-boot-starter-parent` POM을 사용했기 때문에 어플리케이션을 시작하는데 사할 수 있는 유용한 `run` 목표가 있습니다.

Type `mvn spring-boot:run` from the root project directory to start the application. You should see output similar to the following:  
어플리케이션을 시작하기 위해 루트 프로젝트 디렉토리에서 `mvn spring-boot:run`을 입력해보세요. 다음과 비슷한 화면이 출력될 것입니다.

```
$ mvn spring-boot:run

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::  (v2.2.1.RELEASE)
....... . . .
....... . . . (log output here)
....... . . .
........ Started Example in 2.222 seconds (JVM running for 6.514)
```

If you open a web browser to [localhost:8080](http://localhost:8080/), you should see the following output:  
웹 브라우저를 통해 [localhost:8080](http://localhost:8080/)에 접속하면, 다음의 내용이 출력됩니다.

```
Hello World!
```

To gracefully exit the application, press ctrl-c.  
ctrl-c 키를 누르면, 어플리케이션을 정상적으로 종료합니다.

## 4.5 실행 가능한 jar 생성
We finish our example by creating a completely self-contained executable jar file that we could run in production.  
우리는 프로덕션 환경에서 실행할 수 있는 완전 독립적인 실행가능한 jar 파일을 만들고 예제를 끝마칠 것입니다.

Executable jars (sometimes called “fat jars”) are archives containing your compiled classes along with all of the jar dependencies that your code needs to run.  
실행 가능한 jars ("fat jars" 라고 불리기도 합니다)는 실행하기위해 필요한 모든 jar 의존성과 컴파일된 클래스를 포함하고 있는 아카이브입니다.

> **Executable jars and Java**  
Java does not provide a standard way to load nested jar files (jar files that are themselves contained within a jar). This can be problematic if you are looking to distribute a self-contained application.  

> To solve this problem, many developers use “uber” jars. An uber jar packages all the classes from all the application’s dependencies into a single archive.  

> The problem with this approach is that it becomes hard to see which libraries are in your application. It can also be problematic if the same filename is used (but with different content) in multiple jars.  

> Spring Boot takes a [different approach](https://docs.spring.io/spring-boot/docs/current/reference/html/appendix-executable-jar-format.html#executable-jar) and lets you actually nest jars directly.

> **Executable jars and Java**  
자바는 중첩된 jar(jar 파일 내부에 jar가 포함되어있는) 파일을 로드하기 위한 표준 방법을 제공하지 않습니다. 이것은 독립형 어플리케이션을 배포할때 문제가 발생할 수 있습니다.  

> 이 문제를 해결하기 위해 많은 개발자들은 "uber" jars를 사용합니다. uber jar은 모든 어플리케이션의 의존 클래스들을 하나의 아카이브로 패키징합니다.  

> 이 방법의 문제는 어플리케이션 안에 어떤 라이브러를 사용했는지 파악하기 어렵다는 것입니다. 또한 여러 jar 파일들 안에서 같은 파일 이름이 (다른 내용으로) 존재한다면 문제가 될 수 있습니다.  

> 스프링 부트는 [다른 접근법](https://docs.spring.io/spring-boot/docs/current/reference/html/appendix-executable-jar-format.html#executable-jar)을 사용하므로 jar 파일을 직접 중첩시킬 수 있습니다.  

> 실행 가능한 jar 파일을 만들기 위해, `pom.xml` 파일에 `spring-boot-maven-plugin`을 추가해야합니다. 추가하려면, `dependencies` 섹션 바로 아래에 다음 라인을 추가하세요.

```
<build>
    <plugins>
        <plugin>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-maven-plugin</artifactId>
        </plugin>
    </plugins>
</build>
```

> The `spring-boot-starter-parent` POM includes `<executions>` configuration to bind the `repackage` goal. If you do not use the parent POM, you need to declare this configuration yourself. See the [plugin documentation](https://docs.spring.io/spring-boot/docs/2.2.1.RELEASE/maven-plugin//usage.html) for details.

> `spring-boot-starter-parent` POM은 `repackage` goal 바인딩을 위해 `<executions>` 설정이 포함되어 있습니다. 만약 parent POM을 사용하지 않는다면, 이 설정을 직접 정의해야합니다. 자세한 설명은 [plugin documentation](https://docs.spring.io/spring-boot/docs/2.2.1.RELEASE/maven-plugin//usage.html)를 참고하세요.

Save your `pom.xml` and run `mvn package` from the command line, as follows:  
`pom.xml`을 저장하고, 다음과 같이 `mvn package` 명령을 실행하세요.

```
$ mvn package

[INFO] Scanning for projects...
[INFO]
[INFO] ------------------------------------------------------------------------
[INFO] Building myproject 0.0.1-SNAPSHOT
[INFO] ------------------------------------------------------------------------
[INFO] .... ..
[INFO] --- maven-jar-plugin:2.4:jar (default-jar) @ myproject ---
[INFO] Building jar: /Users/developer/example/spring-boot-example/target/myproject-0.0.1-SNAPSHOT.jar
[INFO]
[INFO] --- spring-boot-maven-plugin:2.2.1.RELEASE:repackage (default) @ myproject ---
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
```

If you look in the `target` directory, you should see `myproject-0.0.1-SNAPSHOT.jar`. The file should be around 10 MB in size. If you want to peek inside, you can use `jar tvf`, as follows:  
`target` 디렉토리 안을 보면, `myproject-0.0.1-SNAPSHOT.jar`을 확일할 수 있습니다. 이 파일은 10MB 정도입니다. 이 파일의 내용을 보고싶다면, 다음과 같이 `jar tvf` 명령어를 사용하세요.

```
$ jar tvf target/myproject-0.0.1-SNAPSHOT.jar
```

You should also see a much smaller file named `myproject-0.0.1-SNAPSHOT.jar.original` in the `target` directory. This is the original jar file that Maven created before it was repackaged by Spring Boot.  
또한 `target` 디렉토리 안에 `myproject-0.0.1-SNAPSHOT.jar.original` 라는 파일이 존재해야합니다. 이는 스프링 부트에 의해 repackaged 되기 전 Maven이 생성한 원본 jar 파일입니다.

To run that application, use the `java -jar` command, as follows:  
어플리케이션을 실행하려면, 다음과 같이 `java -jar` 명령어를 사용하세요.

```
$ java -jar target/myproject-0.0.1-SNAPSHOT.jar

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::  (v2.2.1.RELEASE)
....... . . .
....... . . . (log output here)
....... . . .
........ Started Example in 2.536 seconds (JVM running for 2.864)
```

As before, to exit the application, press `ctrl-c.`  
이전과 마찬가지로 오플리케이션을 종료하려면 ctrl-c 키를 누르세요.

---

## 5. 다음 내용
Hopefully, this section provided some of the Spring Boot basics and got you on your way to writing your own applications.  
이 섹션이 스프링 부트에 대한 기본 내용을 제공하고, 당신의 어플리케이션을 작성하는데 도움이 되었길 바랍니다.

If you are a task-oriented type of developer, you might want to jump over to [spring.io](https://spring.io/) and check out some of the [getting started](https://spring.io/guides/) guides that solve specific “How do I do that with Spring?” problems. We also have Spring Boot-specific “[How-to](https://docs.spring.io/spring-boot/docs/current/reference/html/howto.html#howto)” reference documentation.  
당신이 작업 지향 유형의 개발자라면, [spring.io](https://spring.io/)로 넘어가서 "스프링으로 어떻게 하지?" 문제에 대한 해결책을 제시하는 [getting started](https://spring.io/guides/) 가이드를 확인하세요. 또한 우리는 스프링 부트만을 위한 “[How-to](https://docs.spring.io/spring-boot/docs/current/reference/html/howto.html#howto)” 레퍼런스 문서도 제공합니다.

Otherwise, the next logical step is to read [using-spring-boot.html](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot). If you are really impatient, you could also jump ahead and read about [Spring Boot features](https://docs.spring.io/spring-boot/docs/current/reference/html/spring-boot-features.html#boot-features).  
그렇지 않을 경우, 다음 단계는 [using-spring-boot.html](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot)를 읽는 것입니다. 당신이 정말 급하다면, 이를 건너뛰고 [Spring Boot features](https://docs.spring.io/spring-boot/docs/current/reference/html/spring-boot-features.html#boot-features)를 읽으세요.