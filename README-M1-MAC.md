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


## Links 
https://stackoverflow.com/questions/10940736/rbenv-not-changing-ruby-version
