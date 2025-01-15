# Dockerfile Best Practices
This example demonstrates a common pitfall in Dockerfiles: using `ubuntu:latest` and not specifying the Python version, which can lead to unexpected issues.
The solution shows how to improve it with a specific tag and explicit python version.  This ensures reproducibility and minimizes compatibility problems.

## Bug
The provided `Dockerfile_bug` uses `ubuntu:latest`, resulting in a non-reproducible build. It also fails to define a specific Python version, potentially leading to unexpected behavior. The `CMD` instruction is also basic and could benefit from being wrapped in an `ENTRYPOINT`.

## Solution
The `Dockerfile_solution` addresses these issues.  It uses a specific Ubuntu version (22.04), specifies python 3.9, improves the cmd instruction with an entrypoint to allow for better command execution.
