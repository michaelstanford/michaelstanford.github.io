---
layout: post
title: "Objects - a style guide"
description: ""
comments: true
keywords: "dummy content, lorem ipsum"
---

# Heuristics

## Object Creation
1. Inject dependencies and configuration values as constructor arguments.
2. Inject only what you need, not where you can get it from.
3. All constructor arguments are required.
4. Only use constructor injection.
    - No setters
5. There's no such thing as an optional dependency.
    - No `MyDependency = null` anywhere
6. Make all dependencies explicit
    - Turn static dependencies into object dependencies
    - Turn complicated functions into object dependencies
    - Make system calls explicit
        - `new DateTime()` is a system call. When used, it will ask for the information from its environment. 
7. Data relevant for a specific task should be passed as method arguments instead of constructor arguments.
8. Don't let object behavior change after instantiation.