<template>
    <div id="main">
      <header id="header">
        <div class="inner relative">
          <h1>
            <a href="javascript:void(0)" @click="scrollTop"></a>
            <!--<router-link to="/"></router-link>-->
          </h1>
          <ul id="nav">
            <li><a href="javascript:void(0)" data-target="philosophy" id="nav-philosophy" v-scroll-to="{ el: '#philosophy', offset:-70, easing: 'ease' }">{{ langRst.nav_philosophy }}</a></li>
            <li><a href="javascript:void(0)" data-target="service" id="nav-service" v-scroll-to="{ el: '#service', offset:-70, easing: 'ease' }">{{ langRst.nav_service }}</a></li>
            <li><a href="javascript:void(0)" data-target="about" id="nav-about" v-scroll-to="{ el: '#about', offset:-70, easing: 'ease' }">{{ langRst.nav_About }}</a></li>
            <li><a href="javascript:void(0)" data-target="career" id="nav-career" v-scroll-to="{ el: '#career', offset:-70, easing: 'ease' }">{{ langRst.nav_career }}</a></li>
            <li><a href="javascript:void(0)" data-target="contact" id="nav-contact" v-scroll-to="{ el: '#contact', offset:-70, easing: 'ease' }">{{ langRst.nav_contact }}</a></li>
          </ul>
          <!--<a href="javascript:void(0)" class="langBtn" @click="langChange"><span>{{ langTitle }}</span></a>-->
        </div>
      </header>
      <div class="main_top asyncImage">
        <!--<div class="gradient"></div>-->
        <div class="abs">
          <div class="inner">
            <div class="txt">
              <h2>
                <img src="https://s3.ap-northeast-2.amazonaws.com/eosnova.io.resource/images/wzd-txt-title-black.png" width="373"/>
              </h2>
              <p>
                {{ langRst.main_title01 }}
                {{ langRst.main_title02 }}
                {{ langRst.main_title03 }}
              </p>
              <!--<div class="cell">-->
                <!---->
              <!--</div>-->
            </div>
            <div class="img">
              <img src="https://s3.ap-northeast-2.amazonaws.com/eosnova.io.resource/images/wzd-main-image.png" width="680"/>
            </div>
          </div>
        </div>
      </div>
      <!-- PHILOSOPHY -->
      <div class="content" id="philosophy">
        <div class="inner">
          <h2 class="contentTit">Philosophy</h2>
          <p class="contentSub">
            {{ langRst.philosophy_sub01 }}<br/>
            {{ langRst.philosophy_sub02 }}
          </p>
          <ul>
            <li>
              <p class="img">
                <img src="../assets/wzd-icon-philosophy-01.png" style="max-width:90px;"/>
              </p>
              <h4 class="tit">{{ langRst.philosophy_tab_tit01 }}</h4>
              <div class="sub"><p>{{ langRst.philosophy_tab_sub01 }}</p></div>
            </li>
            <li>
              <p class="img">
                <img src="../assets/wzd-icon-philosophy-02.png" style="max-width:90px;"/>
              </p>
              <h4 class="tit">{{ langRst.philosophy_tab_tit02 }}</h4>
              <div class="sub">
                <p>
                  {{ langRst.philosophy_tab_sub02 }}<br/>
                  {{ langRst.philosophy_tab_sub02_2 }}
                </p>
              </div>
            </li>
            <li>
              <p class="img">
                <img src="../assets/wzd-icon-philosophy-03.png" style="max-width:90px;"/>
              </p>
              <h4 class="tit">{{ langRst.philosophy_tab_tit03 }}</h4>
              <div class="sub">
                <p>
                  {{ langRst.philosophy_tab_sub03 }}
                </p>
              </div>
            </li>
          </ul>
        </div>
      </div>
      <!-- SERVICE -->
      <div class="content" id="service">
        <div class="inner">
          <h2 class="contentTit">{{ langRst.ourServices }}</h2>
          <div class="tabNav">
            <ul id="serviceTab">
              <li class="on" @click="tabCtrl('0','a')" id="service01"><a href="javascript:void(0)">{{ langRst.novaWallet }}</a></li>
              <li @click="tabCtrl('1','b')" id="service02"><a href="javascript:void(0)">{{ langRst.themeKeyboard }}</a></li>
              <li @click="tabCtrl('2','c')" id="service03"><a href="javascript:void(0)">{{ langRst.somcloud }}</a></li>
            </ul>
          </div>
          <ul class="tabCont" id="serviceCont">
            <li class="con table on" id="nova">
              <div class="txt cell">
                <h4>NOVA <span>Wallet</span></h4>
                <p>
                  {{ langRst.novaWallet_txt01 }}<br/>
                  {{ langRst.novaWallet_txt02 }}
                </p>
                <div class="downLink">
                  <a href="https://apple.co/2NZZrUj" class="appstore" target="_blank">{{ langRst.appStore }}</a>
                  <a href="https://play.google.com/store/apps/details?id=io.eosnova.wallet.android" class="googleplay" target="_blank">{{ langRst.googlePlay }}</a>
                  <a href="http://www.eosnova.io/" class="web" target="_blank">{{ langRst.web }}</a>
                </div>
              </div>
              <div class="img cell">
                <p>
                  <img src="https://s3.ap-northeast-2.amazonaws.com/eosnova.io.resource/images/wzd-nova-wallet.png" style="width:350px;"/>
                </p>
              </div>
            </li>
            <li class="con table" id="keyboard">
              <div class="txt cell">
                <h4>ThemeKeyboard</h4>
                <p>
                  {{ langRst.keyboard_txt01 }}<br/>
                  {{ langRst.keyboard_txt02 }}
                </p>
                <div class="downLink">
                  <a href="https://play.google.com/store/apps/details?id=com.wzdworks.themekeyboard" class="googleplay" target="_blank">{{ langRst.googlePlay }}</a>
                </div>
              </div>
              <div class="img cell">
                <p>
                  <img src="https://s3.ap-northeast-2.amazonaws.com/eosnova.io.resource/images/wzd-theme-keyboard.png" style="width:350px;"/>
                </p>
              </div>
            </li>
            <li class="con table" id="somcloud">
              <div class="txt cell">
                <h4>Somcloud</h4>
                <p>
                  {{ langRst.somcloud_txt01 }}<br/>
                  {{ langRst.somcloud_txt02 }}
                </p>
                <div class="downLink">
                  <a href="https://itunes.apple.com/kr/app/gugmin-memojang-somnoteu-somnote/id515219433" class="appstore" target="_blank">{{ langRst.appStore }}</a>
                  <a href="https://play.google.com/store/apps/details?id=com.somcloud.somnote" class="googleplay" target="_blank">{{ langRst.googlePlay }}</a>
                  <a href="https://somcloud.com" class="web" target="_blank">{{ langRst.web }}</a>
                </div>
              </div>
              <div class="img cell">
                <p>
                  <img src="https://s3.ap-northeast-2.amazonaws.com/eosnova.io.resource/images/wzd-service-somcloud.png" style="width:450px;"/>
                </p>
              </div>
            </li>
          </ul>
        </div>
      </div>
      <!-- ABOUT US -->
      <div class="content" id="about">
        <div class="inner">
          <h2 class="contentTit">{{ langRst.nav_About }}</h2>
          <p class="contentSub">
            {{ langRst.about_sub }}
          </p>
          <ul class="teamList">
            <li v-for="item in teamList">
              <p class="img"><img :src="item.image" style="max-width:130px;"/></p>
              <p class="title ko" v-if="langState === '한글'">
                <span>{{item.name}}</span>
              </p>
              <p class="title en" v-else>
                <span>{{item.name}}</span>
              </p>
              <p class="work">
                <span class="w1">{{item.work}}</span>
                <span class="w2">{{item.work2}}</span>
              </p>
            </li>
          </ul>
          <div class="history">
            <ul>
              <li>
                <h4>2006</h4>
                <div>
                  <p>{{ langRst.history01_01 }} <strong>{{ langRst.history01_02 }}</strong></p>
                  <p><strong>{{ langRst.history01_03 }}</strong>{{ langRst.history01_04 }}</p>
                </div>
              </li>
              <li>
                <h4>2007</h4>
                <div>
                  <p>{{ langRst.history02_01 }} <strong>{{ langRst.history02_02 }}</strong></p>
                  <p><strong>{{ langRst.history02_03 }}</strong> {{ langRst.history02_04 }}</p>
                </div>
              </li>
              <li>
                <h4>2008</h4>
                <div>
                  <p>{{ langRst.history03_01 }}</p>
                  <p><strong>{{ langRst.history03_02 }}</strong></p>
                </div>
              </li>
              <li>
                <h4>2012</h4>
                <div>
                  <p>{{ langRst.history04_01 }} <strong>{{ langRst.history04_02 }}</strong></p>
                  <p><strong>{{ langRst.history04_03 }}</strong> {{ langRst.history04_04 }}</p>
                </div>
              </li>
              <li>
                <h4>2013</h4>
                <div>
                  <p>{{ langRst.history05_01 }}</p>
                  <p><strong>{{ langRst.history05_02 }}</strong> {{ langRst.history05_03 }}</p>
                </div>
              </li>
              <li>
                <h4>2014</h4>
                <div>
                  <p>{{ langRst.history06_01 }}</p>
                  <p><strong>{{ langRst.history06_02 }}</strong> {{ langRst.history06_03 }}</p>
                </div>
              </li>
              <li>
                <h4>2015</h4>
                <div>
                  <p>{{ langRst.history07_01 }}</p>
                  <p><strong>{{ langRst.history07_02 }}</strong> {{ langRst.history07_03 }}</p>
                </div>
              </li>
              <li>
                <h4>2018</h4>
                <div>
                  <p>{{ langRst.history08_01 }}</p>
                  <p><strong>{{ langRst.history08_02 }}</strong> {{ langRst.history08_03 }}</p>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <!-- CAREER -->
      <div class="content" id="career">
        <div class="smInner">
          <h2 class="contentTit">{{ langRst.nav_career }}</h2>
          <p class="contentSub">
            {{ langRst.career_sub01 }}
          </p>
          <div class="careerBox table">
            <div class="benefit cell">
              <ul>
                <li>
                  <h4 class="tit">
                    <span>1</span>
                    {{ langRst.benefit_tit01 }}
                  </h4>
                  <div class="txt">
                    <p>{{ langRst.benefit_sub01_01 }}</p>
                    <p>{{ langRst.benefit_sub01_02 }}</p>
                  </div>
                </li>
                <li>
                  <h4 class="tit">
                    <span>2</span>
                    {{ langRst.benefit_tit02 }}
                  </h4>
                  <div class="txt">
                    <p>{{ langRst.benefit_sub02_01 }}</p>
                    <p>{{ langRst.benefit_sub02_02 }}</p>
                  </div>
                </li>
                <li>
                  <h4 class="tit">
                    <span>3</span>
                    {{ langRst.benefit_tit03 }}
                  </h4>
                  <div class="txt">
                    {{ langRst.benefit_sub03 }}
                  </div>
                </li>
                <li>
                  <h4 class="tit">
                    <span>4</span>
                    {{ langRst.benefit_tit04 }}
                  </h4>
                  <div class="txt">
                    {{ langRst.benefit_sub04 }}
                  </div>
                </li>
                <li>
                  <h4 class="tit">
                    <span>5</span>
                    {{ langRst.benefit_tit05 }}
                  </h4>
                  <div class="txt">
                    {{ langRst.benefit_sub05 }}
                  </div>
                </li>
                <li>
                  <h4 class="tit">
                    <span>6</span>
                    {{ langRst.benefit_tit06 }}
                  </h4>
                  <div class="txt">
                    {{ langRst.benefit_sub06 }}
                  </div>
                </li>
                <li>
                  <h4 class="tit">
                    <span>7</span>
                    {{ langRst.benefit_tit07 }}
                  </h4>
                  <div class="txt">
                    {{ langRst.benefit_sub07 }}
                  </div>
                </li>
                <li>
                  <h4 class="tit">
                    <span>8</span>
                    {{ langRst.benefit_tit08 }}
                  </h4>
                  <div class="txt">
                    {{ langRst.benefit_sub08 }}
                  </div>
                </li>
              </ul>
            </div>
            <ul class="recruit cell">
              <li>
                <a href="https://www.jobplanet.co.kr/companies/60595/job_postings/%EC%9C%84%EC%9E%90%EB%93%9C%EC%9B%8D%EC%8A%A4" class="table" target="_blank">
                  <div class="cell">
                    <p class="point">{{ langRst.recruit_ment01 }}</p>
                    <h4>Developer <img src="https://s3.ap-northeast-2.amazonaws.com/eosnova.io.resource/images/wzd-icon-arrow.png" width="10px"/></h4>
                    <p class="position">
                      <strong>Android / iOS / Web / Server</strong><br/>
                      {{ langRst.recruit_ment02 }}
                    </p>
                  </div>
                </a>
              </li>
              <li>
                <a href="https://www.jobplanet.co.kr/companies/60595/job_postings/%EC%9C%84%EC%9E%90%EB%93%9C%EC%9B%8D%EC%8A%A4" class="table" target="_blank">
                  <div class="cell">
                    <p class="point">{{ langRst.recruit_ment01 }}</p>
                    <h4>Designer <img src="https://s3.ap-northeast-2.amazonaws.com/eosnova.io.resource/images/wzd-icon-arrow.png" width="10px"/></h4>
                    <p class="position">
                      <strong>UX·UI / GUI</strong><br/>
                      {{ langRst.recruit_ment02 }}
                    </p>
                  </div>
                </a>
              </li>
              <li>
                <a href="https://www.jobplanet.co.kr/companies/60595/job_postings/%EC%9C%84%EC%9E%90%EB%93%9C%EC%9B%8D%EC%8A%A4" class="table" target="_blank">
                  <div class="cell">
                    <p class="point">{{ langRst.recruit_ment01 }}</p>
                    <h4>Operation <img src="https://s3.ap-northeast-2.amazonaws.com/eosnova.io.resource/images/wzd-icon-arrow.png" width="10px"/></h4>
                    <p class="position">
                      {{ langRst.recruit_ment02 }}
                    </p>
                  </div>
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <!-- CONTACT US -->
      <div class="table" id="contact">
        <div class="address cell">
          <div class="table">
            <div class="cell">
              <h2 class="contentTit">{{ langRst.contact_tit }}</h2>
              <div class="info">
                <h4 class="point">
                  Address
                </h4>
                <p>{{ langRst.address }}</p>
              </div>
              <div class="info">
                <h4 class="point">
                  Transport
                </h4>
                <p>
                  {{ langRst.transport01 }}<br/>
                  {{ langRst.transport02 }}
                </p>
              </div>
              <div class="info">
                <h4 class="point">
                  E-mail
                </h4>
                <p>support@wzdworks.com</p>
              </div>
            </div>
          </div>
        </div>
        <div class="cell" id="map">

        </div>
      </div>
      <!-- FOOTER -->
      <footer>
        <div class="inner">
          Copyright © Wizard Works Inc. All rights reserved.
        </div>
      </footer>
    </div>
</template>



<script>


  import { langState, langText, langRst, langTitle } from '../translations/language'
  import { team } from '../utils/team'
  import { partners } from '../utils/partners'

  export default {
    name: 'App',
    data() {
      return {
        fixHd: false,
        langState,
        langText,
        langRst,
        langTitle,
        team,
        partners,
        partnerList: [],
        teamList: [],
        windowWidth  : null,
        tabConHeight : [],
        domHeight : null,
        active : null,
        tabList : ['','NOVA Wallet','ThemeKeyboard','Somcloud'],
      }
    },
    created() {
      // console.log('aaa',this.langState, this.langTitle);
      window.addEventListener('scroll', this.scroll);

      Object.assign(this.langRst, this.langText.ko);
      this.langState = '한글';
      Object.assign(this.partnerList, this.partners.ko);
      Object.assign(this.teamList, this.team.ko);
    },
    destroyed () {
      // window.removeEventListener('scroll', this.scroll);
    },
    mounted(){
      /*
      'use strict';
      const objects = document.getElementsByClassName('asyncImage');
      Array.from(objects).map((item) => {
        const img = new Image();
        img.src = item.dataset.src;
        img.onload = () => {
          item.classList.remove('asyncImage');
          return item.nodeName === 'IMG' ?
            item.src = item.dataset.src :
            item.style.backgroundImage = `url(${item.dataset.src})`;
        };
      });
      */

      let mapContainer = document.getElementById('map'),
          mapOption = {
            center: new daum.maps.LatLng(37.555473, 126.973749),
            level: 3
          };
      let map = new daum.maps.Map(mapContainer, mapOption);

      let imageSrc = 'https://s3.ap-northeast-2.amazonaws.com/eosnova.io.resource/images/wzd-icon-pin.png',
        imageSize = new daum.maps.Size(50, 66),
        imageOption = {offset: new daum.maps.Point(27, 75)};

      let markerImage = new daum.maps.MarkerImage(imageSrc, imageSize, imageOption),
        markerPosition = new daum.maps.LatLng(37.555473, 126.973749);

      let marker = new daum.maps.Marker({
        position: markerPosition,
        image: markerImage
      });
      marker.setMap(map);
    },
    methods : {
      tabCtrl( btn ){
        let tabChild = document.getElementById('serviceTab').children,
            conChild = document.getElementById('serviceCont').children;
        this.tabConHeight = [];
        for (let i = 0; i < tabChild.length; i++) {
          tabChild[i].classList.remove('on');
          if ( i === Number(btn) ) {
            tabChild[i].className = 'on';
            conChild[i].className = 'on';
          }
          else {
            conChild[i].className = 'off';
            conChild[i].classList.remove('on');
          }
        }
      },
      scroll(){
        let nav = document.getElementById('header');
        let scrollPosition = window.scrollY;
        if (scrollPosition > 0) nav.classList.add('fix');
        else nav.classList.remove('fix');

        this.navActive();
      },
      langChange(){
        if( this.langState === 'ENG' ) {
          Object.assign(this.langRst, this.langText.ko);
          this.langState = '한글';
          this.langTitle = 'ENG';
          Object.assign(this.partnerList, this.partners.ko);
          Object.assign(this.teamList, this.team.ko);
        }
        else {
          Object.assign(this.langRst, this.langText.en);
          this.langState = 'ENG';
          this.langTitle = '한글';
          Object.assign(this.partnerList, this.partners.en);
          Object.assign(this.teamList, this.team.en);
        }
      },
      scrollTop(){
        window.scrollTo(0,0);
      },
      navActive() {
        let winPos = window.scrollY,
            navLi = document.getElementById('nav').children,
            navLen = document.getElementById('nav').children.length;
        for (let i = 0; i < navLen; i++) {
          let currentLi = navLi[i].children,
              currentId = currentLi[0].id,
              currentBtn = document.getElementById(currentId),
              currentLink = currentBtn.getAttribute('data-target');
          let targetTop = document.getElementById(currentLink).offsetTop,
              targetHeight = document.getElementById(currentLink).clientHeight;
          if (targetTop-200 <= winPos && (targetTop + targetHeight - 200) > winPos) {
            document.getElementById(currentId).classList.add('on');
          }
          else document.getElementById(currentId).classList.remove('on');
        }
      }
    }
  }
</script>
