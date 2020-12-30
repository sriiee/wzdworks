<template>
  <div id="main">
    <div class="main_top" style="background-color:#333; height:100%;">
      <div class="inner table">
        <div class="cell">
          <h2>Wizard<br/>Works<span style="color:#f5732e;">.</span></h2>
          <p>
            {{ langRst.main_title01 }}<br/>
            {{ langRst.main_title02 }}
          </p>
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
              <span style="display:inline-block; width:90px; height:90px; background:#eee;"></span>
            </p>
            <h4 class="tit">{{ langRst.philosophy_tab_tit01 }}</h4>
            <div class="sub"><p>{{ langRst.philosophy_tab_sub01 }}</p></div>
          </li>
          <li>
            <p class="img">
              <span style="display:inline-block; width:90px; height:90px; background:#eee;"></span>
            </p>
            <h4 class="tit">{{ langRst.philosophy_tab_tit02 }}</h4>
            <div class="sub"><p>{{ langRst.philosophy_tab_sub02 }}</p></div>
          </li>
          <li>
            <p class="img">
              <span style="display:inline-block; width:90px; height:90px; background:#eee;"></span>
            </p>
            <h4 class="tit">{{ langRst.philosophy_tab_tit03 }}</h4>
            <div class="sub"><p>{{ langRst.philosophy_tab_sub03 }}</p></div>
          </li>
        </ul>
      </div>
    </div>
    <!-- SERVICE -->
    <div class="content" id="service">
      <div class="inner">
        <h2 class="contentTit">{{ langRst.ourServices }}</h2>
        <div class="tabCont">

          <v-tabs v-model="active" fixed-tabs>
            <v-tab
              v-for="n in 3"
              :key="n"
              ripple
              @click="next(n)"
            >
              {{ tabList[n] }}
            </v-tab>
            <v-tab-item :key="1">
              <v-card flat>
                <div class="con table on" id="nova">
                  <div class="txt cell">
                    <h4>NOVA <span>Wallet</span></h4>
                    <p>
                      {{ langRst.novaWallet_txt01 }}<br/>
                      {{ langRst.novaWallet_txt02 }}
                    </p>
                    <div class="downLink">
                      <a href="javascript:void(0)">{{ langRst.appStore }}</a>
                      <a href="javascript:void(0)">{{ langRst.googlePlay }}</a>
                      <a href="javascript:void(0)">{{ langRst.web }}</a>
                    </div>
                  </div>
                  <div class="img cell">
                    <p style="width:100%; max-width:350px; height:400px; background:#131415"></p>
                  </div>
                </div>
              </v-card>
            </v-tab-item>
            <v-tab-item :key="2">
              <v-card flat>
                <div class="con table on" id="keyboard">
                  <div class="txt cell">
                    <h4>2NOVA <span>Wallet</span></h4>
                    <p>
                      {{ langRst.novaWallet_txt01 }}<br/>
                      {{ langRst.novaWallet_txt02 }}
                    </p>
                    <div class="downLink">
                      <a href="javascript:void(0)">{{ langRst.appStore }}</a>
                      <a href="javascript:void(0)">{{ langRst.googlePlay }}</a>
                      <a href="javascript:void(0)">{{ langRst.web }}</a>
                    </div>
                  </div>
                  <div class="img cell">
                    <p style="width:100%; max-width:350px; height:400px; background:#131415"></p>
                  </div>
                </div>
              </v-card>
            </v-tab-item>
            <v-tab-item :key="3">
              <v-card flat>
                <div class="con table on" id="somcloud">
                  <div class="txt cell">
                    <h4>3NOVA <span>Wallet</span></h4>
                    <p>
                      {{ langRst.novaWallet_txt01 }}<br/>
                      {{ langRst.novaWallet_txt02 }}
                    </p>
                    <div class="downLink">
                      <a href="javascript:void(0)">{{ langRst.appStore }}</a>
                      <a href="javascript:void(0)">{{ langRst.googlePlay }}</a>
                      <a href="javascript:void(0)">{{ langRst.web }}</a>
                    </div>
                  </div>
                  <div class="img cell">
                    <p style="width:100%; max-width:350px; height:400px; background:#131415"></p>
                  </div>
                </div>
              </v-card>
            </v-tab-item>
          </v-tabs>


        </div>
        <!--
        <ul id="serviceTab">
          <li class="on" @click="tabCtrl('0','a')" id="service01"><a href="javascript:void(0)">{{ langRst.novaWallet }}</a></li>
          <li @click="tabCtrl('1','b')" id="service02"><a href="javascript:void(0)">{{ langRst.themeKeyboard }}</a></li>
          <li @click="tabCtrl('2','c')" id="service03"><a href="javascript:void(0)">{{ langRst.somcloud }}</a></li>
        </ul>
        <ul class="tabCont" id="serviceCont">
          <li class="con table on" id="nova">
            <div class="txt cell">
              <h4>NOVA <span>Wallet</span></h4>
              <p>
                {{ langRst.novaWallet_txt01 }}<br/>
                {{ langRst.novaWallet_txt02 }}
              </p>
              <div class="downLink">
                <a href="javascript:void(0)">{{ langRst.appStore }}</a>
                <a href="javascript:void(0)">{{ langRst.googlePlay }}</a>
                <a href="javascript:void(0)">{{ langRst.web }}</a>
              </div>
            </div>
            <div class="img cell">
              <p style="width:100%; max-width:350px; height:400px; background:#131415"></p>
            </div>
          </li>
          <li class="con table" id="keyboard">
            <div class="txt cell">
              <h4>ThemeKeyboard</h4>
              <p>
                {{ langRst.keyboard_txt01 }}
              </p>
              <div class="downLink">
                <a href="javascript:void(0)">{{ langRst.googlePlay }}</a>
              </div>
            </div>
            <div class="img cell">
              <p style="width:100%; max-width:350px; height:400px; background:#f5732e"></p>
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
                <a href="javascript:void(0)">{{ langRst.appStore }}</a>
                <a href="javascript:void(0)">{{ langRst.googlePlay }}</a>
                <a href="javascript:void(0)">{{ langRst.web }}</a>
              </div>
            </div>
            <div class="img cell">
              <p style="width:100%; max-width:450px; height:400px; background:#ef311d"></p>
            </div>
          </li>
        </ul>
    -->
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
            <p class="title">{{item.name}}</p>
            <p>{{item.work}}</p>
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
          {{ langRst.career_sub01 }}<br/>
          {{ langRst.career_sub02 }}<br/>
          <strong>apply@wzdworks.com</strong>
        </p>
        <div class="careerBox table">
          <div class="benefit cell">
            <ul>
              <li>
                <h4 class="tit">
                  <span>1</span>
                  {{ langRst.benefit_tit01 }}
                </h4>
                <p>{{ langRst.benefit_sub01_01 }}</p>
                <p>{{ langRst.benefit_sub01_02 }}</p>
              </li>
              <li>
                <h4 class="tit">
                  <span>2</span>
                  {{ langRst.benefit_tit02 }}
                </h4>
                <p>{{ langRst.benefit_sub02_01 }}</p>
                <p>{{ langRst.benefit_sub02_02 }}</p>
              </li>
              <li>
                <h4 class="tit">
                  <span>3</span>
                  {{ langRst.benefit_tit03 }}
                </h4>
                {{ langRst.benefit_sub03 }}
              </li>
              <li>
                <h4 class="tit">
                  <span>4</span>
                  {{ langRst.benefit_tit04 }}
                </h4>
                {{ langRst.benefit_sub04 }}
              </li>
              <li>
                <h4 class="tit">
                  <span>5</span>
                  {{ langRst.benefit_tit05 }}
                </h4>
                {{ langRst.benefit_sub05 }}
              </li>
              <li>
                <h4 class="tit">
                  <span>6</span>
                  {{ langRst.benefit_tit06 }}
                </h4>
                {{ langRst.benefit_sub06 }}
              </li>
              <li>
                <h4 class="tit">
                  <span>7</span>
                  {{ langRst.benefit_tit07 }}
                </h4>
                {{ langRst.benefit_sub07 }}
              </li>
              <li>
                <h4 class="tit">
                  <span>8</span>
                  {{ langRst.benefit_tit08 }}
                </h4>
                {{ langRst.benefit_sub08 }}
              </li>
            </ul>
          </div>
          <ul class="recruit cell">
            <li>
              <a href="javascript:void(0)" class="table">
                <div class="cell">
                  <p class="point">{{ langRst.recruit_ment01 }}</p>
                  <h4>Developer &gt;</h4>
                  <p class="position">
                    <strong>Android / iOS / Web / Server</strong><br/>
                    {{ langRst.recruit_ment02 }}
                  </p>
                </div>
              </a>
            </li>
            <li>
              <a href="javascript:void(0)" class="table">
                <div class="cell">
                  <p class="point">{{ langRst.recruit_ment01 }}</p>
                  <h4>Designer &gt;</h4>
                  <p class="position">
                    <strong>UX·UI / GUI</strong><br/>
                    {{ langRst.recruit_ment02 }}
                  </p>
                </div>
              </a>
            </li>
            <li>
              <a href="javascript:void(0)" class="table">
                <div class="cell">
                  <p class="point">{{ langRst.recruit_ment01 }}</p>
                  <h4>Operation &gt;</h4>
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
      this.lang = navigator.language || navigator.userLanguage;
      if (this.lang === 'ko-KR' || this.lang === 'ko') {
        Object.assign(this.langRst, this.langText.ko);
        this.langState = '한글';
        Object.assign(this.partnerList, this.partners.ko);
        Object.assign(this.teamList, this.team.ko);
      } else {
        Object.assign(this.langRst, this.langText.en);
        this.langState = 'ENG';
        Object.assign(this.partnerList, this.partners.en);
        Object.assign(this.teamList, this.team.en);
      }
    },
    beforeDestroy(){
      window.removeEventListener('resize', this.getWindowWidth);
    },
    mounted(){
      let domHeight = document.getElementById('nova').clientHeight,
        wrap = document.getElementById('serviceCont');
      wrap.style.height = domHeight+'px';

      this.$nextTick(function() {
        window.addEventListener('resize', this.getWindowWidth);
        this.getWindowWidth();
      })
    },
    methods : {
      tabCtrl( btn ){
        let tabChild = document.getElementById('serviceTab').children,
          conChild = document.getElementById('serviceCont').children,
          wrap = document.getElementById('serviceCont');
        this.tabConHeight = [];
        for (let i = 0; i < tabChild.length; i++) {
          tabChild[i].classList.remove('on');
          conChild[i].classList.remove('on');
          if ( i === Number(btn) ) {
            tabChild[i].className = 'on';
            conChild[i].className = 'on';
          }
          if( conChild[i].classList.contains('on') ) this.domHeight = conChild[i].clientHeight;
        }
        wrap.style.height = this.domHeight+'px';
      },
      getWindowWidth() {
        // this.windowWidth = document.documentElement.clientWidth;
        let tabChild = document.getElementById('serviceCont').children,
          wrap = document.getElementById('serviceCont');
        this.tabConHeight = [];
        for (let i = 0; i < tabChild.length; i++) {
          if( tabChild[i].classList.contains('on') ) this.domHeight = tabChild[i].clientHeight;
        }
        wrap.style.height = this.domHeight+'px';
      },
      next( i ){
        console.log(i);

      }
    }
  }
</script>

<style scoped>

</style>
