查看系统中是否有bootchar可执行文件
echo 120 > /data/bootchart/start
重启
在 /data/bootchart/目录下会生成几个文件，拷贝出来
利用源码自带的分析工具：/system/core/init/grab-bootchart.sh将这几个文件生成bootchart.tgz压缩包
sudo apt-get install bootchart udo apt-get install pybootchartgui安装bootchart工具
java -jar /usr/share/bootchart/bootchart.jar  /path/bootchart.tgz解析bootchart文件






第二种：
先生成bootchart.tgz（tar -czf bootchart.tgz header proc_diskstats.log proc_ps.log proc_stat.log ），把bootchart-0.92.zip压缩包解压，然后bootchart.tgz放到该目录下，执行
java -jar bootchart.jar bootchart.tgz
就生成了。