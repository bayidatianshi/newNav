# newNav
为了做出更加优雅的导航网站
##修改日期2019年6月24日
##修改人：黄镇杰
主要修改内容：
1.在website-data中添加了学者网和砺儒云课堂两个网站的信息
2.修改了index的个人收藏功能，为了实现刷新后不重置收藏的情况，使用了cookie
	增加了一下几个函数：
	（1）set_cookie(collects)：设置cookie
	（2）get_cookie(can_collect)：根据参数获取cookie
	（3）get_all_collections()：获取保存在cookie中的所有的收藏网站
	（4）del_cookie()：删除cookie
	（5）check_cookie_exist()：检测cookie文件是否存在，不存在就使用默认的cookie文件了
	修改了以下的函数：
	（1）collect(starId)：在该函数最后添加删除旧cookie以及生成新cookie的功能
	（2）初始操作（$function()）：添加了cookie文件的判断，判断是否已经存在cookie文件，存在就使用cookie文件中的收藏网址，不存在就是用默认的收藏网址
	
##修改日期2019年7月10日
##修改人：黄镇杰
主要修改内容：
1.在推荐功能中实现了根据热度实时更新推荐的网址
2.主要增加了以下代码：
	（1）在js/website-data.js 中增加了webname的内容，把所有网站的名字的存在一个数组中
	（2）在index.html中增加了generate_top_welcome_website(return_web_quantity)函数，获取return_web_quantity个热度最高的网址
	（3）在index.html中增加了generateWelcomeWebRecommend()函数用于在获取热度网站之后修改页面使用
