# www.stalexisoca.org

## new user setup

- add to `~/.ssh/config`
```
Host stalexisoca.github.com
  Hostname github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_sk_rk_github_stalexisoca
```
- `git clone https://github.com/stalexisoca/www.stalexisoca.org.git`
- `git config user.name stalexisoca`
- `git config user.email 'stalexisoca@users.noreply.github.com'`
- `git remote set-url --push origin git@stalexisoca.github.com:stalexisoca/www.stalexisoca.org.git`
- `git fetch --all`
- `git branch --track gh-pages origin/gh-pages`

## dev notes

- `find www/ -type f -exec chmod 0644 {} \;`
- `find www/ -type d -exec chmod 0755 {} \;`

bundle install;

cd www;

JEKYLL_ENV=development bundle exec jekyll serve --host 0.0.0.0;

or

JEKYLL_ENV=production bundle exec jekyll build;

for example:

cd /path-to/www.stalexisoca.org/www/ && git pull && bundle install && JEKYLL_ENV=production bundle exec jekyll build
