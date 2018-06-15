# テクノロジー（藤原） 授業 6/8

今日の授業で打ったコマンドをコピー＆ペーストしてください。

（`irb`や`ruby`の実行結果も含めて全てをコピーしてください）

## ターミナルに打ったコマンド

```
MacBook-Proi:~ inoueshunji$ cd fujiwara

MacBook-Proi:fujiwara inoueshunji$ git clonegit@github.com:M-ghaffari/ruby-chap1-intro.git
Cloning into 'ruby-chap1-intro'...
remote: Counting objects: 6, done.
remote: Compressing objects: 100% (5/5), done.
remote: Total 6 (delta 0), reused 3 (delta 0), pack-reused 0
Receiving objects: 100% (6/6), done.
MacBook-Proi:fujiwara inoueshunji$ cd ruby-chap1-intro

MacBook-Proi:ruby-chap1-intro inoueshunji$ brew install rbenv
Updating Homebrew...
==> Installing dependencies for rbenv: autoconf, pkg-config, openssl, ruby-build
==> Installing rbenv dependency: autoconf
==> Downloading https://homebrew.bintray.com/bottles/autoconf-2.69.high_sierra.bottle.4.tar.gz
######################################################################## 100.0%
==> Pouring autoconf-2.69.high_sierra.bottle.4.tar.gz
==> Caveats
Emacs Lisp files have been installed to:
  /usr/local/share/emacs/site-lisp/autoconf
==> Summary
🍺  /usr/local/Cellar/autoconf/2.69: 71 files, 3.0MB
==> Installing rbenv dependency: pkg-config
==> Downloading https://homebrew.bintray.com/bottles/pkg-config-0.29.2.high_sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring pkg-config-0.29.2.high_sierra.bottle.tar.gz
🍺  /usr/local/Cellar/pkg-config/0.29.2: 11 files, 627.2KB
==> Installing rbenv dependency: openssl
==> Downloading https://homebrew.bintray.com/bottles/openssl-1.0.2o_1.high_sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring openssl-1.0.2o_1.high_sierra.bottle.tar.gz
==> Caveats
A CA file has been bootstrapped using certificates from the SystemRoots
keychain. To add additional certificates (e.g. the certificates added in
the System keychain), place .pem files in
  /usr/local/etc/openssl/certs

and run
  /usr/local/opt/openssl/bin/c_rehash

This formula is keg-only, which means it was not symlinked into /usr/local,
because Apple has deprecated use of OpenSSL in favor of its own TLS and crypto libraries.

If you need to have this software first in your PATH run:
  echo 'export PATH="/usr/local/opt/openssl/bin:$PATH"' >> ~/.bash_profile

For compilers to find this software you may need to set:
    LDFLAGS:  -L/usr/local/opt/openssl/lib
    CPPFLAGS: -I/usr/local/opt/openssl/include
For pkg-config to find this software you may need to set:
    PKG_CONFIG_PATH: /usr/local/opt/openssl/lib/pkgconfig

==> Summary
🍺  /usr/local/Cellar/openssl/1.0.2o_1: 1,791 files, 12.3MB
==> Installing rbenv dependency: ruby-build
==> Downloading https://github.com/rbenv/ruby-build/archive/v20180601.tar.gz
==> Downloading from https://codeload.github.com/rbenv/ruby-build/tar.gz/v20180601
######################################################################## 100.0%
==> ./install.sh
🍺  /usr/local/Cellar/ruby-build/20180601: 399 files, 201.5KB, built in 4 seconds
==> Installing rbenv
==> Downloading https://homebrew.bintray.com/bottles/rbenv-1.1.1.high_sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring rbenv-1.1.1.high_sierra.bottle.tar.gz
🍺  /usr/local/Cellar/rbenv/1.1.1: 36 files, 62.7KB
MacBook-Proi:ruby-chap1-intro inoueshunji$ echo 'eval “$(rbenv init -)”' >> ~/.bash_profile
MacBook-Proi:ruby-chap1-intro inoueshunji$ source ~/.bash_profile
-bash: eval: line 5: syntax error near unexpected token `('
-bash: eval: line 5: `“export PATH="/Users/inoueshunji/.rbenv/shims:${PATH}" export RBENV_SHELL=bash source '/usr/local/Cellar/rbenv/1.1.1/libexec/../completions/rbenv.bash' command rbenv rehash 2>/dev/null rbenv() { local command command="$1" if [ "$#" -gt 0 ]; then shift fi case "$command" in rehash|shell) eval "$(rbenv "sh-$command" "$@")";; *) command rbenv "$command" "$@";; esac }”'
MacBook-Proi:ruby-chap1-intro inoueshunji$ rbenv install 2.5.1
ruby-build: use openssl from homebrew
Downloading ruby-2.5.1.tar.bz2...
-> https://cache.ruby-lang.org/pub/ruby/2.5/ruby-2.5.1.tar.bz2
Installing ruby-2.5.1...
load: 2.87  cmd: clang 18094 running 0.00u 0.00s
load: 4.42  cmd: ruby 33671 running 20.93u 0.68s
load: 4.42  cmd: ruby 33671 running 21.25u 0.68s
load: 4.42  cmd: ruby 33671 running 21.56u 0.69s
load: 4.42  cmd: ruby 33671 running 21.78u 0.69s
load: 4.42  cmd: ruby 33671 running 21.97u 0.70s
Installed ruby-2.5.1 to /Users/inoueshunji/.rbenv/versions/2.5.1

MacBook-Proi:ruby-chap1-intro inoueshunji$ rbenv global 2.5.1

MacBook-Proi:ruby-chap1-intro inoueshunji$ vi ~/.bash_profile
MacBook-Proi:ruby-chap1-intro inoueshunji$ source ~/.bash_profile
-bash: eval: line 2: syntax error near unexpected token `('
-bash: eval: line 2: `“export PATH="/Users/inoueshunji/.rbenv/shims:${PATH}" export RBENV_SHELL=bash source '/usr/local/Cellar/rbenv/1.1.1/libexec/../completions/rbenv.bash' command rbenv rehash 2>/dev/null rbenv() { local command command="$1" if [ "$#" -gt 0 ]; then shift fi case "$command" in rehash|shell) eval "$(rbenv "sh-$command" "$@")";; *) command rbenv "$command" "$@";; esac }”'
MacBook-Proi:ruby-chap1-intro inoueshunji$ vi ~/.bash_profile
MacBook-Proi:ruby-chap1-intro inoueshunji$ rbenv init
# Load rbenv automatically by appending
# the following to ~/.bash_profile:

eval "$(rbenv init -)"

MacBook-Proi:ruby-chap1-intro inoueshunji$ vi ~/.bash_profile
MacBook-Proi:ruby-chap1-intro inoueshunji$ source ~/.bash_profile
MacBook-Proi:ruby-chap1-intro inoueshunji$ rbenv versions
  system
* 2.5.1 (set by /Users/inoueshunji/.rbenv/version)
MacBook-Proi:ruby-chap1-intro inoueshunji$ ruby -v
ruby 2.5.1p57 (2018-03-29 revision 63029) [x86_64-darwin17]
 
MacBook-Proi:ruby-chap1-intro inoueshunji$ ruby hrlloruby.rb
Traceback (most recent call last):
ruby: No such file or directory -- hrlloruby.rb (LoadError)
MacBook-Proi:ruby-chap1-intro inoueshunji$ ruby helloruby.rb
Heloo,_Ruby./nMacBook-Proi:ruby-chap1-intro inoueshunji$ cd
MacBook-Proi:~ inoueshunji$ cd fujiwara
MacBook-Proi:fujiwara inoueshunji$ cd fujiwara
-bash: cd: fujiwara: No such file or directory
MacBook-Proi:fujiwara inoueshunji$ ls
hello-github		ruby-chap1-intro
ionic-tutorial
MacBook-Proi:fujiwara inoueshunji$ cd ruby-chap1-intro/
MacBook-Proi:ruby-chap1-intro inoueshunji$ ruby helloruby.rb
Heloo,_Ruby.

```
```
MacBook-Proi:ruby-chap1-intro inoueshunji$ irb --simple-prompt
>> x+1
Traceback (most recent call last):
        2: from /Users/inoueshunji/.rbenv/versions/2.5.1/bin/irb:11:in `<main>'
        1: from (irb):1
NameError (undefined local variable or method `x' for main:Object)
>> cd
Traceback (most recent call last):
        2: from /Users/inoueshunji/.rbenv/versions/2.5.1/bin/irb:11:in `<main>'
        1: from (irb):2
NameError (undefined local variable or method `cd' for main:Object)
>> lv
Traceback (most recent call last):
        2: from /Users/inoueshunji/.rbenv/versions/2.5.1/bin/irb:11:in `<main>'
        1: from (irb):3
NameError (undefined local variable or method `lv' for main:Object)
>> 2
=> 2
>> 
>> 
>> ruby
Traceback (most recent call last):
        2: from /Users/inoueshunji/.rbenv/versions/2.5.1/bin/irb:11:in `<main>'
        1: from (irb):7
NameError (undefined local variable or method `ruby' for main:Object)
>> irb
>> exit
=> #<IRB::Irb: @context=#<IRB::Context:0x00007fe7730055e8>, @signal_status=:IN_EVAL, @scanner=#<RubyLex:0x00007fe772a02420>>
>> exit!
MacBook-Proi:ruby-chap1-intro inoueshunji$ irb --simple-prompt
>> TEST=1
=> 1
>> test=2
=> 2
>> TEST =2
(irb):3: warning: already initialized constant TEST
(irb):1: warning: previous definition of TEST was here
=> 2
>> end =1
Traceback (most recent call last):
        1: from /Users/inoueshunji/.rbenv/versions/2.5.1/bin/irb:11:in `<main>'
SyntaxError ((irb):4: syntax error, unexpected keyword_end)
end =1
^~~
>> a,b,c=1,2,3
=> [1, 2, 3]
>> a,b,*c=1,2,3,4,5
=> [1, 2, 3, 4, 5]
```
