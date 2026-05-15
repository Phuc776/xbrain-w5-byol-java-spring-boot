# NOTES

## Strategy Chosen

Strategy A — Native AWS Lambda Handler using `aws-serverless-java-container-springboot3`.

---

## Goal

The original application was a standard Spring Boot HTTP server.

The goal was to make it run on AWS Lambda with minimal architecture changes while still using a native Lambda handler approach.

---

## Approach

Instead of running Spring Boot as a standalone HTTP server on port 8080, the application was adapted to run behind an AWS Lambda handler.

The following library was used:

```xml
<dependency>
    <groupId>com.amazonaws.serverless</groupId>
    <artifactId>aws-serverless-java-container-springboot3</artifactId>
    <version>2.1.2</version>
</dependency>