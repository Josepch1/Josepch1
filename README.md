<h1 align="center">José Pedro C. Homenhuck</h1>

<p align="center">
  👋 <b>Backend developer</b> · PHP, Laravel and PostgreSQL · Porto Alegre, Brazil
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/josepch/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:josepedro.homenhuck@gmail.com">
    <img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>

## About

Hey, I'm José Pedro. I'm a backend dev at GEO Digital, and I take freelance backend work on the side.

Most of what I write is PHP. Laravel when the project fits it, plain PHP when a framework would only get in the way. Somewhere in there I usually break something and spend the evening finding out why.

## How I work

Static analysis and tests are part of writing the code for me, not a step that comes after it.

**Architecture.** Domain-Driven Design in a modular monolith: one module per bounded context, each split into Domain, Application, Infrastructure and HTTP. The domain layer holds the entities, value objects, domain events and repository interfaces, and knows nothing about Eloquent or HTTP.

The dependency rule from Clean Architecture points inward, and Deptrac enforces it in CI. A shortcut import fails the build instead of surviving review. Where a layer genuinely has to be crossed, the exception is declared in the config with the reason written above it, so it stays a decision rather than a suppressed warning.

**Testing.** This is the part I enjoy most. When I already know what a piece of code should do, I write the failing test before I write it, and let the test drive the shape of the interface. It is easier to design something you have already had to call once.

Separate suites for unit, integration, feature, smoke and end to end, plus architecture tests that assert the shape of the code rather than its output. Test names read as behaviour, so a failure tells you what the system stopped doing.

Coverage only says which lines ran. Mutation testing says whether anything would have noticed if those lines were wrong, and it is the check that has found the most useless tests I had written.

**Static analysis.** PHPStan and Larastan at a strict level, Rector for upgrades, Pint for formatting. Secret scanning with Gitleaks on every push.

**Databases.** PostgreSQL and MySQL. Multi-tenant schemas using list partitioning with composite foreign keys. CI runs against a real Postgres, not SQLite, because the two disagree exactly where it hurts.

**Commits.** Conventional Commits, and the body explains why the change exists, what it was validated against, and which alternative I ruled out. Future me reads those more often than the code.

**Delivery.** Docker for local and production parity, GitHub Actions for CI plus a nightly run, and short-lived branches off `develop`.

## Stack

**Day to day**

![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

**Testing and quality**

![Pest](https://img.shields.io/badge/Pest-6C5CE7?style=flat-square&logo=pest&logoColor=white)
![PHPUnit](https://img.shields.io/badge/PHPUnit-366488?style=flat-square&logo=php&logoColor=white)
![PHPStan](https://img.shields.io/badge/PHPStan-4B8BBE?style=flat-square)
![Infection](https://img.shields.io/badge/Infection-8E44AD?style=flat-square)
![Deptrac](https://img.shields.io/badge/Deptrac-2C3E50?style=flat-square)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

<details>
<summary><b>Also worked with</b></summary>

<br>

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-087EA4?style=flat-square&logo=react&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)
![Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)

</details>

## Public work

Most of what I build is in private repositories, so I put together one that is not.

**[php-quality-gates](https://github.com/Josepch1/php-quality-gates)** is a small layered module wired to the checks described above. Clone it, run `composer check`, then add an import that breaks a layer boundary and watch the build refuse it. Everything else public here is older and does not say much about how I work today.

---

<p align="center">
  <sub>Want to talk backend, or just say hi? <a href="https://www.linkedin.com/in/josepch/">LinkedIn</a> is the fastest way to reach me.</sub>
</p>
