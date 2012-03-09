ros_comm_upstart
================

This project is a native Debian package, i.e. the only way to use it
is through the generated Debian package.

They can be found on the Downloads section of the GitHub project:
https://github.com/laas/ros_comm_upstart/downloads

1. Download the last version
2. Install it:
`$ sudo dpkg -i ./ros-electric-ros-comm-upstart_*_all.deb`
3. Enjoy!

roscore is now available as a service running as a separate user.

The Debian package creates a user and a group called 'ros'.
The system user home directory is '/var/lib/ros'.

As any other upstart service, it can be controlled as follow:

   * start: `start roscore`
   * stop: `stop roscore`
   * restart: `restart roscore`
   * status: `status roscore`

The log files are stored in `/var/log/ros` and cleaned using logrotate
regularly.

The roscore process id is stored in `/var/run/roscore.pid`.

Uninstalling the package will *not* delete the user nor the group.
You have to do it manually. The user home directory as well as the
logs will also remain on the filesystem.

Use the GitHub issue tracker to report feedbacks and bugs:
https://github.com/laas/ros_comm_upstart/issues
