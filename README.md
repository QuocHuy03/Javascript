> # <span style="color: yellow">**JAVASCRIPT**</span>

---

- ### <span style="color: #2ed573">**Some tips**</span>

  - `.preventDefault()`: loại bỏ hành vi mặc định của brs
  - `.stopPropagation()`: loại bỏ hành vi nổi bọt
  - `.closet('class')`: ktra xem `nó hoặc cha nó` có class = 'class' hay không
  - `data-name='value'`: get ra -> dataset.name

---

- ### <span style="color: #2ed573">**Toán tử**</span>

1. `&&` là tìm kiếm điều kiện sai (false) trong dãy 6 kiểu dữ liệu false xét hết giá trị từ trái qua phải:

    - nguyên dãy true thì lấy phần tử cuối cùng và gán cho biến (dừng lại ở phần tử cuối cùng)
    - Nếu có phần tử false trong dãy thì dừng lại và gán cho biến (nếu nguyên dãy là false thì lấy phần tử đầu)
2. `||` là tìm kiếm điều kiện đúng (true) xét hết giá trị từ trái qua phải:

    - nguyên dãy false thì lấy phần tử cuối cùng và gán cho biến (dừng lại ở phần tử cuối cùng)
    - Nếu có phần tử true trong dãy thì dừng lại và gán cho biến (nếu nguyên dãy là true thì lấy phần tử đầu)
3. `??` nếu trước nó là undefined or null thì lấy cái đằng sau

---

- ### <span style="color: #2ed573">**String**</span>

  - `.split(',')`: Str -> Arr
  - `.indexOf('')`: tìm vị trí kí tự (không có trả về -1)
  - `.slice(start, end)`: cắt chuỗi
  - `.replace('', '')`: thay thế gtri chuỗi
  - `.replace(/gtri/i, '')`: không phân biệt hoa thường
  - `.replace(/gtri/g, '')`: thay thế tất cả
  - `.concat()`: nối 2 hoặc nhiều chuỗi
  - `.trim()`: loại bỏ khoảng trắng 2 đầu chuỗi
  - `.charAt()`: get kí tự by index (vượt quá index trả về chuỗi rỗng)
  - `.includes('gtri', vị trí bắt đầu tìm)`: tìm kiếm kí tự từ index (trả về `true`/`false`)

---

- ### <span style="color: #2ed573">**Array**</span>

  - `.join('')`: Arr -> Str
  - `.toString()`: chuyển về chuỗi ngăn cách bởi '`,`'
  - `.join('dấu cần ngăn cách')`
  - `.pop()`: xóa bỏ ptu cuối mảng và trả về ptu đã xóa
  - `.shift()`: xóa bỏ ptu đầu mảng và trả về ptu đã xóa
  - `.push()`: thêm 1 hoặc nhiều ptu vào cuối mảng
  - `.unshift()`: thêm 1 or nhiều ptu vào đầu mảng
  - `array[index] = 'value'`: thay thế ptu mảng
  - `.splice(index, số lượng ptu muốn xóa kể từ index, tham số từ đây trở đi là chèn)`
  - `.concat()`: nối 2 hoặc nhiều mảng
  - `.slice(start, end)`: cắt mảng
  - `.includes('gtri', vị trí bắt đầu tìm)`: tìm kiếm kí tự từ index (trả về `true`/`false`)
  - `new Set(arr)`: loại bỏ ptu trùng lặp (trả về `1 Set dạng Object`)
  - `Array.from()`: Nodelist, Html Collection, Set, Obj... -> Arr

---

- ### <span style="color: #2ed573">**Object**</span>

  - `[...obj]`: Object -> Arr
  - `.key = 'value'`: thêm key (nếu key chưa có) hoặc sửa key (nếu key đã có)
  - `['key'] = 'value'`: thêm key `vi phạm` (nếu key chưa có) hoặc sửa key `vi phạm` (nếu key đã có)
  - ['key']: lấy value của key vi phạm
  - `delete obj.key`: xóa cặp key - value
  - Object Constructor:

    ```js
    function User(firstName, lastName, avatar) {
        this.firstName = firstName;
        this.lastName= lastName;
        this.avatar= avatar;
    }
    var author = new User('Le Quoc', 'Huy', 'Admin')
    var user = new User('Member', '1', 'Avatar1')
    ```
  
  - Object Prototype
    
    \- Để thêm thuộc tính/phương thức vào hàm tạo:

    ```js
    author.key ='value' // thêm thuộc tính riêng
    User.prototype.key = 'value'
    User.prototype.nameFunction = function() {}
    ```

---

- ### <span style="color: #2ed573">**Math**</span>

  - `Math.PI()`: số pi
  - `Math.round()`: làm tròn bth
  - `Math.abs`: trị tuyệt đối
  - `Math.ceil()`: làm tròn trên
  - `Math.floor()`: làm tròn dưới
  - `Math.random()`: random số < 1
  - `Math.min()`: trả về số nhỏ nhất
  - `Math.max()`: trả về số lớn nhất
  - `.toFixed(n)`: lấy n số thập phân sau dấu phẩy

---

- ### <span style="color: #2ed573">**Loop**</span>

  - switch:

    ```js
    switch(đk) {
        case giá trị:
            // code khi case đúng
            break // bởi vì nếu case đúng sẽ chạy hết kể từ case đúng đó
        default:
            // câu lệnh thực hiện khi all case sai
            break
    }
    ```
  - Ternary Operator: Toán Tử 3 Ngôi

    ```js
    đk ? code chạy nếu đk đúng : code chạy nếu đk sai
    ```
  - for of:

    - đối với `arr`: trả ra value
    - đối với `str`: tách từng kí tự trong chuỗi
    - `Lưu Ý`: đối với `object` không dùng được
        ```js
        Object.keys(obj): // arr chứa các keys
        Object.values(obj): // arr chứa các values
        ```
  - for in:

    - đối với `str`: trả về index
    - đối với `arr`: trả về index
    - đối với `object`: trả về key
  - do while:

    ```js
    do {
        // code
    } while (đk)
    ```
    - lần 1: chạy code trong do
    - lần 2: ktra đk -> đúng chạy tiếp đến khi sai dừng, hoặc nếu đk sai thì dừng hẳn ở lần đầu
  - <span style="color: cyan">*break & continue Keyword*</span>
    + `break`: thoát vòng lặp
    + `continue`: bỏ qua lặp

---

- ### <span style="color: #2ed573">**Array II**</span>

  - forEach:

    ```js
    .forEach(function(cur, index) {
        // duyệt qua mảng (no return)
    })
    ```
  - every:

    ```js
    .every(function(cur, index) {
        // return boolean: true nếu all ptu thảo mãn đk, ngược lại 1 ptu không thỏa mãn đk thì false
    })
    ```
  - some:

    ```js
    .some(function(cur, index) {
        // return boolean: true nếu 1 ptu thảo mãn đk, ngược lại all ptu không thỏa mãn đk thì false
    })
    ```
  - find:

    ```js
    .find(function(cur, index) {
        // tìm ptu đầu tiên thõa mãn đk
        // nếu có thì gán ngược lại và return về gtri đó
        // nếu không có thì return về undefined
    })
    ```
  - filter:

    ```js
    .filter(function(cur, index) {
        // tìm tất cả ptu thỏa mãn đk
        // nếu có thì gán ngược lại và return về 1 mảng
        // nếu ko có thì return về []
    })
    ```
  - map:

    ```js
    .map(function(cur, index, origin) {
        // duyệt qua mảng và return về mảng mới phụ thuộc vào gtri func bên trong return
    })
    ```
  - reduce:

    ```js
    .map(function(result, cur, index, origin) {
        // duyệt qua mảng
        // khi không có giá trị khởi tạo: lấy ptu đầu tiên của mảng, cur là ptu thứ 2 mảng
    }, initialValue)
    ```

---

- ### <span style="color: #2ed573">**HTML DOM**</span>

  - Elements
    - `document.getElementById('id')`: chỉ trả về 1, `trực tiếp`
    - `document.querySelector('css selector')`: nếu nhiều chỉ trả về 1 ptu đầu tiên, `trực tiếp`
    - `document.getElementsByClassName('class')`: trả về 1 HTML Collection
    - `document.getElementsByTagName('tag')`: trả về 1 HTML Collection
    - `document.querySelectorAll('css selector')`: trả về tất cả, dạng Nodelist
      + `document.forms`: trả về HTML Collection tất cả thẻ form
      + `document.forms.id`: trả về thẻ form theo id chỉ định
      + `document.forms['id']`: trả về thẻ form theo id `vi phạm` chỉ định
      + `document.anchors`: trả về tất cả thẻ a có attribute là `name=''`
      + `document.links`: trả về tất cả thẻ a
    ---
    - seter (element, attribute, text)
      + `.innerHTML = ''`: (ghi đè tất cả con bên trong)
      + `.outerHTML = ''`: (ghi đè tất cả con kể cả nó)
    - geter
      + `.innerHTML`: trả về 1 chuỗi (bao gồm khoảng cách thực sự)
      + `.outerHTML`: trả về 1 chuỗi (bao gồm cả chính nó)

  - Attributes
    - seter
      - `.setAttribute('attribute_name', 'value')`
      - `.attribute_name (class -> className) = 'value'` (attribute hợp lệ)
    - geter
      - `.getAttribute('attribute_name')`
      - `.attribute_name (attribute hợp lệ)`

  - Texts
    - geter
      - `.innerText`: lấy ra phần text nhìn thấy trên brs
      - `.textContent`: lấy ra khoảng cách thực sự bên trong html
    - seter
      - `.innerText` or `.textContent` = 'value'

---

- ### <span style="color: #2ed573">**CSS DOM**</span>

  - seter (inline css)
    - `.style.css_property = 'value'`
    - TH nhiều property:

      ```js
      Object.assign(.style, { 
        // write CSS
       }) 
      ```
  - geter (inline css)
    - `.style.css_property`

  - classList property
    - seter
      - `.classList.add('class_name1', 'class_name2',...)`: thêm class
      - `.classList.remove('class_name')`: xóa class
      - `.classList.contains('class_name')`: ktra class return boolean
      - `.classList.toggle('class_name')`: class chưa có thì thêm, có rồi thì xóa
    - geter
      - `.classList.length`: lấy độ dài class
      - `.classList[]`: lấy ra class chi tiết (không có thì undefined)
      - `.classList.value` để lấy ra chuỗi class

---

- ### <span style="color: #2ed573">**JSON (JavaScript Object Notation)**</span>
- Là một định dạng dữ liệu (chuỗi)

  - `JSON.stringify()`: js -> json
  - `JSON.parse()`: json -> js

---

- ### <span style="color: #2ed573">**Promise**</span>
- Async: setTimeout, setInterval, fetch, XMLHttpRequest, file reading, request animation frame,...

```js
var promise = new Promise(
    function(resolve, reject) {
        // chưa trả thành công hay thất bại: trạng thái pending
        // thành công -> resolve(): trạng thái fulfilled
        // thất bại -> reject(): trạng thái rejected
    }
)

promise
    .then(function() {
      return 1
        // thành công lọt vào đây
        // then trên return then dưới nhận lấy
        // chú ý: nếu giá trị return ko phải Promise: chạy tuần tự như bth
        // nếu giá trị trả về 1 new Promise thì sẽ giải quyết xong Promise mới chạy tiếp
    })
    .then(function(data) {
        console.log(data)
        return 2
    })
    .then(function(data) {
        console.log(data)
    })
    .catch(function() {
        // thất bại lọt vào đây
    })
    .finally(function() {
        // 1 trong 2 thành công hay thất bại vẫn lọt vào đây
    })

// khi giữa các then có 1 then bị reject (lỗi) thì sẽ bị đứng
// dùng Promise.resolve & reject để tạo 1 promise đơn
// dùng Promise.all([promise1, promise2]) để cùng nhận 1 kq và làm việc gì đó chung
```

---

- ### <span style="color: #2ed573">**fetch**</span>
- API (Application Programing Interface)
- backend -> API -> Fetch -> JSON/XML -> JSON parse -> JS type -> hiển thị ra brs

  - ex:

    ```js
    var postApi = 'https://jsonplaceholder.typicode.com/posts'
    fetch(postApi)
      .then(function(response) {
        return response.json()
      })
      .then(function(posts) {
        var htmls = posts.map(function(post) {
          return `<li>
          <h2>${post.title}</h2>
          <p>${post.body}</p>
          </li>`
      })
      var html = htmls.join('')
      document.querySelector('#post-block').innerHTML = html
    })
    ```

---

- ### <span style="color: #2ed573">**ES6**</span>

  - arrow function
    - cú pháp: `() => {}`
    - nếu chỉ có 1 tham/đối số thì bỏ `()`
    - `() => value`: return value
    - `({key: value,...})`: return nhanh đối với object
    - `lưu ý`: khi sử dụng với `this`, `constructor function` không dùng được

  - classes
    - cú pháp:

      ```js
      class Name {
        constructor() {
          // constructor func
        }
        method_func() {
          // phương thức
        }
      }
      ```

  - enhanced objects literals
    - method:
    ```js
    getFunc: function () {}
    getFunc() {}
    ```

  - destructuring: phân rã (arr, obj)
    - lấy ra từng ptu trong mảng:
      ```js
      var arr = [1, 2, 3]
      var [a, b, c] = arr
      console.log(a, b, c)
      // nếu không cần lấy gtri nào đó -> để trống [a, , c]
      ```
    - rest:
      ```js
      // in array
      var [a, b, ...rest]
      console.log(rest) // lấy ra những ptu còn lại

      // in object
      var obj = {
        name: 'zh',
        age: 17,
        birth: {
          age: 18
        }
      }
      var { name, age } = obj
      rest: var {a, b, ...rest}
      console.log(rest) // lấy ra những ptu còn lại
      var { name, age: parentAge, birth: { age } }
      // nếu sử dụng để lấy ra key chưa có thì có thể set default value = '' { name, age: parentAge, birth: { age }, address = 'Hue' }

      // in function
      function(...rest) {
        // rest được truyền dưới dạng tham số trong func thì return về 1 arr
      }
      ```

  - spread
    - `...` : bỏ ngoặc của arr, obj

  - tagged template literals

    ```js
    function highlight([first, ...strings], ...values) {
      return values.reduce(
        (acc, cur) => [...acc, `<span>${cur}</span>`, strings.shift()],
        [first]
      ).join('')
    }
    var brand = 'F8'
    var course = 'JS'
    html = highlight`Học lập trình ${course} tại ${brand}!`
    ```

  - modules
    - thêm `type='module'` vào thẻ script
    - import name_mdl from ''
    - `export default name_mdl` (mỗi file chỉ export default được 1 lần)
    - `export const name_mdl = ''`: export thường
    - `import {} from ''`: dùng với destructuring để chọn ra những export thường cần import
    - `import * as file_name from ''`: import tất cả những export thường

  - optional chaining (?.)
    - `?.key`: khi nghi ngờ key của 1 obj có tồn tại hay không
    - `arr?.[index]`: khi nghi ngờ value của 1 arr có tồn tại hay không
    - `func?.()`: khi nghi ngờ 1 function tồn tại hay không 

---

- ### <span style="color: #2ed573">**IIFE**</span>
- là hàm gọi ngay lập tức

  - khi sử dụng thêm '`;`' đằng trước
  - là hàm '`private`'
    ```js
    ;(function() {
      // code
    })()

    ;(()=>{
      // code
    })()

    dấu toán tử()=>{
      // code
    }()
    ```
---

- ### <span style="color: #2ed573">**Scope**</span>

  - Global: var, let, const -> toàn cục có thể truy cập được
  - Code Block: let, const -> chỉ trong khối mới có thể truy cập được
  - Local: var, function
  - Mỗi lần call func thì sẽ tạo ra một phạm vi mới (ô nhớ mới)

---

- ### <span style="color: #2ed573">**Closure**</span>
- là hàm có thể ghi nhớ nơi nó được tạo ra và truy cập được biến ngoài phạm vi nó (bản chất func)

---

- ### <span style="color: #2ed573">**Hoisting**</span>

  - var: đưa khai báo lên đầu gán gtri mặc định = undefined
  - `function declaration`: đưa nguyên cụm func lên đầu -> dùng hàm trước khi khai báo vẫn đc
  - `let, const`: đưa khai báo lên đầu nhưng không gán gtri mặc định -> move to 'temporal dead zone'

---

- ### <span style="color: #2ed573">**Strict Mode**</span>

  - thêm vào đầu file js: '`use strict`' để sử dụng
  - thêm vào `đầu bên trong thẻ script`
  - thêm vào `đầu hàm`
  - thêm vào `hàm`

  - báo lỗi khi sửa object có `writable: false`
      ```js
      // 1
      Object.freeze({key: value})
      // 2
      Object.defineProperty(student, 'fullName', {
        value: 'Duy'
      })
      ```
  - báo lỗi khi xóa object
  - báo lỗi khi hàm có tham số trùng tên
  - func chỉ sử dụng bên trong block code
  - báo lỗi khi tên biến = từ khóa ngôn ngữ

---

- ### <span style="color: #2ed573">**Value Type & Reference Type**</span>

- Value Type: kiểu tham trị -> kiểu dữ liệu nguyên thủy (gtri được sao chép lưu trong từng ô nhớ khác nhau)
- Reference Type: kiểu tham chiếu -> obj, arr, function (gtri sẽ lưu vào địa chỉ và gtri sau sẽ tham chiếu (trỏ) tới địa chỉ đó)

---

- ### <span style="color: #2ed573">**this**</span>

- trong function -> trả về window (undefined nếu sử dụng 'use strict')
- tham chiếu đến đối tượng gọi nó
- đối với arrow function, this sẽ không có context và nhảy ra bên ngoài lấy this

---

- ### <span style="color: #2ed573">**bind()**</span>

  - ràng buộc đối tượng `bind(obj)`: tức là `this bị ràng buộc` với obj
  - tham số thứ `2 trở đi` thì sẽ là `tham/đối số truyền vào`
  - là `hàm mới với this mới`, `không sửa this` của đối tượng ban đầu

---

- ### <span style="color: #2ed573">**call()**</span>

  - sử dụng để `gọi hàm và bind this`
  - `.call(obj)`: strict mode vẫn dùng được
  - tham số thứ `2 trở đi` thì sẽ là `tham/đối số truyền vào`
  - tính `kế thừa` trong oop
  - tính `mượn hàm`

---

- ### <span style="color: #2ed573">**apply()**</span>

  - sử dụng để gọi hàm và bind this tuy nhiên tham số thứ 2 là một mảng
