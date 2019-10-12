---
id: 587d7fae367417b2b2512be4
title: Access the JSON Data from an API
challengeType: 6
forumTopicId: 301499
localeTitle: Доступ к данным JSON из API
---

## Description
<section id='description'>
В предыдущей задаче вы видели, как получить данные JSON от FreeCodeCamp Cat Photo API. Теперь вы более подробно рассмотрите возвращенные данные, чтобы лучше понять формат JSON. Вспомните некоторые обозначения в JavaScript: <blockquote> [] -&gt; Квадратные скобки обозначают массив <br> {} -&gt; Кудрявые скобки обозначают объект <br> &quot;&quot; -&gt; Двойные кавычки обозначают строку. Они также используются для ключевых имен в JSON </blockquote> Понимание структуры данных, возвращаемых API, важно, поскольку оно влияет на то, как вы извлекаете нужные значения. Справа нажмите кнопку «Получить сообщение», чтобы загрузить JavaScript-код FreeCodeCamp Cat Photo API JSON в HTML. Первый и последний символы, которые вы видите в данных JSON, являются квадратные скобки <code>[ ]</code> , которые обозначают что возвращаемые данные содержатся в массиве. Второй символ в данных JSON - кудрявые <code>{ }</code> скобки, в которые заключены объекты. Посмотрев внимательно, вы увидите, что в массиве три отдельных объекта. Данные JSON представляют собой массив состоящий из трех объектов, каждый из которых содержит информацию о фотографии кота. Вы узнали ранее, что объекты содержат пары <code>(key, value)</code>, разделенные запятыми. Например, в примере «Кошка» первый объект имеет <code>&quot;id&quot;:0</code> где «id» - это ключ, а 0 - его соответствующее значение. Аналогично, есть ключи для «imageLink», «altText» и «codeNames». У каждого объекта фотокамеры есть такие же клавиши, но с разными значениями. Еще одна интересная пара <code>(key, value)</code> в первом объекте - <code>&quot;codeNames&quot;:[&quot;Juggernaut&quot;,&quot;Mrs. Wallace&quot;,&quot;ButterCup&quot;]</code> . Здесь «codeNames» - это ключ, а его значением является массив из трех строк. Возможно иметь массивы объектов, а также вложенные объекты, то есть ключ, значением которого является другой ключ с массивом в качестве значения. Вспомните как извлечь данные из массивов и объектов. Массивы используют скобку для доступа к элементу на определенном индексе. Для доступа к значению данного свойства объекты используют либо скобку, либо точечную нотацию. Вот пример, который отображает «altText» первой фотографии кота - обратите внимание, что проанализированные данные JSON в редакторе сохраняются в переменной <code>json</code> : <blockquote> console.log (JSON [0] .altText); <br> // "A white cat wearing a green helmet shaped melon on its head." </blockquote>
</section>

## Instructions
<section id='instructions'>
Для кошки с «id» из 2, отобразите на консоли второе значение в массиве <code>codeNames</code> . Чтобы получить доступ к значению, вы можете использовать скобки или точечную нотацию на объекте (который сохраняется в переменной <code>json</code> ).
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should use bracket and dot notation to access the proper code name, and print "Loki" to the console.
    testString: assert(code.match(/(?:json\[2\]\.codeNames\[1\]|json\[2\]\[('|")codeNames\1\]\[1\])/g));

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<script>
  document.addEventListener('DOMContentLoaded',function(){
    document.getElementById('getMessage').onclick=function(){
      req=new XMLHttpRequest();
      req.open("GET",'/json/cats.json',true);
      req.send();
      req.onload=function(){
        json=JSON.parse(req.responseText);
        document.getElementsByClassName('message')[0].innerHTML=JSON.stringify(json);
        // Add your code below this line


        // Add your code above this line
      };
    };
  });
</script>
<style>
  body {
    text-align: center;
    font-family: "Helvetica", sans-serif;
  }
  h1 {
    font-size: 2em;
    font-weight: bold;
  }
  .box {
    border-radius: 5px;
    background-color: #eee;
    padding: 20px 5px;
  }
  button {
    color: white;
    background-color: #4791d0;
    border-radius: 5px;
    border: 1px solid #4791d0;
    padding: 5px 10px 8px 10px;
  }
  button:hover {
    background-color: #0F5897;
    border: 1px solid #0F5897;
  }
</style>
<h1>Cat Photo Finder</h1>
<p class="message">
  The message will go here
</p>
<p>
  <button id="getMessage">
    Get Message
  </button>
</p>

```

</div>

</section>

## Solution
<section id='solution'>

```html
// solution required
```

</section>
