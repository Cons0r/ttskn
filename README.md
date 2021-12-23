# Pre-built tech stack ttskn(TS, TailwindCSS, SvelteKit, Netlify) Pronounced Tisk-N or Tiskin
To start run
```
npm i
```
## Testing
```bash
npm run dev
```
## publishing (netlify)
1. Create a [Netlify Account](https://app.netlify.com)
2. Create a github repository using [The github UI](https://github.com) OR [The github CLI](https://github.com/cli/cli#installation)
### UI
After creating the repo (as you usually do) run
```bash
git init # if you havent already
git remote add origin github.com/<username>/<repo>.git
git add .
git commit -am "Initial commit"
git branch -M main
git push --set-upstream origin main
```
### CLI
```bash 
git init # if you havent already
gh repo create # this will ask the repo name and if you want to add remote.
git add .
git commit -am "Inition commit"
git push --set-upstream origin master
```
3. Add your repo to netlify. If you have created your account you should be able to login to the [Netlify Console](https://app.netlify.com), here you can create your team and link github account, after doing so create the app from your github repo
## publishing (without netlify)
find the sveltekit adapter for your platform here is the [folder the adapters are saved](https://github.com/sveltejs/kit/tree/master/packages), if you cant find the one you need try adapter-auto.  
Run
```bash
npm uninstall adapter-netlify
npm i -D @sveltejs/adapter-<type>@next
```
change
```js
import adapter from '@sveltejs/adapter-netlify';
```
in svelte.config.js to
```js
import adapter from '@sveltejs/adapter-<type>';
```