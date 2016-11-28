## NYCDA Backend Exam - Part 3

### 1 - What is the difference between git pull and git merge?
Git pull runs a remote git fetch and then a git merge to your current branch. If you want to bring your local repository up to speed with a remote repository that is what you would run.

***git merge [sourceBranch]***: merges the sourceBranch to your current branch.

### 2 - Why do we use a pull request on github instead of merging our branch directly to master and then pushing it to github?
To review changes first to make sure we want them in master, or any other Pull Request destination. It is easier to comment on code and see changes with pull requests.

### 3 - Why do we use database migrations?
Because its way easier to alter the table this way with an ORM rather than doing SQL quires. It also keep a schema change history for collabroation purposes.

### 4 - What is the difference between up and down functions of sequelize migration files?
Up function is for migrations, down function for rollbacks.

### 5 - Name 3 reasons why Sass/SCSS is better than CSS?
1 - We can combine different scss files together with ```@import```
2 - We can use variables
3 - We can nest definitions

### 6 - What is the right way to include bootstrap to your project?
Download the bootstrap package with npm. Then ```@import``` all the individual bootstrap files in your scss directory, according to their order in the actual bootstrap.scss

### 7 - Why _variables.scss file is important?
all bootstrap styling values are defined in the _variables.scss. By changes those values we can theme/adjust bootstrap to our needs.

### 8 - Lets say you want to change the alert component of bootstrap, what are steps/strategy would you use to make that change?
- First try to see if you can override the bootstrap _variables.scss file, by changing the variables _alerts.scss uses.
- If that isnt satisfactory then create your own _alerts.scss file under your custom /bootstrap folder and write the styling scoped to the .alert {}
- if your styling is unrelated to the bootstrap alert component you should create your own component file and include it in your build process, application.css
