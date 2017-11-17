<template>
<div class="resume">
  <div class="leftCol m_box">
    <div class="shadow"></div>
    <div class="title">

      <h2>{{person.name.first}} {{person.name.middle}}  
        {{person.name.last}}</h2>
      <div>{{person.position}}</div>

    </div>

    <div class="heading" id="myselfpic">
    </div>
    <div class="section-headline">
      {{ lang.headings.contact }}
    </div>
    <!-- <div class="item">
      <div class="icon">
        <i class="material-icons">account_circle</i>
      </div>
      <div class="text">
        <ul>
          <li> Born in {{person.birth.year}} in {{person.birth.location}}</li>
        </ul>
      </div>
    </div>
 -->
  <a href="danielkapper.com" target="_blank">
      <div class="item">
        <div class="icon">
          <i class="material-icons">language</i>
        </div>
        <div class="text">
          <span>{{person.contact.website}}</span>
        </div>
      </div>
    </a>

    <a :href="'mailto:'+person.contact.email">
      <div class="item">
        <div class="icon">
          <i class="material-icons">email</i>
        </div>
        <div class="text">
          {{person.contact.email}}
        </div>
      </div>
    </a>

    

    <a :href="'https://github.com/'+person.contact.github" target="_blank">
      <div class="item">
        <div class="icon">
          <i class="fa fa-github"></i>
        </div>
        <div class="text">
          <!-- <span>@{{person.contact.github}}</span> -->
          <span>github.com/{{person.contact.github}}</span>
        </div>
      </div>
    </a>

    <a :href="'tel:'+person.contact.phone">
      <div class="item">
        <div class="icon">
          <i class="material-icons">phone</i>
        </div>
        <div class="text">
          {{person.contact.phone}}
        </div>
      </div>
    </a>

    <div class="item">
      <div class="icon">
        <i class="material-icons">location_city</i>
      </div>
      <div class="text">
        <ul>
          <li>{{person.contact.street}}</li>
          <li>{{person.contact.city}}</li>
        </ul>
      </div>
    </div>

   <!--  <a :href="'mailto:'+person.contact.email">
      <div class="item">
        <div class="icon">
          <i class="material-icons">email</i>
        </div>
        <div class="text">
          {{person.contact.email}}
        </div>
      </div>
    </a> -->

    <!-- <a :href="person.contact.website" target="_blank">
      <div class="item">
        <div class="icon">
          <i class="material-icons">language</i>
        </div>
        <div class="text">
          <span>{{person.contact.website}}</span>
        </div>
      </div>
    </a> -->

    <div class="item last">
      <div class="section-headline">
        {{ lang.headings.skills }}
      </div>
      <div class="skill" v-for="skill in person.skills">
        <div class="right">
          <span>{{skill.name}}&nbsp;</span>
          <div class="progress">
            <div class="determinate" :style="'width: '+skill.level+'%;'">
              <!-- <i class="fa fa-circle"></i> -->
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="rightCol">
    <!-- <div class="title">
      <h2>{{person.name.first}} {{person.name.middle}} {{person.name.last}}</h2>
      <div>{{person.position}}</div>
    </div> -->
    <div class="section-headline">Professional Profile</div>
      <div class="block">
          <!-- <div class="info"> -->
             <p>A passionate and self-motivated learner that is dedicated to continuously 
               expanding my skill set and experience as a Web Developer. Skilled and detail 
               oriented coder with the ability to effectively communicate ideas, problems, 
               and solutions individually or in collaboration with a team. Strategic thinker 
               who is dedicated to continuous learning.</p>
          <!-- </div> -->
      </div>

    <div class="section-headline">Key Projects</div>
    <div class="block">
      <!-- <div class="block-helper"></div> -->
      <!-- <div class="headline">{{project.name}}</div> -->
      <p class="info">
        <!-- {{project.one}} <br>
        {{project.two}} <br>
        {{project.three}} <br>
        {{project.fore}} <br>
        {{project.five}} -->
        <ul class="a">
          <li>Built a website that contains an algorithm written in JavaScript. 
            The algorithm takes in a ransom note string and another magazines 
            string to determine if the magazine contains all the letters from the note. </li>
          <li>
            Designed a dynamic, browser compatible dice game using HTML and CSS
            which integrated multiplayer functionality by manipulating the DOM with
            JavaScript and jQuery.
          </li>
        </ul>
      </p>
    </div>

    <div class="section-headline">Professional Experience</div>

    <div class="block">
      <div class="headline">Titan House - <i>Consultant</i><span class="subheadline moveOut" style="float:right">Washington, DC</span>
        <div class="subheadline">November 2017 to Present</div>
        
        <p class="info">
          <ul class="a">
            <li>Thoroughly research private equality firms portfolio companies.</li>
            <li>
              Build detailed profiles of chief executive officers working companies. 
            </li>
            <li>
              Effectively manage my own productivity and produced quality.
            </li>
            <!--
            <li class="b">
              Communicated daily updates to team members in scrum meetings.
            </li> -->
          </ul>
          
        </p>
      </div>

     

        <div class="headline moveUp">Winco Windows, Inc. - <i>Manager</i><span class="subheadline" style="float:right">St. Louis, MO</span>
        <div class="subheadline">May 2015 to August 2017</div>
        
        <p class="info">
          <ul class="a">
            <li>Managed a team of five employees responsible for meeting daily and weekly deadlines by building a solid and helpful team environment.</li>
            <li>
              Trained and evaluated employee performance.
            </li>
            <li>
              Maintained inventory records and placed orders for new materials.
            </li>
          </ul>
          
        </p>
      </div>

         <div class="headline moveUp">MedModo App - <i>Co-founder</i> <span class="subheadline" style="float:right">St. Louis, MO</span>
        <div class="subheadline">January 2017 to June 2017</div>
        
        <p class="info">
          <ul class="a">
            <li>Designed a customer development program that measured how much value the app created for users.</li>
            <li>
              Acquired evidence to assist with deciding whether to pivot or proceed.
            </li>
            <li>
              Functioned as an enthusiastic member of the team in a fast-paced environment.
            </li>
            <li class="b">
              Communicated daily updates to team members in scrum meetings.
            </li>
          </ul>
        </p>
      
      </div>
  </div>

    <div class="section-headline">{{ lang.headings.education }}</div>
    <div class="block" v-for="education in person.education">
      <div class="block-helper"></div>
      <div class="headline">Missouri State University - <i>Computer Science</i></div>
      <div class="subheadline">
        2008 - 2011
      </div>
      <p class="info">
        {{education.description}}
      </p>
    </div>
  </div>

  <div style="clear:both;"></div>
</div>
</template>

<script>
import Vue from 'vue';
import { getVueOptions } from './resumes';

let name = 'material-dark';
export default Vue.component(name, getVueOptions(name));
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
.resume {
  font-family:'Roboto' !important;
  background:#cccccc;
}
.moveOut {
  margin-right: -15px !important; 
}
.moveUp {
  margin-top: 12px; 
}
a {
  cursor:pointer;
}
.a {
  list-style-type: square;
  margin-left: 20px; 
  /*padding: 0; */
  li {
    padding: 0; 
  }
}
.b {
  margin-bottom: 15px; 
}

.description-personal {
  margin-left:20px;
  margin-top:20px;
  padding-right:40px;
  text-align:justify;
  font-family:Roboto;
}

.title {
  right:25px;
  padding-left:20px;
  padding-top:20px;
  bottom:25px;
  h2 {
    text-transform:uppercase;
    display:block;
    font-size:1.17em;
    /*-webkit-margin-before:1em;
    -webkit-margin-after:1em;
    -webkit-margin-start:0;
    -webkit-margin-end:0;*/
    /*color:white;*/
    /*color:rgba(0,0,0,0.7);*/
    /*color: #ffffff; */
    /*padding-top:0;*/
    padding: 0; 
    margin-top:0;
    letter-spacing:5px;
    font-weight:400;
  }
  div {
    margin-top:-5px;
    margin-top:0;
    margin:0;
    padding:0;
    line-height:15pt;
    font-weight:300;
    font-weight:500;
    letter-spacing:2px;
    letter-spacing:3px;
    /*color:white;*/
    /*color:#16151c;*/
    /*color:rgba(63,61,60,0.71);*/
    /*color: red;*/
    display:block;
    font-size:0.67em;
    font-size:10pt;
   /* -webkit-margin-before:2.33em;
    -webkit-margin-start:0;
    -webkit-margin-end:0;*/
    margin-bottom: 10px; 
    padding-top:0;
    text-transform:uppercase;
    opacity:0.8;
  }
}
.section-headline {
  text-transform:uppercase;
  font-weight:500;
  letter-spacing:3px;
  font-size:10pt;
  opacity:0.8;
  margin-left:20px;
  margin-top:20px;
  margin-bottom:8px;
  color:#3f3d3c;
}
.c {
  clear:both;
}
li {
  margin:0;
  padding:0;
  /*list-style-type:none;*/
  padding-top:9px;
}

ul {
  margin:0;
  padding:0;
  /*list-style-type:none;*/
}
p {
  margin-top:0;
  margin-bottom:0;
  font-family:'Roboto', sans-serif;
  font-weight:300;
  font-size:10pt;
  line-height:17pt;
}
.m_box {
  box-shadow:0 2px 5px 0 rgba(0,0,0,0.16), 0 2px 10px 0 rgba(0,0,0,0.12);
}
.fa, .material-icons {
  display:inline-block;
  font-style:normal;
  font-weight:normal;
  line-height:1;
  -webkit-font-smoothing:antialiased;
  -moz-osx-font-smoothing:grayscale;
  font-size:26px;
}
h1, h3, h5, h6 {
  font-weight:400;
  margin:0;
}
h2 {
  font-weight:400;
  font-weight:500;
  margin:0;
  margin:0;
  font-size:22pt;
  line-height:37pt;
}
h4 {
  font-weight:400;
  margin:0;
  font-size:12pt;
  line-height:20pt;
  opacity:1;
}
.rightCol {
  width:63.5%;
  height:100%;
  float:right;
  display:flex;
  flex-direction:column;
  .block {
    width:90%;
    position:relative;
    background-color:#ffffff;
    padding:15px;
    margin-top:5px;
    margin-bottom:5px;
    display:inline-block;
    /*box-shadow:10px 0px 0px 10px rgba(0,0,0,0.16), 0 0px 0px 0 rgba(0,0,0,0.12);    */
    /*box-shadow: 0px 0px 5px 0px rgba(0,0,0,0.51);*/
    .headline {
      font-weight:400;
      display:inline-block;
      font-size:15px;
      color:rgba(0,0,0,0.870588);
      i {
        font-weight:300; 
      }
    }
    .subheadline {
      color:rgba(0,0,0,0.541176);
      display:block;
      font-size:14px;
      font-weight:300;
      margin-bottom: 8px; 
    }
    .info {
      font-size:14px;
      color:rgba(0,0,0,0.870588);
      margin-bottom:0;
      /*padding-top:10px;*/
    }
    .icon {
      width:16%;
      float:left;
      margin-left:0;
      .fa, .material-icons {
        text-align:center;
        display:block;
        font-size:30pt;
      }
    }
    .content {
      width:80%;
      position:absolute;
      height:96%;
      left:17%;
      padding-right:3%;
      text-align:left;
      display:flex;
      flex-direction:column;
      .item {
        border-bottom:1px solid #bdbdbd;
        flex:1;
        width:97%;
        display:flex;
        justify-content:center;
        flex-direction:column;
        text-align:left;
        padding-top:0;
        span {
          color:#d8ab94;
          margin-top:0;
          font-size:10pt;
          line-height:16pt;
        }
        p {
          margin-top:5px;
        }
      }
      .item:last-of-type {
        border-bottom-style:none;
        border-bottom-style:none;
      }
    }
  }
}
.leftCol {
  width:35%;
  height:100%;
  float:left;
  padding:0;
  text-align:left;
  color:#ffffff;
  color:rgba(255,255,255,0.59);
  background-color:#16151c;
  overflow:hidden;
  display:block;
  .section-headline {
    color:rgba(255,255,255,0.54);
  }
  a {
    color:rgba(255,255,255,0.59);
    text-decoration:none;
  }
  .heading {
    background-color:white;
    background-repeat:no-repeat;
    background-size:cover;
    background-position:center;
    position:relative;
    width:100%;
    height:277px;
  }
  .item {
    width:100%;
    margin-top:13px;
    float:left;
    .fa, .material-icons {
      display:inherit;
      text-align:center;
    }
    .icon {
      width:20%;
      float:left;
    }
    .text {
      float:right;
      width:69%;
      padding-right:10%;
      padding-top:0;
      display:block;
      font-size:15px;
      font-weight:300;
      li {
        padding-top:0;
        display:block;
        font-size:15px;
        font-weight:300;
      }
    }
    span {
      font-weight:300;
    }
    .skill {
      clear:both;
      width:97%;
      padding-top:4px;
      .left {
        float:left;
        width:10%;
        padding-top:3px;
        i:nth-child(2) {
          float:left;
          padding-top:4px;
        }
      }
      .right {
        float:right;
        width:93%;
        .progress {
          float:left;
          position:relative;
          height:2px;
          display:block;
          width:95%;
          background-color:rgba(255,255,255,0.19);
          border-radius:2px;
          margin:0.5rem 0 1rem;
          overflow:visible;
          margin-bottom:10px;
          .determinate {
            background-color:#78909c;
            position:absolute;
            top:0;
            bottom:0;
            .fa, .material-icons {
              font-size:13px;
              position:absolute;
              top:-4px;
              right:-2px;
              margin-left:50%;
              color:white;
            }
          }
        }
      }
    }
  }
  .item.last .text {
    border-bottom-style:none;
    padding-bottom:0;
  }
}
#myselfpic {
  padding-top: 20px; 
  /*border: 5px solid black;*/
  /*border-bottom: 80px solid black;*/
  background-image:url('../assets//profile-images/m3.png');
  color:black;
  margin-bottom: 15px; 
}
#githubIcon {
  width:25px;
  padding-left:17px;
}
</style>
