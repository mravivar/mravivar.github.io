## Github Pages and Jekyll
Jekyll uses kramdown to process and convert md files to static HTML files

- github pages documentation
  [github](https://docs.github.com/en/pages/quickstart)

- set up
  ```
  brew install chruby ruby-install xz

  ruby-install ruby 3.1.3

  echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.bash_profile
  echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.bash_profile
  echo "chruby ruby-3.1.3" >> ~/.bash_profile # run 'chruby' to see actual version

  ruby -v

  gem install jekyll
  ```

- run locally
  ```
  cd docs
  bundle install .
  ```

- to update github pages gem [github](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll#updating-the-github-pages-gem)
  ```
  bundle update github-pages # if you have bundler
  gem update github-pages # otherwise
  ```

__________

## Set up new jekyll site
1. commands
  ```
  git clone your-repository
  cd your-repository
  jekyll new --skip-bundle .
  (or)
  jekyll new --skip-bundle . --force
  ```

2. update Gemfile  
  [github](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll)

3. run commands
  ```
  bundle add webrick
  bundle install
  bundle exec jekyll serve
  ```

4. verify locally  
  [http://localhost:4000](http://localhost:4000)

5. git push

__________

## Known Issue
# h1
## h2
### h3
#### h4
##### h5
###### h6
