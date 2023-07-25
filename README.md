# NodeJS_Sample0

## How to run the application
Run the command:

```
node sample0.js
```
## Github actions for this application
This is the build.yml file for continuous integration in Github actions:

```yml
name: Node.js Build

on:
  push:
    branches:
      - main  # Adjust this to your main branch name if it's different

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Set up Node.js
        uses: actions/setup-node@v2
        with:
          node-version: '14'  # Choose your preferred Node.js version

      - name: Build and run Node.js app
        run: |
          node sample0.js
```
