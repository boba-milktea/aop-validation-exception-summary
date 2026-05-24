# Spring Boot summary — AOP, Validation & Exception Handling

**Study reference for [Hack Your Future](https://www.hackyourfuture.net/) Backend (Java) students.**

This repo is a short recap of the Spring Boot training on **clean API design**: cross-cutting logic (AOP), input validation, and global error handling. Use it after the lessons or when revising for projects.

## What’s inside

One file: **`index.html`** — an interactive slide deck (quizzes and small exercises included). Open it in your browser; nothing to install.

```bash
open index.html
```

Use **arrow keys** or **Next / Previous** to move through the slides.

## Four topics (matches the course)

| # | Topic | You’ll use |
|---|--------|------------|
| 1 | **AOP** | `@Aspect`, `@Around`, pointcuts — logging/timing without copying code into every service method |
| 2 | **Validation** | `@Valid`, `@NotBlank`, `@Email`, `@Min` on DTOs — reject bad input at the controller |
| 3 | **@Valid vs @Validated** | `@Valid` on `@RequestBody`; `@Validated` on class + path/query params — different exceptions |
| 4 | **Global exceptions** | `@RestControllerAdvice` + `@ExceptionHandler` — same JSON error shape for every endpoint |

**Remember:** `@Valid` → `MethodArgumentNotValidException`. `@Validated` on parameters → `ConstraintViolationException`. Handle both in your advice class.

## When to use this

- Right after **Week 13 / Spring 3** (or whenever your cohort covers these READMEs)
- Before building a REST API with DTOs and a global exception handler
- When you forget *where* validation belongs or *why* `pjp.proceed()` must be returned in `@Around` advice

## License

MIT — see [LICENSE](LICENSE).