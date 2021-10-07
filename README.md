# happy2
void menu()
{
	printf("******************\n");
	printf("**  1.继续游戏  **\n");
	printf("******************\n");
	printf("**  2.退出游戏  **\n");
	printf("******************\n");
	

}
game()
{
	int ret = 0;
	int guess = 0;
	ret = rand() % 100 + 1;
	while (1)
	{
		printf("请猜数字\n");
		scanf("%d", &guess);
		if (guess > ret)
			printf("猜大了\n");
		else if (guess < ret)
			printf("猜小了\n");
		else
		{
			printf("恭喜你，猜对了\n");
			break;
		}

	}
}
int main()
{
	int input = 0;
	srand((unsigned int)time(NULL));
	do
	{
		menu();
		printf("请选择:");
		scanf("%d", &input);
		switch (input)
		{
		case 1:
			game();
			break;
		case 2:
			printf("退出游戏\n");
			break;
		default:
			printf("输入错误\n");
         }
	} while (input);


	return 0;
}
