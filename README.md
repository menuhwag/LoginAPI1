# LoginAPI1 & Book
Login API 연습 예제
<h2>접근</h2>
<h3>로그인</h3>
<ol>
  <li>회원가입<br>POST /api/auth/register/local<br>
    
    {
      "username": String.min(4).max(15),
      "email": Email,
      "password": String.min(6)
    }
    
  </li><br>
  <li>로그인<br>POST /api/auth/login/local</li><br>
  
    {
      "email": Email,
      "password": String.min(6)
    }
  
  <li>
    중복확인
    <ul>
      <li>이메일<br>GET /api/auth/exists/email/:value</li><br>
      <li>아이디<br>GET /api/auth/exists/username/:value</li>
    </ul>
  </li><br>
  <li>로그아웃<br>POST /api/auth/logout</li><br>
  <li>쿠키 체크<br>GET /api/auth/check</li>
</ol>
<h3>북</h3>
<ol>
  <li>
    리스트
    <ul>
      <li>전체<br>GET /api/books</li><br>
      <li>단일<br>GET /api/books/:id</li>
    </ul>
  </li><br>
  <li>등록(게시)<br>POST /api/books</li><br>
  
    {
      "title": String,
      "authors":{
                  "name": String,
                  "email": Email
                },
      "publishedDate": Date,
      "price": Number,
      "tags": List(String)
    }
    
  <li>삭제<br>DELETE /api/books/:id</li><br>
  <li>
    수정
    <ul>
      <li>전체<br>PUT /api/books/:id</li><br>
      
        {
            "title": String,
            "authors":{
                        "name": String,
                        "email": Email
                      },
            "publishedDate": Date,
            "price": Number,
            "tags": List(String)
        }
    
  <li>일부분<br>PATCH /api/books/:id</li>
  
        {
            "title": String,
            "authors":{
                        "name": String,
                        "email": Email
                      },
            "publishedDate": Date,
            "price": Number,
            "tags": List(String)
        }
     
</ul>
  </li>
</ol>
