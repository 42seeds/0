## » 072720251534
> sevgili günlük, bugün ebob hesabını hatırlayamadığım için exam-02'den 50 aldım.

```c
int ebob(int a, int b)
{
	int tmp;

	while (b != 0)
	{
		tmp = b;
		b = a % b;
		a = tmp
	}
	return (a);
}
```