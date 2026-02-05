- Define a Runner (execution environment)
```yml
jobs:
	first-job:
	runs-on: ubuntu-latest
```

- Contain one or more [[Steps]]
```yml
  first-job:
    runs-on: ubuntu-latest
    steps:
      - name: Print Hello
        run: echo "Hello"
      - name: Print Goodbye
        run: echo "Bye"
```

- Run in parallel (**default**) or sequential
- Can run under certain conditions ("needs")
```yml
# The "deloy" job needs the "test" job to run first
deploy:
	needs: test
	runs-on: ubuntu-latest 
```

- **Every job gets its own runner, its own VM that's. totally isolated from other machines and jobs

