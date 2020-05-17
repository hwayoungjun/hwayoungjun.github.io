---
layout: post
title: Spring Boot 프로젝트 Tomcat 배포
subtitle: Tranditional Deploy
gh-repo: hwayoungjun/hwayoungjun.github.io
gh-badge: [star, fork, follow]
tags: [Spring Boot]
comments: true
categories : [spring]
pagination: 
  enabled: true
---

{% highlight java linenos %}
@SpringBootApplication
public class Application extends SpringBootServletInitializer {

    @Override
    protected SpringApplicationBuilder configure(SpringApplicationBuilder application) {
        return application.sources(Application.class);
    }

    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }

}
{% endhighlight %}

{% highlight java linenos %}
<packaging>war</packaging>
{% endhighlight %}

{% highlight java linenos %}
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-tomcat</artifactId>
    <scope>provided</scope>
</dependency>
{% endhighlight %}
