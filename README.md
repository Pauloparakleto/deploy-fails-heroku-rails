# Deploy buildpack ruby heroku bug

This evening I tried to deploy the actual release of my project and also previous releases.

How to reproduce the behavior below.
Steps:
1) generate a new rails with the pg database; jump to inside it.
2) run db:create
3) run rails server
Checking it is ok, push this to the heroku. I used the CLI. So...
4) `heroku git:remote -a deploy-test-node`;
5) `git add.`
6) `git commit -am "initial"`
7) `git push heroku master`


## It is supposed to run the same error

remote:        Compiling...

remote:        Compilation failed:

remote:        yarn run v1.22.17

remote:        info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.

remote:        

remote:        
remote:        error Command "webpack" not found.
remote:        
remote: 
remote:  !
remote:  !     Precompiling assets failed.

remote:  !
remote:  !     Push rejected, failed to compile Ruby app.

remote: 
remote:  !     Push failed

remote: Verifying deploy...

remote: 
remote: !       Push rejected to deploy-test-node.

remote: 
To https://git.heroku.com/deploy-test-node.git

 ! [remote rejected] master -> master (pre-receive hook declined)

error: failed to push some refs to 'https://git.heroku.com/deploy-test-node.git'``