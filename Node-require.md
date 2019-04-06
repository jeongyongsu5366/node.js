# Node.js two

```javascript
# main.js

const circle = require('./circle.js');
console.log(`지름이 4인 원의 면적: ${circle.area(4)}`);
console.log(`지름이 4인 원의 둘레: ${circle.circumference(4)}`);

```



```javascript
# circle.js

const {PI} = Math;
exports.area = (r) => PI * r * r;
exports.circumference = (r) => 2 * PI * r; 
```

인터넷 회사가있다.

여기에는

Java, Javascript, C , Swift, Python 이라는 도구들이있다.

그리고 현재 나는 저 회사의 도구가 필요한 상태이다. 그래서 나는 저 회사와 우선은 계약을 체결했다.

이 계약을 node.js로 표현하자면 require라고 할 수 있다.

```javascript
# net.js

const {PI} = Math;
exports.java = (r) => PI * r * r;
exports.python = (r) => 2 * PI * r;
Swift = (r) => r * r * PI;
C = (r) => r * PI;
```



근데 net이라는 회사에서는 자바랑 파이썬만 준다고 허락해놓았다. 이것이 바로 exports 예약어로 사용할 수 있다.

위의 코드에서보면, java 랑 python만 exports가 붙어있다. 다시 말해서, 나는 비록 net이라는 회사랑 계약을 체결함에도 불구하고, net이라는 회사가 python, java 만 허락을 해놓았기 때문에 다른 것들은 사용할 수 없다.

```javascript
# su.js

const Su = require('./net.js')
console.log(`자바를 사용하자: ${net.java}`);
console.log(`파이썬을 사용하자: ${new.python}`);
```



자 이러한 개념에 기반을 두었을때드는 의문점: 그럼 다른 사람의 API를 사용할 때 내가 안의 코드를 일일이 다보고 하나하나 export를 해야하는가, 만일 그렇다면 엄청나게 귀찮을 뿐만아니라 애써 만든 코드를 다른 사람에게 공유해야할 문제가 생길 수 있다. 



그래서 이러한 문제를 해결하기 위해 npm이라는 기술이 나왔고, API 공유자는 위의 java 나 python 등 이름과 기능만을 알려주면된다.







