## » 202506271534
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

int int_log2(int n)
{
	int log;

	log = 0;
	while (n > 1)
	{
		n = n / 2;
		log++;
	}
	return (log);
}
```

## » 202506282359
> sevgili günlük, bugün 5 saat libft evosu dinledim.

## » 202506292113
> sorting

```
- if is_sorted  
  - return  
  
- if size == 2  
  - swap_a  
  
- if size == 3  
  - sort_three  
    - swap_a, rotate_a, reverse_a  
  
- while (size > 3)  
  - move_min_to_top  
  - push_b  
  
- sort_three  
  
- while (stack->b)  
  - push_a          (because stack b is sorted)
```

## ft_ex

```c
#include <unistd.h>

void	ft_putchr(char c)
{
	write(1, &c, 1);
}

void	ft_putstr(char *str)
{
	while (*str)
		ft_putchr(*str++);
}

void	ft_putnbr(int nb)
{
	if (nb >= 10)
	{
		ft_putnbr(nb / 10);
		ft_putnbr(nb % 10);
	}
	else
		ft_putchr(nb + '0');
}

int	ft_atoi(char *str)
{
	int	res;

	res = 0;
	while (*str)
		res = res * 10 + (*str++ - '0');

	return (res);
}

void	ft_abakus(char *str, int x)
{
	int	num = ft_atoi(str);

	ft_putnbr(x);
	ft_putstr(" x ");
	ft_putnbr(num);
	ft_putstr(" = ");
	ft_putnbr(num * x);
	ft_putstr("\n");
}

void ft_ebob(char *s1, char *s2)
{
	int x = ft_atoi(s1);
	int y = ft_atoi(s2);
	int res = 0;

	while (y != 0)
	{
		res = y;
		y = x % y;
		x = res;
	}

	ft_putnbr(x);
}

int	main(int argc, char **argv)
{
	if (argc < 2)
	{
		ft_putstr("\n");
		return (0);
	}


	// * ft_abakus
	// int i = 0;
	// while (++i < 10)
	// 	ft_abakus(argv[1], i);


	// * ft_ebob
	// ft_ebob(argv[1], argv[2]);


	ft_putstr("\n");
	return (0);
}
```

## » 202507081918
```c
unsigned char reverse_bit(unsigned char c)
{
	unsigned char res;
	char 	      bit;
	char 	      n;

	res = 0;
	n 	= -1;
	while (n++ < 8)
	{
		bit = (c >> n) & 1;		// a'yı n bit sağa kaydır , en sağdaki (0. bit'i) al
		res |= bit << (7- n);   // bit değerini n bit sola kaydır ve res 'e ekle
	}
	return (res);
}

unsigned char	swap_bits(unsigned char c)
{
	unsigned char	res;
	unsigned char	left;
	unsigned char	right;

	res   = 0;
	left  = c << 4;
	right = c >> 4;
	res |= left;
	res |= right;
	return (res);
}
```