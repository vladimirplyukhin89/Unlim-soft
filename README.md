## Тест для компании Анлим-Софт на позицию фронтенд разработчик.

### 1.

Правильно сработает второй вариант, потому что объявление с помощью функции с помощью function() {} имеет момент всплытия и регистрации функции в начале кода, что позволяет возможность использовать функцию до её объявления

### 2.

```
<template>
  <component-name
    v-for="i of limitedCount"
    :key="i"
  />
</template>

<script>
export default {
  data() {
    return {
      count: 20,
    };
  },
  computed: {
    limitedCount() {
      // Ограничиваем значение count до 10
      return this.count < 10 ? this.count : 10;
    },
  },
};
</script>
```

### 3.

```
interface IResource {
	id: number;
	count: number;
}

type TMaterials = Record<number, number>;

const resources: IResource[] = [
		{
			id: 1,
			count: 13,
		},
		{
			id: 2,
			count: 5,
		},
		{
			id: 3,
			count: 24,
		},
		{
			id: 4,
			count: 101,
		},
		{
			id: 5,
			count: 72,
		},
		{
			id: 6,
			count: 64,
		},
		{
			id: 7,
			count: 305,
		},
		{
			id: 8,
			count: 67,
		},
		{
			id: 9,
			count: 95,
		},
		{
			id: 10,
			count: 21,
		},
		{
			id: 11,
			count: 37,
		},
	];

	const getCountMaterials = (items: IResource[]): TMaterials => {
		const res: TMaterials = {};

		resources.forEach(({ id, count }) => (res[id] = count));
		return res;
	};

	const materials = getCountMaterials(resources);
	console.log(materials);
```
