1. Create a new mono repo

- npm init -y

2. Create a new apps

- mkdir apps
- `npx create-next-app apps/blog --ts --use-npm`

3. Create a new dashboard app using vite

- npm create vite@latest
- name it as `dashboard`

4. Create a new libs/utils shared libary

- mkdir libs/utils
- cd libs/utils, run `npm init -y`
- cd back to project roots, install tsup with `npm i tsup --save-dev -w @monorepo/utils`

5. Install a package:

- Install `lodash` in a libs/utils, run `npm install lodash -w=@monorepo/utils`
- Install `lodash` in all projects, run `npm install lodash -ws`
- Install `lodash` in workspace root, run `npm install lodash -W`

6. Build projects, project

- To build a specific project, run `npm run build -w @monorepo/utils`
- To build all the projects in the workspaces, run `npm run build -ws`
