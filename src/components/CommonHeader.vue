<template>
  <header id="top-header">
        <div class="flex">
          <h1 class="header-logo">estra inc.</h1>
          <nav class="header-nav">
            <ul>
              <li><a href="#">home</a></li>
              <li><a href="#">about</a></li>
              <li><a href="#">service</a></li>
              <li><a href="#">works</a></li>
              <li><a href="#">price</a></li>
              <li><a href="#">contact</a></li>
            </ul>
          </nav>
        </div>
        <div id="hamburger" @click="hamburger()" :class="{'active':isClass}">
      <span></span>
      <span></span>
      <span></span>
    </div>
    <nav class="menu-content" :class="{'open':isClass}">
      <p class="menu-title">estra inc.</p>
      <ul class="menu-content_inner">
        <li>
          <a href="#">home</a>
        </li>
        <li>
          <a href="#">about</a>
        </li>
        <li>
          <a href="#">service</a>
        </li>
        <li>
          <a href="#">works</a>
        </li>
        <li>
          <a href="#">price</a>
        </li>
        <li>
          <a href="#">contact</a>
        </li>
      </ul>
    </nav>
      </header>
</template>
<script>
export default {
  data() {
    return {
      isClass: false
    };
  },
  methods: {
    hamburger() {
      this.isClass = !this.isClass; //trueとfalseを切り替え
    }
  }
}
</script>
<style scoped>
#hamburger {
  display: none; 
}
html,
body,
div,
span,
object,
iframe,
h1,
h2,
h3,
h4,
h5,
h6,
p,
blockquote,
pre,
abbr,
address,
cite,
code,
del,
dfn,
em,
img,
ins,
kbd,
q,
samp,
small,
strong,
sub,
sup,
var,
b,
i,
dl,
dt,
dd,
ol,
ul,
li,
fieldset,
form,
label,
legend,
table,
caption,
tbody,
tfoot,
thead,
tr,
th,
td,
article,
aside,
canvas,
details,
figcaption,
figure,
footer,
header,
hgroup,
menu,
nav,
section,
summary,
time,
mark,
audio,
video {
  margin: 0;
  padding: 0;
  border: 0;
  outline: 0;
  font-size: 100%;
  vertical-align: baseline;
  background: transparent;
}

body {
  line-height: 0;
}

article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
menu,
nav,
section {
  display: block;
}

nav ul {
  list-style: none;
}

blockquote,
q {
  quotes: none;
}

blockquote:before,
blockquote:after,
q:before,
q:after {
  content: "";
  content: none;
}

a {
  margin: 0;
  padding: 0;
  font-size: 100%;
  vertical-align: baseline;
  background: transparent;
}

/* change colours to suit your needs */
ins {
  background-color: #ff9;
  color: #000;
  text-decoration: none;
}

/* change colours to suit your needs */
mark {
  background-color: #ff9;
  color: #000;
  font-style: italic;
  font-weight: bold;
}

del {
  text-decoration: line-through;
}

abbr[title],
dfn[title] {
  border-bottom: 1px dotted;
  cursor: help;
}

table {
  border-collapse: collapse;
  border-spacing: 0;
}

/* change border colour to suit your needs */
hr {
  display: block;
  height: 1px;
  border: 0;
  border-top: 1px solid #cccccc;
  margin: 1em 0;
  padding: 0;
}

input,
select {
  vertical-align: middle;
}


html {
  height: 100%;
}

a {
  color: #333333;
  text-decoration: none;
}

img {
  width: 100%;
  height: 100%;
  display: block;
}

.flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}

body {
  color: #333333;
  height: 100%;
}

.mgb-15 {
  margin-bottom: 15px;
}

.common-btn {
  display: block;
  width: 130px;
  height: 40px;
  line-height: 40px;
  background: #fff;
  padding: 0 20px;
  color: #000;
  text-align: center;
}

.section-title {
  font-size: 40px;
  line-height: 1;
}

.section-title span {
  font-size: 20px;
}
.header-nav li {
  display: inline-block;
  margin-right: 35px;
  font-size: 16px;
}

.header-nav a {

  color: #fff;
}
#top-header {
  height: 70px;
  line-height: 70px;
  background: rgb(0, 0, 0);
}

@media screen and (max-width: 768px) {
  .header-nav {
    display: none;
  }
  .header-logo {
  font-size: 20px;
  font-weight: bold;
  margin-left: 35px;
  color: #fff;
  line-height: 70px;
  }
   .header-logo {
    margin: 0;
    width: 100%;
    text-align: center;
  }
   

#hamburger {
    width: 40px;
    height: 40px;
    position: absolute;
    cursor: pointer;
    z-index: 100;
    top: 15px;
    right: 20px;
    transition: 0.4s;
    display: block;
  }
  #hamburger span {
    display: block;
    width: 35px;
    height: 2px;
    background-color: #fff;
    transition: 0.8s;
  }
  #hamburger span:nth-of-type(1) {
    position: absolute;
    top: 10px;
    left: 2px;
  }
  #hamburger span:nth-of-type(2) {
    position: absolute;
    top: 20px;
    left: 2px;
  }
  #hamburger span:nth-of-type(3) {
    position: absolute;
    top: 30px;
    left: 2px;
  }
  #hamburger.active span:nth-of-type(1) {
    top: 20px;
    transform: rotate(45deg);
  }

  #hamburger.active span:nth-of-type(2) {
    opacity: 0;
  }
  #hamburger.active span:nth-of-type(3) {
    top: 20px;
    transform: rotate(-45deg);
  }
  .menu-content {
    display: block;
    width: calc(100% - 80px);
    height: 100%;
    text-align: center;
    transition: 0.2s;
    position: fixed;
    top: 0;
    left: calc(-100% - 80px);
    background: #fff;
    color: #333333;
    box-shadow: 80px 0 rgba(38, 98, 213, 0.3);
    z-index: 999;
  }
  .menu-content .menu-title {
    margin: 40px 20px;
    font-size: 2.2rem;
    color: #333333;
    text-align: left;
    font-weight: bold;
  }
  .menu-content li a {
    color: #333333;
    margin: 15px;
    padding: 5px;
    border-bottom: 0.5px solid #2662d5;
    text-decoration: none;
    display: block;
  }
  .menu-content li {
    width: 100%;
    text-align: left;
  }
  .menu-content.open {
    left: 0;
  }
}

</style>