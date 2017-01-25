**Front-End School 3**

# Day8  

## Index  

1. [아침 액티비티](#아침액티비티)
2. [탭 메뉴 구현](#탭메뉴구현)
3. [IR기법](#ir법)
4. [Transition](#transition) 
5. [box-Shadow](#box-shadow)  
6. [sprite](#sprite)  
7. [한 줄 Tip](#한줄tip)  
---

### 아침 액티비티    

   1. [Sololearn](https://www.sololearn.com/Courses/)  
   2. 그리드 시스템이란?
      - [그리드 시스템에 대해서 알아보자](http://inmoon99.tistory.com/m/34)
      - [웹 그리드 시스템](https://github.com/yamoo9/PSD2HTML-CSS/wiki/%EC%9B%B9-%EA%B7%B8%EB%A6%AC%EB%93%9C-%EC%8B%9C%EC%8A%A4%ED%85%9C)
      - [웹 그리드 시스템을 위한 가이드](http://slowalk.tistory.com/2270)   

### 탭 메뉴 구현  

```javascript
$(function(){    
  $('.tab').on('click',function(e){      
    e.preventDefault();      
    $(this).parent().parent().addClass('act').siblings().removeClass('act');
  });  
});
```

### IR기법 

접근성을 높이면서 이미지를 보여주기 위한 방법

   * 패딩 트릭: h0, p을 이미지 높이로 사용 후 넘치는 부분을 hidden  
   
   ```css
   .branding{
     background: #000 url(css/images/title.png) no-repeat;
     width: 290px;
     height: 0;
     padding-top: 195px;
     overflow: hidden;
   }
   ```  

   * 글자를 배경으로 덮는 방법  

   ```css
   .ir-bg{
     background:url(css/images/title.png) no-repeat;
     width: 290px;
     height: 195px;
     position: absolute;
     top: 0;
     left: 0;
   }
   ```  
 * 네이버 메인도 글자위에 글자이미지를 덮어 씌운 것


### Transition  

   - translform: rotate(각도 )  
   - 애니메이션과 다르게 keyframes 필요없다.  
   - hover되는 순간 실행된다.  

**CSS**
   ```css
   img{
     transform: rotate(0deg);
     /*1초 동안 360도 회전시켜줌*/
     transition: all 1s;
     border: 10px solid red;
     border-radius: 50%;
   }
   img:hover, img:focus{
     transform: rotate(360deg);
     border: 10px dashed blue;
     border-radius: 5%;
   }
   ```  
**HTML**
   ```html
   <body>
     <h1>트랜지션 효과</h1>
     <img src="images/sun.gif" alt="태양" tabindex="0">
   </body>
   ```  
   
### box-shadow  

### sprite  
 * 많은 이미지에 대한 성능이슈 해결을 위한 sprite 기법

### 한 줄 Tip  
   * [Zen Garden](http://www.csszengarden.com/) - CSS 참고  
   * 글자 강조를 위한 시맨틱 태그: 강한 강조 `<strong>`, 일반적인 강조 `<em>`  
   * [그리드 관련 사이트css-tricks](https://css-tricks.com/snippets/css/complete-guide-grid/)    
   * outline 속성: `border: 1px` 는 박스의 크기에 포함되지만 outline은 포함되지 않는다.    
   * list 생성 단축키: Ctrl + Alt + W [Windows] , Ctrl + Option + W [Mac]     

**만들고자 하는 리스트 의 텍스트 입력 후**  

패스트캠퍼스  
생산성 본부  
멀티 캠퍼스  
웹접근성 연구소  
W3C  

**단축표현 입력**  

`ul.related-list>li*>a[#]`  

**완성**  

```html  
<ul class="related-list">
  <li>패스트캠퍼스</li>
  <li>생산성 본부</li>
  <li>멀티 캠퍼스</li>
  <li>웹접근성 연구소</li>
  <li>W3C</li>
</ul>
```  

