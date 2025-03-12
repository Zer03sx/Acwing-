#include <iostream>
using namespace std;

#define MAX_SIZE 100
typedef int ElemType;	//让顺序表存储其他类型元素时，可以快速完成代码修改的过程

typedef struct {
	ElemType data[MAX_SIZE];	//
	int lenth;		//当前顺序表有多长
}SqList;

bool ListInsert(SqList& L, int pos, ElemType element) {
	// 判断pos是否合法

	if (pos < 1 || pos > L.lenth + 1)
		return false;

	// 如果存储空间满了
	if (L.lenth >= MAX_SIZE)
		return false;
	
	//把后面的元素依次后移
	for (int j = L.lenth; j >= pos; j--)
	{
		L.data[j] = L.data[j - 1];
	}
	//放入要插入的元素
	L.data[pos - 1] = element;
	L.lenth++;	//顺序表长度加1
	return true;
}

void PrintList(SqList L)
{
	for (int i = 0; i < L.lenth; i++)
		cout << L.data[i] << " ";
	cout << endl;
}

int main()
{
	SqList L;
	bool ret;	//ret用来装函数的返回值
	L.data[0] = 0;
	L.data[1] = 1;
	L.data[2] = 2;
	L.lenth = 3;

	PrintList(L);
	
	ret = ListInsert(L, 2, 60);
	if (ret){
		cout << "insert sqlist success" << endl;
	}
	else {
		cout << "insert sqlist false" << endl;
	}
	
	PrintList(L);
	
	system("pause");
	return 0;
}
