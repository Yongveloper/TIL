# JavaScript Array Methods <code>slice()</code> vs <code>splice()</code>

## π‘ <code>slice()</code> λ°°μ΄ λ©μλ

> <code>slice()</code> λ©μλλ <strong>λ°°μ΄μ λ³΅μ¬λ³Έμ λ§λ€κ±°λ λ°°μ΄μ μΌλΆλ₯Ό λ°ννλ λ° μ¬μ©ν  μ μλ€.</strong>

> <code>slice()</code> λ©μλλ μλ λ°°μ΄μ λ³κ²½νμ§ μκ³  λμ  <strong>μμ λ³΅μ¬λ³Έ</strong>μ μμ± νλ€λ μ μ μ μν΄μΌ νλ€ .

κΈ°λ³Έ κ΅¬λ¬Έμ λ€μκ³Ό κ°λ€.

```javascript
slice(optional start parameter, optional end parameter)
```

μ΄ μμμμλ κ³ΌμΌ λͺ©λ‘μ λ§λ€μλ€.

```javascript
const fruits = ['apple', 'banana', 'mango', 'melon'];
```

### <code>slice()</code> λ©μλλ₯Ό λ§€κ°λ³μ μμ΄ μ¬μ©νλ λ°©λ² β

<code>slice()</code> λ©μλλ₯Ό νμ©ν΄ ν΄λΉ λ°°μ΄μ μμ λ³΅μ¬λ³Έμ λ§λ€ μ μλ€.

```javascript
console.log(fruits.slice()); // ['apple', 'banana', 'mango', 'melon']
```

## start λ§€κ°λ³μλ₯Ό μ¬μ©ν΄μ <code>slice()</code> λ©μλλ₯Ό μ¬μ©νλ λ°©λ² β

μ΅μμΌλ‘ μ€ μ μλ start λ§€κ°λ³μλ₯Ό μ¬μ©ν΄μ λ°°μ΄μμ μμλ₯Ό μ ννκΈ° μν μμ μμΉλ₯Ό μ€μ ν  μ μλ€.

μ΄ μμμμλ index 2λ₯Ό μμ μ°μΉλ‘ μ€μ ν΄μ index 2λΆν° λ§μ§λ§ indexκΉμ§ μ νν΄μ μ λ°°μ΄λ‘ λ°ννλ€.

```javascript
const newFruits = fruits.slice(2);

console.log(newFruits); // ['mango', 'melon']
```

μλ λ°°μ΄μ μμ λμ§ μλ κ²μ λ³Ό μ μλ€.

```javascript
const fruits = ['apple', 'banana', 'mango', 'melon'];

const newFruits = fruits.slice(2);

console.log('μλ κ³ΌμΌ: ', fruits); // ['apple', 'banana', 'mango', 'melon']
console.log('μλ‘μ΄ κ³ΌμΌ: ', newFruits); // ['mango', 'melon']
```

λ°°μ΄ λμμ λΆν° μ ννκ³  μΆλ€λ©΄ μμ indexλ₯Ό μ¬μ©ν  μλ μλ€.

```javascript
const newFruits = fruits.slice(-1);

console.log(newFruits); // ['melon']
```

start λ§€κ°λ³μκ° λ°°μ΄μ λ§μ§λ§ index λ³΄λ€ ν¬λ©΄ λΉ λ°°μ΄μ΄ λ°νλλ€.

```javascript
const newFruits = fruits.slice(4);

console.log(newFruits); // []
```

## start μ end λ§€κ°λ³μλ₯Ό μ¬μ©νμ¬ <code>slice()</code> λ©μλλ₯Ό μ¬μ©νλ λ°©λ² β

end μμΉκ° μ§μ λ κ²½μ° <code>slice()</code> λ©μλλ start μμΉμμ end μμΉκΉμ§ μμλ₯Ό μΆμΆνλ€.

<strong>end μμΉλ μλ‘μ΄ λ°°μ΄μ μΆμΆλ μμμ ν¬ν¨λμ§ μλλ€.</strong>

```javascript
const fruits = ['apple', 'banana', 'mango', 'melon'];

const newFruits = fruits.slice(1, 3);

console.log(newFruits); // ['banana', 'mango'];
```

## π‘ <code>splice()</code> λ°°μ΄ λ©μλ

> <code>slice()</code> λ©μλμ λ¬λ¦¬ <code>splice()</code> λ©μλλ <strong>μλ λ°°μ΄μ λ΄μ©μ λ³κ²½νλ€.</strong>

> <code>splice()</code> λ©μλλ κΈ°μ‘΄ λ°°μ΄μ μμλ₯Ό μΆκ°νκ±°λ μ κ±°νλ λ° μ¬μ©λλ©° λ°ν κ°μ <strong>λ°°μ΄μμ μ κ±°λ ν­λͺ©μ΄ λ°ν λλ€.</strong>

<code>splice()</code> λ©μλμ κΈ°λ³Έ κ΅¬λ¬Έμ λ€μκ³Ό κ°λ€.

```javascript
splice(start, optional delete count, optional items to add)
```

μ΄ μμμλ μμΌ ν­λͺ©μ λ°°μ΄μ΄ μλ€.

```javascript
const week = ['Mon', 'Tue', 'Wen', 'Thu', 'Fri'];
```

## <code>splice()</code> λ©μλ μ¬μ©ν΄μ μμλ₯Ό μΆκ°νλ λ°©λ² β

λ°°μ΄μ index 1μ λ€λ₯Έ μμΌμ μΆκ°νλ €λ©΄ λ€μκ³Ό κ°μ΄ ν  μ μλ€.

```javascript
week.splice(1, 0, 'Sat');
```

μ²« λ²μ§Έ μ«μλ μμ indexκ³ , λ λ²μ§Έ μ«μλ μ­μ  νμλ€.

μλ¬΄ ν­λͺ©λ μ­μ νμ§ μμΌλ―λ‘ μ­μ  νμλ 0μ΄λ€.

```javascript
const week = ['Mon', 'Tue', 'Wen', 'Thu', 'Fri'];

week.splice(1, 0, 'Sat');

console.log(week); // ['Mon', 'Sat', 'Tue', 'Wen', 'Thu', 'Fri'];
```

## <code>splice()</code> λ©μλλ₯Ό μ¬μ©ν΄μ μμλ₯Ό μ κ±°νλ λ°©λ² β

μ΄ μμμμλ λ°°μ΄μμ "Wen"μ μ κ±°νλ €κ³  νλ€. start λ° delete λ§€κ°λ³μλ₯Ό μ¬μ©ν΄μ μ κ±°ν  μ μλ€.

```javascript
week.splice(2, 1);
```

μ«μ 2λ μμ μμΉμ΄κ³ , μ«μ 1μ μ­μ  νμλ₯Ό λνλΈλ€. "Wen"μ index 2μ μμΉν΄ μμΌλ―λ‘ λ°°μ΄μμ μ κ±°λλ€.

```javascript
const week = ['Mon', 'Tue', 'Wen', 'Thu', 'Fri'];

week.splice(2, 1);

console.log(week); // ['Mon', 'Tue', 'Thu', 'Fri'];
```

## π κ²°λ‘ 

<code>slice()</code> μ <code>splice()</code> λ©μλλ μλ‘ λΉμ·ν΄ λ³΄μΌ μ μμ§λ§ λͺ κ°μ§ μ£Όμ μ°¨μ΄μ μ΄ μλ€.

<code>slice()</code> λ©μλλ <strong>λ°°μ΄μ λ³΅μ¬λ³Έμ λ§λ€κ±°λ λ°°μ΄μ μΌλΆλ₯Ό λ°ν νλλ° μ¬μ©ν  μ μκ³ , μλ λ°°μ΄μ λ³κ²½νμ§ μκ³  λμ , μμ λ³΅μ¬λ³Έμ μμ±νλ€.</strong>

<code>splice()</code> λ©μλλ <strong>μλ λ°°μ΄μ λ΄μ©μ λ³κ²½νκ³ , κΈ°μ‘΄ λ°°μ΄μ μμλ₯Ό μΆκ° νκ±°λ μ κ±°νλ λ° μ¬μ©λλ©° λ°ν κ°μ λ°°μ΄μμ μ κ±°λ ν­λͺ©μ΄ λλ€.</strong>

λ°°μ΄μμ μλ¬΄ κ²λ μ κ±°λμ§ μμ κ²½μ° λ°ν κ°μ λΉ λ°°μ΄μ΄λ€.
