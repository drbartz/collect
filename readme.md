# Collect
Collect gathers basic stats from the operating system with the help of psutil
and python.

Thanks [Felix Richter, makefu](https://github.com/makefu/) original fork from https://github.com/makefu/Statser

Focus is portability and therefore the ability to have a usable stats generator
working under windows and linux. primarily windows as currently there is
nothing usable under windows which generates stats and writes them to for
example graphite.

# Graphite Support
Primary target is the ability to write stats to a graphite node, still it
should not be too hard to append more possible targets, even though these are
not in scope.

# Install PreReqs
    pip install -r deps.lst

# Create log file
	sudo useradd collect -s /sbin/nologin
	sudo touch /var/log/collect.log
	sudo chmod 664 /var/log/collect.log
	sudo chown collect:collect /var/log/collect.log

# initial settins
	cp -a src/settings.py_example src/settings.py

# Running
	src/collect.py

