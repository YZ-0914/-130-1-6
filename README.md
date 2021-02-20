# -130-1-6
#define _CRT_SECURE_NO_WARNINGS 1

#include<stdio.h>

//第1题
//题目描述：于老师经常告诉我们“学习编程最好的办法就是上机实践，因为你要对计算机下指令，想让计算机帮你干活，就得多和计算机‘交流’，实践才能出真知。”
//输入描述：无
//输出描述：Practice makes perfect!

//int main()
//{
//	printf("Practice makes perfect!");
//	return 0;
//}

//第2题
//题目描述：KIKI学会了printf在屏幕输出信息，他想输出一架小飞机，请帮他编写程序输出这架小飞机。
//输入描述：无
//输出描述：
//     **     
//     **
//************
//************
//    *  *
//    *  *    
//int main()
//{
//	printf("     **     \n");
//	printf("     **     \n");
//	printf("************\n");
//	printf("************\n");
//	printf("    *  *    \n");
//	printf("    *  *    \n");
//	return 0;
//}

//第2题
//每个人都想成为大V（VIP：Very Important Person），但要一点一点积累才行，先从小v做起，要求输出由小写字母v组成的大V。
//输入描述：无
//输出描述：
//v     v
// v   v 
//   v   


//int main()
//{
//	printf("v     v\n");
//	printf(" v   v \n");
//	printf("   v   \n");
//	return 0;
//}

//int main()
//{
//	printf("v     v\n v   v \n   v   \n");
//	return 0;
//}

//备注：换行使用转义字符'\n'
#include<string.h>

//int main()
//{
//	//printf("abc\ndef");
//	//C语言转义字符
//
//	printf("%d", strlen("c:\test\041\test.c"));
//	//结果是13
//	//     \t -- tab -水平制表符
//	//     \041 -- \ddd - d是8进制数字
//	//     以32作为ASCII码值代表的字符
//	printf("%c\n", '041');
//	return 0;
//
//}

//第3题
//题目描述：确定不同整型数据类型在内存中占多大（字节），输出不同整形数据类型在内存中占多大（字节）。
//输入描述：
//输出描述：
//不同整型数据类型在内存中占多大（字节），具体格式详见输出样例。输出样例中的？为不同整型数据类型在内存中占的字节数，输出样例如下：
//The size of short is ? bytes.
//The size of int is ? bytes.
//The size of long is ? bytes.
//The size of long long is ? bytes.
//int main()
//{
//	printf("The size of short is %d bytes.\n", sizeof(short));//2
//	printf("The size of int is %d bytes.\n", sizeof(int));//4
//	printf("The size of long is %d bytes.\n", sizeof(long));//4
//	printf("The size of long long is %d bytes.\n", sizeof(long long));//8
//	return 0;
//	//sizeof -操作符 - 不是函数
//	//sizeof(int)
//	int a = 10;
//	printf("%d\n", sizeof(int));
//	printf("%d\n", sizeof a);
//	printf("%d\n", sizeof(a));
//}

//第4题
//题目描述：我们处理的整数通常用十进制表示，在计算机内存中是以二进制补码形式存储，但通常二进制表示的整数比较长，为了便于在程序设计过程中理解和处理数据，通常采用八进制和十六进制，缩短了二进制补码表示的整数，但保持了二进制数的表达特点，请输出十进制整数1234对应的八进制和十六进制。
//输入描述：无
//输出描述：十进制整数1234对应的八进制和十六进制（字母大写），用空格分开，并且要求，在八进制前显示前导0，在十六进制数前显示前导0x。
//备注：printf可以使用格式控制串“%o”、“%x”分别输出八进制整数和十六进制整数，并使用修饰符“#”控制前导显示
//int main()
//{
//	printf("0%o 0x%x", 1234, 1234);
//	return 0;
//}

//%c - 字符
//%hd - 短整型
//%d - 整形
//%s - 字符串
//%f - 单精度浮点数
//%lf - 双精度浮点数
//%p - 地址格式
//……
//int main()
//{
//	printf("%d\n", 100);
//	printf("%c\n", 100);
//
//	return 0;
//}

//int main()
//{
//	printf("%s\n", "abcdef");
//	return 0;
//}

//第5题
//题目描述：一个四位数，反向输出。
//输入描述：一行，输入一个整数n（1000 <= n <= 9999)。
//输出描述：针对每组输入，反向输出应对四位数。
//示例：输入1234，输出4321
//1234
//% 10 = 4
//123
//% 10 = 3
//12
//% 10 = 2
//1
//% 10 = 1

//int main()
//{
//	int n = 0;
//	//输入
//	scanf("%d", &n);//1234
//	//输出
//	while (n!=0)
//	{
//		printf("%d", n % 10);
//		n = n / 10;
//	}
//	
//	return 0;
//}

//第6 题
//题目描述：实现字母的大小写转换，多组输入输出。
//输入描述：多组输入，每一行输入大写字母。
//示例：输入A B输出a b
//int main()
//{
//	//只能处理一个字符的-err
//	/*int ch = getchar();
//	ch = ch + 32;
//	putchar(ch);*/ 
//	int ch = 0;
//	//EOF  end of file
//	while ((ch = getchar())!=EOF)//ctrl+z结束
//	{
//		//putchar(ch + 32);
//		printf("%c\n", ch + 32);
//		getchar();//清理‘\n’
//	}
//	return 0;
//}
//输入缓冲区的概念

int main()
{
	char password[20] = { 0 };
	printf("请输入密码：>");
	scanf("%s", password);
	printf("请确认（Y/N)：>");
	getchar();//处理缓冲区的\n
	int ch = getchar();
	if (ch == 'Y')
		printf("确认成功\n");
	else
		printf("放弃确认\n");
		return 0;
}
#define _CRT_SECURE_NO_WARNINGS 1

#include<stdio.h>

//7、题目描述：KIKI学会了printf在屏幕输出信息，他想输出一架小飞机，请帮他编写程序输出这架小飞机。
//输入描述：无
//输出描述：
//    **
//    **
//************
//************
//   *   *
//   *   *
//int main()
//{
//	printf("     **     \n");
//	printf("     **     \n");
//	printf("************\n");
//	printf("************\n");
//	printf("    *  *    \n");
//	printf("    *  *    \n");
//	return 0;
//
//}

//8、题目描述：BoBo写了一个十六进制整数ABCDEF，他问KiKi对应的十进制整数是多少。
//输入描述：无
//输出描述：十六进制整数ABCDEF对应的十进制整数，所占域宽为15.
//备注：printf可以使用使用格式控制串“%md"输出域宽为m的十进制整数。
//int main()
//{
//	printf("%15d\n", 0xABCDEF);
//	return 0;
//}
//域宽
//int main()
//{
//	printf("%d\n", 15);
//	printf("%4d\n", 15);
//	return 0;
//}

//9、题目描述：KIKI写了一个输出“Hello world！"的程序，BOBO老师告诉他printf函数有返回值，你能帮助他写一个程序输出printf("Hello world!")的返回值吗？
//输入描述：无
//输出描述：包括两行：
//第一行为“Hello world!"
//第二行为printf("Hello world!")调用后的返回值

//int main()
//{
//	int ret=printf("Hello world!");
//	printf("\n");
//	printf("%d\n", ret);
//	return 0;
//}
//
//int main()
//{
//	int ret = printf("Hello world!");
//	printf("\n%d\n", ret);
//	return 0;
//}
//
//int main()
//{
//	printf("\n%d\n", printf("Hello world!"));
//	return 0;
//}
//
//int main()
//{
//	printf("%d", printf("%d", printf("%d",43)));
//	//4321
//	return 0;
//}

//10、题目描述：依次输入一个学生的学号，以及3科（C语言，数学，英语）成绩，在屏幕上输出该学生的学号，3科成绩。
//输入描述：学号及3科成绩，学号和成绩之间用英文分号隔开，成绩之间用英文逗号隔开。
//输出描述：学号，3科成绩，输出格式详见输出样例。
//示例：输入  17140216；80.845，90.55，100.00
//输出 The each subject score of No.17140216 is 80.85, 90.55, 100.00
//int main()
//{
//	int num = 0;
//	float c_score = 0.0;
//	float math_score = 0.0;
//	float eng_score = 0.0;
//	scanf("%d;%f,%f,%f", &num, &c_score, &math_score, &eng_score);
//	printf("The each subject score of  No.%d is %.2f,%.2f,%.2f.\n", num, c_score, math_score, eng_score);
//	return 0;
//}

//11、题目描述：从键盘任意输入一个字符，编程判断是否是字母（包括大小写）。
//输入描述：多组输入，每行输入包括一个字符。
//输出描述：针对每行输入，输出该字符是字母（YES）或不是（NO).。
//示例：输入H  9    输出YES   NO

//int main()
//{
//	int ch = 0;
//	while ((ch = getchar()) != EOF)
//	{
//		//判断字母
//		if ((ch >= 'A'&&ch <= 'Z') || (ch >= 'a'&&ch <= 'z'))
//		{
//			printf("YES\n");
//		}
//		else
//		{
//			printf("NO\n");
//		}
//		//清理掉\n
//		getchar();
//		
//	}
//	return 0;
//}
#include <ctype.h>
//int main()
//{
//	int ch = 0;
//	while ((ch = getchar()) != EOF)
//	{
//		//判断字母
//		//if ((ch >= 'A'&&ch <= 'Z') || (ch >= 'a'&&ch <= 'z'))
//		if (isalpha(ch))
//		{
//			printf("YES\n");
//		}
//		else
//		{
//			printf("NO\n");
//		}
//		//清理掉\n
//		getchar();
//
//	}
//	return 0;
//}

//12、题目描述：输入一个字符，用它构造一个三角形金字塔。
//输入描述：输入只有一行，一个字符。
//输出描述：该字符构成的三角形金字塔。
//示例：输入1
//输出
//       1
//      1 1
//    1  1  1
//  1  1   1   1
//1  1  1   1   1

int main()
{
	char ch = 0;
	scanf("%c", &ch);
	int i = 0;
	for (i = 0; i < 5; i++)
	{
		//空格
		int j = 0;
		for (j = 0; j < 5 - i - 1; j++)
		{
			printf(" ");

		}
		//数字
		for (j = 0; j <= i; j++)
		{
			printf("%c ", ch);
		}
		printf("\n");
	}
	return 0;
}
