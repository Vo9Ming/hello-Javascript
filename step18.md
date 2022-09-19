# DOM으로 버튼 추가해보기

### 준비하기

아래의 내용이 포함된 html 파일을 하나 작성합니다.

#### <div id="test">메뉴판 예제< /div>

#### <script src="add_button.js"></script>

DOM을 이용해 html 객체 추가하기

##### var el = document.getElementById('test');

##### var menu = document.createElement('ul');

##### menu.id = 'menupan';

##### var item1 = document.createElement('li');

##### item1.id = 'menu1';

##### item1.innerHTML = "설렁탕";

##### var item2 = document.createElement('li');

##### item2.id = 'menu2';

##### item2.innerHTML = "추어탕";

##### menu.appendChild(item1);

##### menu.appendChild(item2);

##### el.appendChild(menu);

## input 과 button 샘플

#### <input type='text' id='input1'><button id='btn1' onclick='read()'>click</button>

#### <script>

#### var read = function() {

#### var input = document.getElementById('input1');

#### console.log(input.value);

#### };

#### </script>
