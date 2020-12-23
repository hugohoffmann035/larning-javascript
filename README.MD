# **Dates in javascript**

### **Date toString**
#### returns a string representation of the Date in the format specified in ECMA-262
[Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toString)

### Example
```
const current = new Date("2020-12-23");
const date = current.toString();
console.log(date)
// result: Tue Dec 22 2020 21:00:00 GMT-0300 (Horário Padrão de Brasília)
```

### **Date toLocaleString**
#### The toLocaleString() method returns a string with a language sensitive representation of this date.
[Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleString)
### **Locale**
- Example: pt-BR
- 
### **Options**

#### **weekday**
- **long** - terça-feira
- **short** - ter
- **narrow** - T
- 
#### **day**
- **numeric** - 22
- **2-digit** - 01

#### **month**
- **numeric** - 12
- **2-digit** - 12
- **long** - Dezembro
- **short** - Dez
- **narrow** - D

#### **year**
- **numeric** - 2020
- **2-digit** - 20

### Example
```
const current = new Date("2020-12-23");
const options = {
    hour: '2-digit',
    minute: '2-digit',
    second: '2-digit',
    weekday: 'long',
    month: 'numeric',
    year: 'numeric',
    day: 'numeric',
}
const date = current.toLocaleString('pt-BR', options)
console.log(date)
// result: terça-feira, 22/12/2020 21:00:00
```

### **Date valueOf**
#### The valueOf() method returns the primitive value of a Date object as a number data type, the number of milliseconds since midnight 01 January, 1970 UTC.
[Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toString)

### Example
```
const current = new Date("2020-12-23");
const date = current.valueOf()
console.log(date)
// result: 1608681600000
```

### **Date getters**

### Example
```
const current = new Date("2020-12-23");
const day = current.getDate();
const month = current.getMonth() + 1;
const year = current.getFullYear();

const formatDay = day.toString().padStart(2, '0')
const formatMonth = month.toString().padStart(2, '0')

console.log(`${formatDay}/${formatMonth}/${year}`)
// result: 22/12/2020
```


### **Date setters**

### Example
```
const date = new Date();
date.setFullYear(2020);
date.setMonth(12 - 1);
date.setDate(23);
console.log(date.toLocaleString())
// result: 23/12/2020 09:48:43
```