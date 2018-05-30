language: node_js
node_js:
- '6'
cache:
  bundler: true
  directories:
  - node_modules
script: 
  - npm run release

deploy:
  provider: npm
  email: supermanchc@gmail.com
  api_key: $NPM_KEY
  on:
    tags: true
    branch: master
    skip_cleanup: true