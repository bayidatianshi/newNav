# newNav\<br>
为了做出更加优雅的导航网站\<br>
\<br>
修改日期2019年6月24日\<br>
修改人：黄镇杰\<br>
主要修改内容：\<br>
1.在website-data中添加了学者网和砺儒云课堂两个网站的信息\<br>
2.修改了index的个人收藏功能，为了实现刷新后不重置收藏的情况，使用了cookie\<br>
	增加了一下几个函数：\<br>
	（1）set_cookie(collects)：设置cookie\<br>
	（2）get_cookie(can_collect)：根据参数获取cookie\<br>
	（3）get_all_collections()：获取保存在cookie中的所有的收藏网站\<br>
	（4）del_cookie()：删除cookie\<br>
	（5）check_cookie_exist()：检测cookie文件是否存在，不存在就使用默认的cookie文件了\<br>
	修改了以下的函数：\<br>
	（1）collect(starId)：在该函数最后添加删除旧cookie以及生成新cookie的功能\<br>
	（2）初始操作（$function()）：添加了cookie文件的判断，判断是否已经存在cookie文件，存在就使用cookie文件中的收藏网址，不存在就是用默认的收藏网址\<br>
	