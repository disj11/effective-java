# 스프링 부트 사용
---

This section goes into more detail about how you should use Spring Boot. It covers topics such as build systems, auto-configuration, and how to run your applications. We also cover some Spring Boot best practices.  
이번 장에서는 스프링 부트를 어떻게 사용하는지에 대해 자세히 설명합니다. 빌드 시스템과 자동 구성, 어플리케이션 실행 방법과 같은 주제를 다룹니다. 또한 스프링 부트의 모범 사례를 알아봅니다. 

Although there is nothing particularly special about Spring Boot (it is just another library that you can consume), there are a few recommendations that, when followed, make your development process a little easier.  
스프링 부트에 특별할 것은 없지만 (사용할 수 있는 라이브러리의 하나일 뿐) 개발 진행을 쉽게 하기 위한 몇가지 추천 사항이 있습니다.

If you are starting out with Spring Boot, you should probably read the [Getting Started](https://docs.spring.io/spring-boot/docs/current/reference/html/getting-started.html#getting-started) guide before diving into this section.  
만약 스프링 부트를 사용하려고 한다면, 이 섹션을 읽기 전에 [Getting Started](https://docs.spring.io/spring-boot/docs/current/reference/html/getting-started.html#getting-started)를 확인해보세요.

## 1. 빌드 시스템
It is strongly recommended that you choose a build system that supports [dependency management](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-dependency-management) and that can consume artifacts published to the “Maven Central” repository.  
[의존성 관리](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-dependency-management)를 지원하고, "Maven Central"을 통한 artifacts 사용이 가능한 빌드 시스템을 사용할 것을 추천합니다.

We would recommend that you choose Maven or Gradle. It is possible to get Spring Boot to work with other build systems (Ant, for example), but they are not particularly well supported.
우리는 Maven 이나 Gradle을 사용할 것을 추천합니다. 스프링 부트를 다른 빌드 시스템(예를 들면, Ant)과 함께 사용 가능하지만, 그것을 특별히 추천하지는 않습니다.

## 1.1. 의존성 관리
Each release of Spring Boot provides a curated list of dependencies that it supports. In practice, you do not need to provide a version for any of these dependencies in your build configuration, as Spring Boot manages that for you. When you upgrade Spring Boot itself, these dependencies are upgraded as well in a consistent way.  

스프링 부트 각각의 릴리즈는 지원되는 의존성 목록이 선별되어 있습니다. 실제로, 이는 스프링 부트가 관리하기 때문에 당신은 빌드 설정에 의존성의 버전을 제공할 필요가 없습니다.
스프링 부트를 업그레이드 하면, 이러한 의존성들은 일관된 방식으로 업그레이드됩니다.

> You can still specify a version and override Spring Boot’s recommendations if you need to do so.

> 필요한 경우 당신은 스프링 부트의 권장 버전을 무시하고, 이를 직접 명시할 수 있습니다.

The curated list contains all the spring modules that you can use with Spring Boot as well as a refined list of third party libraries. The list is available as a standard [Bills of Materials (`spring-boot-dependencies`)](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-maven-without-a-parent) that can be used with both Maven and Gradle.
선별된 목록에는 스프링 부트에서 사용할 수 있는 모든 스프링 모듈 뿐만 아니라 서드 파티 라이브러리까지 포함되어 있습니다. 이 목록은 Maven 및 Gradle과 함께 사용될 수 있는 표준 [Bills of Materials (`spring-boot-dependencies`)](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-maven-without-a-parent)으로 제공됩니다.

> Each release of Spring Boot is associated with a base version of the Spring Framework. We **highly** recommend that you not specify its version.

> 스프링 부트 각각의 릴리즈는 스프링 프레임워크의 기본 버전과 연관됩니다. 직접 버전을 명시하지 않는 것을 추천합니다.