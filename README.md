### 远程文件管理器使用说明 


​	使用要求：

​			需要安装jdk8 以上

​			需要安装启动redis（默认的端口即可）
       https://github.com/tporadowski/redis/releases
       windows: redis-server.exe
       https://redis.io/download
       linux:./redis-server
       
       Installation Redis in linux
              Download, extract and compile Redis with:
                     $ wget https://download.redis.io/releases/redis-6.2.6.tar.gz
                     $ tar xzf redis-6.2.6.tar.gz
                     $ cd redis-6.2.6
                     $ make

​	解压之后，打开application.yml

​	修改以下几个地方

 * file:
   	   path: C:/TEMP/         #改成自己的路径
 * user:
     data:
       uname: admin		#用户名，改成自己的用户名
       upwd: admin             #密码，改成自己安全的密码
 * server:
     port: 80		         #访问端口，改一个数字，访问路径是   http://localhost:你的端口/




改好之后，双击	开启.bat  ,稍等10秒，访问 http://localhost:你的端口/

Run in aliyun:

nohup java -jar /root/file-upload-and-dowload-0.0.1-SNAPSHOT.jar >/dev/null 2>&1 & 
nohup /root/redis/redis-6.2.6/src/redis-server >/dev/null 2>&1 & 
