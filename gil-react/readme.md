# ๐ useState()
useState๋ ๊ฐ์ ๋ณ๊ฒฝํ์ฌ ๋ฐํํ **๋ชจ๋  ์ฝ๋๋ฅผ ๋ค์ ๋ ๋** ํ๋(๋ฆฌ๋ ๋) React Hook ์ด๋ค. <br>
cdn์ผ๋ก ์ฐ๋ ๊ฒ๊ณผ ๋ค๋ฅด๊ฒ ๋ธ๋์์๋ React๋ ์๋ตํด์ ์ฌ์ฉํ๋ค.
๊ทธ๋ฆฌ๊ณ  ํ์ผ ๋ด์ import ํด์ค๋ค. 

```jsx
import {useState} from "react";
const [counter, setValus] = useState(0);
```

<br>

# ๐ useEffect()
useState๋ฅผ ์ฐ๋ฉด ํ๋ฒ๋ง ์คํ ๋์ด๋ ๋๋ ์ฝ๋๋ ๋ค๊ฐ์ด ๋ฆฌ๋ ํฐ๋ฅผ ํ๊ธฐ๋๋ฌธ์ ํจ์จ์ด ์ข์ง ์๋ค.
๋ฐ๋ผ์ useEffect๋ฅผ ์ฌ์ฉํ์ฌ ํ๋ฒ๋ง ์คํ๋  ์ฝ๋๋ฅผ ์ค์ ํด์ค๋ค.

<br> 

useState์ ๊ฐ์ด import ํด์ค ๋ค ์ฒซ๋ฒ์งธ ์ธ์๋ก ํ๋ฒ๋ง ์คํ์ํฌ ํจ์๋ฅผ ์ ๋ฌํ๋ค.

```jsx
import {useEffect} from "react";
useEffect(()=> console.log('only once!'),[]);

//๋๋ฒ์งธ ์ธ์๋ก useState ๊ฐ์ ๋ฃ์ผ๋ฉด ๊ฐ์ด ๋ณ๊ฒฝ ๋ ๋ ๋ ๋๋ง ๋๋๋ก ์ฒ๋ฆฌํด ์ค์ ์๋ค.
const [value, setValue] = useState(0);
useEffect(()=> console.log('hi!'),[value]);
```

> useEffect๋ฅผ ์ฌ์ฉํ ๋ return์ ๋ฐํํ  ํจ์๋ ์ฝ๋๋ฅผ ์์ฑํ๋ฉด destroy ์ return์ด ์คํ๋๋ค.
```js
useEffect(()=>{
    //create
    console.log('hi!');

    //destroy
    return console.log('bye');
},[]);
```
