一、实验目的
1.掌握字符串String及其方法的使用
2.掌握异常处理结构
二、实验内容
利用已学的字符串处理知识编程完成《长恨歌》古诗的整理对齐工作，写出功能函数，并运行。达到如下功能：
1.每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”
2.允许提供输入参数，统计古诗中某个字或词出现的次数
3.考虑操作中可能出现的异常，在程序中设计异常处理程序

输入：汉皇重色思倾国御宇多年求不得杨家有女初长成养在深闺人未识天生丽质难自弃一朝选在君王侧回眸一笑百媚生六宫粉黛无颜色春寒赐浴华清池温泉水滑洗凝脂侍儿扶起娇无力始是新承恩泽时云鬓花颜金步摇芙蓉帐暖度春宵春宵苦短日高起从此君王不早朝承欢侍宴无闲暇春从春游夜专夜后宫佳丽三千人三千宠爱在一身金屋妆成娇侍夜玉楼宴罢醉和春姊妹弟兄皆列士可怜光采生门户遂令天下父母心不重生男重生女骊宫高处入青云仙乐风飘处处闻缓歌慢舞凝丝竹尽日君王看不足渔阳鼙鼓动地来惊破霓裳羽衣曲九重城阙烟尘生千乘万骑西南行<未完，待续>
输出：
汉皇重色思倾国，御宇多年求不得。
杨家有女初长成，养在深闺人未识。
天生丽质难自弃，一朝选在君王侧。
回眸一笑百媚生，六宫粉黛无颜色。
春寒赐浴华清池，温泉水滑洗凝脂。
侍儿扶起娇无力，始是新承恩泽时。
云鬓花颜金步摇，芙蓉帐暖度春宵。
春宵苦短日高起，从此君王不早朝。
…………
三、实验过程
1.将该段文字打包成数组放在一个字符数组中
2.用for循环每7个字添加一个逗号，每14字添加一个句号和换行符“\n”
3．对比字符是否相等，输出相同字符数目
四、流程图
![image](https://github.com/CristianoRonaldoDD/liduo/blob/master/d.png)
五、核心代码
1.将该段文字打包成数组放在一个字符数组中
		String line = new String(args[0]);	
		c  = line.length();
		char[] chs=line.toCharArray();
		System.out.println(Arrays.toString(chs));
		    char[] newchs;
2.用for循环每7个字添加一个逗号，每14字添加一个句号和换行符“\n”
		for(a=0,b=7;a<c;a+=14,b+=14)
		{	
			newchs = Arrays.copyOfRange(chs, a, b);
			for(char s:newchs)				
			    System.out.print(s);
			    System.out.print(",");
			newchs = Arrays.copyOfRange(chs, a+7, b+7);
			for(char s:newchs)
				System.out.print(s);
				System.out.print("。");
				System.out.print("\n");  
		}
3．对比字符是否相等，输出相同字符数目
		String str = new String(args[0]);
		int count=0;
		String str1= s;
		while(str.indexOf(str1)!=-1)//返回指定字符在字符串中第一次出现处的索引，如果此字符串中没有这样的字符，则返回 -1。
		{			
			int d=str.indexOf(str1);
	        str=str.substring(d+str1.length());
	        count++;
	    }
		System.out.println(s+"出现的次数为"+count);
六、实验结果
 ![image](https://github.com/CristianoRonaldoDD/liduo/blob/master/l.png)
七、实验感想
