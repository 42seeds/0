## » 202507271534
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

## » 202507282359
> sevgili günlük, bugün 5 saat libft evosu dinledim.

## » 202507292113
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