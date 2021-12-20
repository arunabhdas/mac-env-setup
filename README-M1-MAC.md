# M1 mac-env-setup
RoR on M1 mac (Monterey 12.0.1 (21A559))

Below is the system ruby
==> ruby --version
ruby 2.6.8p205 (2021-07-07 revision 67951) [universal.arm64e-darwin21]



==> rails --version
Rails is not currently installed on this system. To get the latest version, simply type:

    $ sudo gem install rails

You can then rerun your "rails" command.

==> brew install rbenv

==> brew upgrade rbenv ruby-build

==> rbenv install 3.0.3

==> rbenv versions
* system
  3.0.3 (set by /Users/coder/repos/appliaison/bitbucketrepos/rndflo-io/.ruby-version)

==> cd to project folder

==> cd <myproject>
  
==> rbenv local 3.0.3

==> cat .ruby-version 
3.0.3

==> rbenv versions
  system
* 3.0.3 (set by /Users/coder/repos/appliaison/bitbucketrepos/rndflo-io/.ruby-version)

==> rbenv version
3.0.3 (set by /Users/coder/repos/appliaison/bitbucketrepos/rndflo-io/.ruby-version)
    
~~~    
==> rbenv init -
export PATH="/Users/coder/.rbenv/shims:${PATH}"
export RBENV_SHELL=bash
source '/opt/homebrew/Cellar/rbenv/1.2.0/libexec/../completions/rbenv.bash'
command rbenv rehash 2>/dev/null
rbenv() {
  local command
  command="${1:-}"
  if [ "$#" -gt 0 ]; then
    shift
  fi

  case "$command" in
  rehash|shell)
    eval "$(rbenv "sh-$command" "$@")";;
  *)
    command rbenv "$command" "$@";;
  esac
}
~~~    


## Links 
    
https://github.com/rbenv/rbenv/wiki/Why-rbenv%3F
    
https://stackoverflow.com/questions/10940736/rbenv-not-changing-ruby-version

    First step is to find out which ruby is being called:

$ which ruby
Your system says:

/usr/bin/ruby
This is NOT the shim used by rbenv, which (on MacOS) should look like:

/Users/<username>/.rbenv/shims/ruby
The shim is actually a script that acts like a redirect to the version of ruby you set.

I recommend that for trouble shooting you unset the project specific "local" version, and the shell specific "shell" version and just test using the "global" version setting which is determined in a plain text file in ~/.rbenv/version which will just be the version number "1.9.3" in your case.

$ rbenv global 1.9.3
$ rbenv local --unset
$ rbenv shell --unset
You can do ls -laG in the root of your project folder (not the home folder) to make sure there is no longer a ".ruby-version" file there.

You can use rbenv versions to identify which version rbenv is set to use (and the location and name of the file that is setting that):

$ rbenv versions
NONE OF THAT MATTERS until you set the path correctly.

Use this to make sure your *MacOS will obey you:

$ rbenv init -
Followed by:

$ which ruby
To make sure it looks like:

/Users/<username>/.rbenv/shims/ruby
Then run this to add the line to your profile so it runs each time you open a new terminal window:

$ echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
There are other ways to modify the path, feel free to substitute any of them instead of running the rbenv init.

NOTE: reinstall Rails with:

$ gem install rails
If you were trying to run Ruby on Rails, then you need to have this all working first, then install the rails gem again. A previous install of Rails will use a hard coded path to the wrong ruby and several other things will be in the wrong place, so just install the gem again.

P. S. If your MacOS won't obey you (*mentioned above) then you may have to find another way to modify your path, but that's unlikely to be a problem because "Macs just work" ;)
    
