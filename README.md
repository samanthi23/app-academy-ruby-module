App Acadmey - Ruby Module

Git Module

Installation Instructions for Git Module: 

# install git
brew install git

# makes git terminal output pretty
git config --global color.ui true

# this will mark you as the 'author' of each committed change
git config --global user.name "your name here"

# use the email associated with your GitHub account
git config --global user.email your_email_here

Installation of Rbenv and Ruby

# update 
Installation of rbenv and Ruby: 

1. Update your system

sudo yum update
2. Install build-essential

sudo yum install -y build-essential
3. Install rbenv

git clone https://github.com/sstephenson/rbenv.git ~/.rbenv
4. Install ruby-build

git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build
**5. Add to ~/.bash_"

$ echo 'export PATH="~/.rbenv/bin:$PATH"' >> ~/.bashrc
$ echo 'eval "$(rbenv init -)"' >> ~/.bashrc
**6. **

shopt -s expand_aliases
source ~/.bashrc
7. Verify rbenv installation

type rbenv
You should get a message saying that rbenv is a function
8.Verify rbenv versions

rbenv versions
9. Verify current ruby version

ruby -v
10.Install another ruby version

rbenv install 2.5.0
11. Verify all rbenv install versions

rbenv versions 
12.Set a new local version

rbenv local 2.5.0
If you get a permission error, close and reopen your terminal and workspace.

**13. Finally, check your current rbenv version"

rbenv version	
14. Way to go!
15.

Installation of Pry and Byebug - gems

gem install bundler pry byebug



1. Installation of Postgres 

sudo yum install postgresql postgresql-server postgresql-devel postgresql-contrib postgresql-docs

sudo service postgresql initdb

2. Edit postgres conf to connect via localhost: 5432

sudo emacs /var/lib/pgsql9/data/postgresql.conf

ctrl X, ctrl C

3. uncomment

#listen_addresses = 'localhost'
#port = 5432

4. Update pg_hba.conf file for ec2-user auth:

sudo emacs /var/lib/pgsql9/data/pg_hba.conf

# TYPE  DATABASE        USER            ADDRESS                 METHOD
# "local" is for Unix domain socket connections only
local   all             all                                     trust
# IPv4 local connections:
host    all             ec2-user        127.0.0.1/0             trust
# IPv6 local connections:
host    all             all             ::1/128                 md5

5. Start / Restart postgres server

sudo service postgresql start 

or sudo service postgresql restart

6. Login and change password

sudo su - postgres # login as postgres user

psql -U postgres # login to postgres db as postgres user

Change Password:

ALTER USER postgres WITH PASSWORD 'YOUR_PASSWORD';

Add ec2-user :

CREATE USER "ec2-user" SUPERUSER;

ALTER USER "ec2-user" WITH PASSWORD 'YOUR_PASSWORD';

Exit postgres:

postgres=# \q

Logout of postgres user account:

exit

Installation of SQLite:

1. brew install sqlite

or brew reinstall sqlite # if already installed

sqlite3

# open SQLite CLI with this command
sqlite3

#  you should see this output
# SQLite version 3.16.0 2016-11-04 19:09:39
# Enter ".help" for usage hints.
# Connected to a transient in-memory database.
# Use ".open FILENAME" to reopen on a persistent database.

# .q to quit
sqlite> .q

exit 

1. Login to Postgres from ec2-user ( or username )
 
psql postgres


Happy coding! 

AWS EC2 instance !!

========================

DATA STRUCTURES:
(in Ruby)

========================

#BFS 

```
queue = [ root ]
until queue.empty?
    el = queue.shift
    process!(el) #return if it's 7 or else skip it
    el.children.each { |child | 
    queue << child }
end
```

#DFS ( Depth First Search ) # uses a stack

```
def dfs ( root, target )
    return nil if root is nil 
    return root if root.val == target
    root.children.each do |child |
        search_result = dfs( child, target )
        return search_result 
    end
    nil

end
```

base case:  

root.nil? false # or return nil if you didn't find something

root.val == target # root

# if I dfs on the left side or right side 
# person is on the left side


```
def dfs ( root, target )
    return nil if root is nil 
    return root if root.val == target
    root.children.each do | child | 
        search_result = dfs ( child, target )
        return search_result unless search_result.nil?
    end
    nil
end
```