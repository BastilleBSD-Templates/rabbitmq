# rabbitmq
Bastille Template for RabbitMQ jail

 STATUS: Testing`

RabbitMQ is a message queue system. It lets computer programs send each 
other work to do, without waiting for them to do it.


After applying the template and running it you have to do several steps to use this template.

Create an administrative user for your server.

	rabbitmqctl add_user administrator choose_a_password
	rabbitmqctl set_permissions -p  / administrator “.*” “.*” “.*”
	rabbitmqctl set_user_tags administrator administrator

If you want the web-based management interface, run the following command:


	rabbitmq-plugins enable rabbitmq_management

Use a web browser to look at your server at http://your-server-ip:15672/ . Port 15672 
is the RabbitMQ web administration portal.

Finally, install the RabbitMQAdmin program where your user can get to it on your FreeBSD 
machine. This program is a script provided by the web administration portal. (It needs 
python 2.7 to run.)

	wget http://127.0.0.1:15672/cli/rabbitmqadmin

	chmod 0755 rabbitmqadmin



