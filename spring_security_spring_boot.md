---
title: "Spring Boot Security using GitHub Copilot"
description: "Security in Spring Boot with GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---
 
## Spring Boot Security using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)
 
### Description
It is the crucial step in the spring boot tutorial for beginners step by step.
Moreover, the basic benefit of Spring Security, like with all other Spring projects, lies in how quickly and readily it can be customized. Therefore, it easily fits particular needs. The following ideas are crucial for Spring Security.
- Authorization
- Authentication
- OAuth2
- Form Authentications
- JWT(JSON Web Token)

Copilot can help you understand security in Spring Boot in a few ways.
1. It can help you identify potential security vulnerabilities in your code.
2. Copilot can help you understand the security implications of different Spring Boot features. 
3. Copilot can help you write more secure code. Copilot can suggest secure coding practices, such as using strong passwords and validating user input.

Overall, Copilot can be a valuable tool for understanding and improving security in Spring Boot However, it is important to remember that Copilot is not a replacement for a human security expert.

Also, GitHub Copilot provides accurate suggestions when you write comments with clear instructions.
We can give instruction to create SecurityConfig in Spring Boot, it will create all example we needed.

### Example

## Input Code
```java

@EnableWebSecurity
public class SecurityConfig extends WebSecurityConfigurerAdapter {
    @Override
    protected void configure(HttpSecurity http) throws Exception {
        // perform authorization based on the request 
            
}
}
```

## Result Suggested by Copilot

```java
@EnableWebSecurity
public class SecurityConfig extends WebSecurityConfigurerAdapter {
    @Override
    protected void configure(HttpSecurity http) throws Exception {
        // perform authorization based on the request

        http.authorizeRequests()
                // allow all requests to the root path
                .antMatchers("/").permitAll()
                // allow all requests to the /login path
                .antMatchers("/login").permitAll()
                // allow all requests to the /register path
                .antMatchers("/register").permitAll()
                // allow all requests to the /user path
                .antMatchers("/user").permitAll()
                // allow all requests to the /admin path
                .antMatchers("/admin").permitAll()
                // all other requests must be authenticated
                .anyRequest().authenticated()
                // configure login
                .and().formLogin()
                // specify the login page
                .loginPage("/login")
                // specify the login success page
                .defaultSuccessUrl("/user")
                // configure logout
                .and().logout()
                // specify the logout page
                .logoutUrl("/logout")
                // specify the logout success page
                .logoutSuccessUrl("/login")
                // invalidate the session
                .invalidateHttpSession(true)
                // delete the session cookie
                .deleteCookies("JSESSIONID")
                // configure exception handling
                .and().exceptionHandling()
                // specify the access denied page
                .accessDeniedPage("/access-denied");
            
}
}
```
