---
layout: post
title:  "Test post-code"
date:   2020-08-10
author: Choi kwanghyun
categories: Exercise
---
##  인사
안녕하세요. 프로젝트 카테고리 테스트 페이지입니다.


###  설명글

임시로 제가 gui 300 * 300 스윙 프레임을 하나 만들어 보았습니다.

###  Code

Java로 구현하였고 코드는 아래와 같습니다.

{% highlight html %}
{% raw %}
import javax.swing.*;

public class MyFrame extends JFrame {
	MyFrame(){
		setTitle("300 * 300 스윙 프레임 만들기");
		setSize(300, 300);
		setVisible(true);
	}
	
	public static void main(String[] args) {
		MyFrame frame = new MyFrame();
	}
}
{% endraw %}
{% endhighlight %}

감사합니다.

###  Capture
