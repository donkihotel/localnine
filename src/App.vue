<template>
    <v-app>
        <!-- <v-main>
                                  <HelloWorld />
                                </v-main> -->
        <v-main>
            <section id="hero">
                <v-row no-gutters>
                    <v-img :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'" src="https://images.unsplash.com/photo-1487017159836-4e23ece2e4cf?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1951&q=80">
                        <v-theme-provider dark>
                            <v-container fill-height>
                                <v-row align="center" class="white--text mx-auto" justify="center">
                                    <v-col class="white--text text-center" cols="12" tag="h1">
                                        <span :class="[
                                            $vuetify.breakpoint.smAndDown
                                              ? 'display-1'
                                              : 'display-2',
                                          ]" class="font-weight-light">
                                          Weclome To
                                        </span>
    
                                        <br />
    
                                        <span :class="[
                                            $vuetify.breakpoint.smAndDown
                                              ? 'display-3'
                                              : 'display-4',
                                          ]" class="font-weight-black">
                                          Localnine
                                        </span>
                                    </v-col>
    
                                    <v-btn class="align-self-end" fab outlined @click="$vuetify.goTo('#about-me')">
                                        <v-icon>mdi-chevron-double-down</v-icon>
                                    </v-btn>
                                </v-row>
                            </v-container>
                        </v-theme-provider>
                    </v-img>
                </v-row>
            </section>
    
            <section id="about-me">
                <div class="py-12"></div>
    
                <v-container class="text-center">
                    <h2 class="display-2 font-weight-bold mb-3">ABOUT</h2>
    
                    <v-responsive class="mx-auto mb-8" width="56">
                        <v-divider class="mb-1"></v-divider>
    
                        <v-divider></v-divider>
                    </v-responsive>
    
                    <v-responsive class="mx-auto title font-weight-light mb-8 text-justify" max-width="720">
                        AWS는 아마존 웹 서비스이다. 우리는 AWS에서 서비스 구축, 교육, 문제해결을 도울 수 있는 일을 하고 있다. IT서비스 발전과 함께 많은 수의 개인 또는 회사들의 AWS 서비스에서 개발하고 사용하고자 하고 있다. 하지만 AWS 기술적 지식이 없으면 문제 해결을 외부로부터 도움을 받아야 한다. 그 외부는 AWS 컨설팅 회사일 경우가 있다. 하지만 이 회사들의 제공해주는 서비스 비용은 비싸다. 하지만 우리는 보다 합리적인 비용으로 개인 및 회사에
                        만족할 수 있는 서비스를 제공하고 있다.
                    </v-responsive>
    
                    <v-avatar class="elevation-12 mb-12" size="128">
                        <v-img src="@/assets/icons/me.jpg"></v-img>
                    </v-avatar>
    
                    <div></div>
    
                    <!-- <v-btn color="grey" href="https://vuetifyjs.com" outlined large>
                                            <span class="grey--text text--darken-1 font-weight-bold">
                                          ANOTHER PROJECT
                                        </span>
                                        </v-btn> -->
                </v-container>
    
                <div class="py-12"></div>
            </section>
    
            <section id="features" class="grey lighten-3">
                <div class="py-12"></div>
    
                <v-container class="text-center">
                    <h2 class="display-2 font-weight-bold mb-3">서비스</h2>
    
                    <v-responsive class="mx-auto mb-12" width="56">
                        <v-divider class="mb-1"></v-divider>
    
                        <v-divider></v-divider>
                    </v-responsive>
    
                    <v-row>
                        <v-col v-for="({ icon, title, text, price }, i) in features" :key="i" cols="12" md="4">
                            <v-card class="py-12 px-4" color="grey lighten-5" flat>
                                <v-theme-provider dark>
                                    <div>
                                        <v-avatar color="primary" size="88">
                                            <v-icon large v-text="icon"></v-icon>
                                        </v-avatar>
                                    </div>
                                </v-theme-provider>
    
                                <v-card-title class="justify-center font-weight-black text-uppercase" v-text="title"></v-card-title>
    
                                <v-card-text class="subtitle-1 text-justify" v-text="text">
                                </v-card-text>
                                <v-card-text class="subtitle-1">
                                    <div class="float-right font-weight-black">{{ price }}~</div>
                                </v-card-text>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-container>
    
                <div class="py-12"></div>
            </section>
    
            <section id="stats">
                <v-parallax :height="$vuetify.breakpoint.smAndDown ? 700 : 500" src="https://images.unsplash.com/photo-1510915228340-29c85a43dcfe?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80">
                    <v-container fill-height>
                        <v-row class="mx-auto">
                            <v-col v-for="[value, title] of stats" :key="title" cols="12" md="3">
                                <div class="text-center">
                                    <div class="display-3 font-weight-black mb-4" v-text="value"></div>
    
                                    <div class="title font-weight-regular text-uppercase" v-text="title"></div>
                                </div>
                            </v-col>
                        </v-row>
                    </v-container>
                </v-parallax>
            </section>
    
            <section id="blog">
                <div class="py-12"></div>
    
                <v-container>
                    <h2 class="display-2 font-weight-bold mb-3 text-uppercase text-center">
                        고객사례
                    </h2>
    
                    <v-responsive class="mx-auto mb-12" width="56">
                        <v-divider class="mb-1"></v-divider>
    
                        <v-divider></v-divider>
                    </v-responsive>
    
                    <v-row>
                        <v-col v-for="({ src, text, title, tag, price }, i) in paginatedOrders" :key="i" cols="12" md="4">
                            <v-img :src="require(`@/assets/images/${src}`)" class="mb-4" height="275" max-width="100%"></v-img>
    
                            <h3 class="font-weight-black mb-4 text-uppercase">
                                ({{ tag }}) {{ title }}
                            </h3>
    
                            <div class="title font-weight-light mb-5" v-text="text"></div>
    
                            <v-btn class="ml-n4 font-weight-black float-right" text>
                                작업비용: {{ price }}
                            </v-btn>
                        </v-col>
                    </v-row>
                </v-container>
    
                <div class="py-6"></div>
    
                <div class="text-center">
                    <v-btn color="grey" @click="loadMore()" outlined large v-if="currentPage * maxPerPage < articles.length">
                        <span class="grey--text text--darken-1 font-weight-bold">더 보기</span>
                    </v-btn>
                </div>
    
                <div class="py-12"></div>
            </section>
    
            <v-sheet id="contact" color="#333333" dark tag="section" tile>
                <div class="py-12"></div>
    
                <v-container class="text-center">
                    <h2 class="display-2 font-weight-bold mb-3 text-uppercase">문의</h2>
    
                    <v-responsive class="mx-auto mb-12" width="56">
                        <v-divider class="mb-1"></v-divider>
    
                        <v-divider></v-divider>
                    </v-responsive>
    
                    <v-theme-provider light>
                        <v-row>
                            <v-col cols="12">
                                <v-avatar size="52" rounded>
                                    <v-img src="@/assets/icons/kakao.jpg"></v-img>
                                </v-avatar>
                                <v-btn x-large href="https://open.kakao.com/o/sfJs7iHe" class="ml-2">
                                    <span class="grey--text text--darken-1 font-weight-bold">채팅 상담하기</span
                                  >
                                </v-btn>
                              </v-col>
                              <v-col cols="12">
                                <v-avatar size="52" rounded>
                                  <v-img src="@/assets/icons/mail.jpg"></v-img>
                                </v-avatar>
                                <v-btn
                                  x-large                 
                                  class="ml-2" 
                                  @click="mailCopy()"                   
                                  v-clipboard="copyText()"
                                >
                                  <span class="grey--text text--darken-1"
                                    >{{email}}</span
                                  >
                                </v-btn>
                              </v-col>              
                            </v-row>
                          </v-theme-provider>
                        </v-container>
                
                        <div class="py-12"></div>
                      </v-sheet>
                    </v-main>
                
                    <v-footer class="justify-center" color="#292929" height="100">
                      <div
                        class="title font-weight-light grey--text text--lighten-1 text-center"
                      >
                        &copy; {{ new Date().getFullYear() }} — AWS, LLC — Made with 💜 by
                        localnine
                      </div>
                    </v-footer>
                
                    <v-snackbar v-model="snackbar" color="success" timeout="3000" outlined>
                        {{ snackbarText }}
                    </v-snackbar>
                  </v-app>
</template>

<script>
//import HelloWorld from "./components/HelloWorld";

export default {
    name: "App",

    components: {
        //HelloWorld,
    },

    data() {
        return {
            snackbar: false,
            snackbarText: '준비중 입니다',
            features: [{
                    icon: "mdi-aws",
                    title: "설계 & 구축",
                    text: "JAVA, PHP, NODE, PYTHON 웹 서버 구축을 할 수있다. 고객의 목표로 하는 서비스에 맞추어 AWS 설계를 제안 할 수 있으며, 비용 최소화 된 웹 서버 구축, 또는 개발과 운영의 DevOps 구축을 제공한다",
                    price: "60,000원",
                },
                {
                    icon: "mdi-school",
                    title: "교육",
                    text: "고객의 필요로 하는 맞춤 AWS 교육을 제공해 줄 있다. 교육 방법은 팀뷰어 화면 공유 프로그램을 통해 목소리를 통해 제공한다. 교육은 AWS 기본, 구축된 AWS 관리,  DevOps, CI/CD 교육을 제공할 수 있다.",
                    price: "50,000원",
                },
                {
                    icon: "mdi-wrench",
                    title: "문제해결",
                    text: "AWS 사용하다보면, 알수없는 문제를 가질 수 있다. 이 문제는 개발된 프로그램과 AWS 와 긴밀한 관계를 가지고 있다. 우리는 프로그램에 대한 이해와 AWS 서버에 대한 이해를 바탕으로 문제 해결을 도울수 있다",
                    price: "20,000원",
                },
            ],
            stats: [
                ["16+", "설계 & 구축"],
                ["13+", "교육"],
                ["20+", "문제해결"],
                ["49+", "전체 작업 수"],
            ],
            articles: [{
                    tag: "구축",
                    src: "22-01-02-01.jpg",
                    title: "쇼핑몰 세일즈 솔루션 웹 서버",
                    text: "RDS MYSQL, EC2 아파치 PHP 코드이그나이터, Certficate, ELB, Route 구성하여 SSL 적용 도메인 연결 구성하여 소스 이전 해드림",
                    price: "60,000원",
                },
                {
                    tag: "구축/교육",
                    src: "22-01-04-01.jpg",
                    title: "포토폴리오 웹 서버",
                    text: "RDS MYSQL, EC2 Nginx-React NodeExepress, Route 구성하여 도메인 연결 구성하여 소스 이전과 교육도 해드림",
                    price: "60,000원",
                },
                {
                    tag: "구축",
                    src: "22-01-10-01.jpg",
                    title: "스타트업 솔루션 웹 서버",
                    text: "RDS MARIADB, EC2 Nginx-Vue NodeExepress, Certficate, ELB, Route 구성하여 SSL 적용된 도메인 연결 구성하여 소스 이전 해드림",
                    price: "60,000원",
                },
                {
                    tag: "문제해결",
                    src: "22-01-20-01.jpg",
                    title: "서버 응답없음",
                    text: "사용중인 AWS에서 서버 장애가 발생하여, 연결된 부분을 추적하여 ELB, EC2에서 어플리케이션 헬스체크가 되지 않던 부분을 개선하여 정상화시킴",
                    price: "30,000원",
                },                
                {
                    tag: "문제해결",
                    src: "22-01-24-01.jpg",
                    title: "서버 비용 감소",
                    text: "홈페이지로 2개의 EC2 사용하고 있으며, 다수의 EBS를 사용하고 있는것이 확인됨. 사용하지 않는 리소스를 해제하고, EC2 사양을 낮추어 서버 비용을 10만원대에서 3만원으로 다운시켜 드림",
                    price: "30,000원",
                },
                {
                    tag: "문제해결",
                    src: "22-01-27-01.jpg",
                    title: "AWS SSL연결",
                    text: "구축된 EC2 서버에 AWS SSL 적용을 ELB로 연결하여 HTTPS 서비스 연결을 해드림",
                    price: "30,000원",
                },
                {
                    tag: "문제해결",
                    src: "22-02-04-01.jpg",
                    title: "서버 500에러 발생",
                    text: "사용중인 EC2에서 500에러 발생, 스프링을 개발된 프로그램을 추적하여 DB 핸들링할때 에러가 발생되는 원인의 발견됨. 관련하여 DB 키 및 데이터 중복관련하여 프로그램 조치를 가이드 해드림",
                    price: "30,000원",
                },
                {
                    tag: "교육",
                    src: "22-03-15-01.jpg",
                    title: "PHP를 활용한 AWS 웹 서버 구축",
                    text: "원격 화면 공유프로그램을 통하여 AWS 이해, 비용, 네트워크, EC2(PHP), RDS, ROUTE 구축 및 관리 사용법에 대한 기본 이해를 교육으로 제공",
                    price: "50,000원",
                },
                {
                    tag: "문제해결",
                    src: "22-03-21-01.jpg",
                    title: "EC2 PHP ionCube 설치",
                    text: "EC2에 PHP ionCube를 설치를 도와드림",
                    price: "30,000원",
                },
                {
                    tag: "구축",
                    src: "22-03-23-01.jpg",
                    title: "HTML로 구성된 홈페이지 웹 서버",
                    text: "EC2에 NGINX를 구성하여 Openl SSL – Lets Encrypt 설치를 해드림",
                    price: "40,000원",
                },
                // 추가
                {
                    tag: "문제해결",
                    src: "22-04-07-01.jpg",
                    title: "CloudFront 에 도메인 연결 안됨",
                    text: "S3, CloudFront, Certificate, Route 점검하여  SSL 적용된 도메인 연결을 해드림",
                    price: "30,000원",
                },
                {
                    tag: "문제해결",
                    src: "22-04-14-01.jpg",
                    title: "DB 접속 에러",
                    text: "PHP와 연결해서 사용중인 MySQL에서 DB 연결 에러가 발생하여, MySQL 설정을 조정하여 정상 작동 해드림",
                    price: "30,000원",
                },
                {
                    tag: "구축",
                    src: "22-04-16-01.jpg",
                    title: "포토폴리오 웹 서비스 구축",
                    text: "도메인 연결 Route, EC2에 Nginx, Node, MongoDB 로 구성하여, 소스 이전하고 하여 구축 해드림",
                    price: "60,000원",
                },
                {
                    tag: "교육",
                    src: "22-04-19-01.jpg",
                    title: "AWS VUE 웹 서버 구축",
                    text: "도메인 연결 Route, EC2에 Nginx Vue, Node, MongoDB 로 구성하는 웹 서버 구축 교육을 해드림",
                    price: "50,000원",
                },
                {
                    tag: "구축",
                    src: "22-05-10-01.jpg",
                    title: "학교축제 웹 서버",
                    text: "도메인 Route,  RDS Mysql, EC2에 Nginx, Node를 설치하여, 소스 이전하고 구축 해드림",
                    price: "60,000원",
                },
                {
                    tag: "구축",
                    src: "22-05-12-01.jpg",
                    title: "프론트만 있는 React 기반 포토폴리오 사이트",
                    text: "도메인 Route,  CloudFront, S3에 React 빌드 배포를 하여 SSL연결된 웹 서버 구축 해드림",
                    price: "40,000원",
                },
                {
                    tag: "구축",
                    src: "22-06-15-01.jpg",
                    title: "포토폴리오 웹 서버",
                    text: "도메인 Route,  RDS MySQL, CloudFront, EC2에 Nginx Tomcat Spring 소스를 배포하여 웹 서버 구축 해드림",
                    price: "60,000원",
                },
                {
                    tag: "문제해결",
                    src: "22-07-06-01.jpg",
                    title: "웹 사이트 SSL 갱신 문제",
                    text: "AWS 웹 서바가 구축되어 있고 배포된 소스에 SSL 인증서가 갱신되지 않는 부분을 Spring 배포소스 분석하여 SSL 인증서 첨부하여다시 패키징해서 문제해결을 도와드림",
                    price: "60,000원",
                },
                {
                    tag: "문제해결",
                    src: "22-07-07-01.jpg",
                    title: "사용중인  AWS 비용 축소",
                    text: "사용중 EC2 에서 서버 성능을 축소하여 비용 감면을 해드리고, EC2에 있는 불필요한 프로세스스 해제를 낮은 사양에서도 서비스가 잘 돌아가도록 해드림",
                    price: "40,000원",
                },
                {
                    tag: "문제해결",
                    src: "22-07-09-01.jpg",
                    title: "사용중인  PHP 기반 CI/CD 작동 오류",
                    text: "GitHub, S3, CodeDeploy, EC2, ELB, Route 를 점검하여 정상적으로 작동되도록 조치를 해드리고 교육을 해드림",
                    price: "100,000원",
                },
                {
                    tag: "구축",
                    src: "22-07-25-01.jpg",
                    title: "회사 웹 서버 구축",
                    text: "도메인 Route, RDS Mysql, EC2에 Nginx, Node를 구성하여 웹 서버 구축 해드림",
                    price: "60,000원",
                },
            ],
            email: 'localnine@naver.com',
            currentPage: 1,
            maxPerPage: 6

        };
    },
    computed: {
        totalResults() {
            return Object.keys(this.articles).length
        },
        pageCount() {
            return Math.ceil(this.totalResults / this.maxPerPage)
        },
        pageOffest() {
            return this.maxPerPage * this.currentPage
        },
        paginatedOrders() {
            return this.articles.slice(0, this.currentPage * this.maxPerPage);
        }
    },
    methods: {
        articleShow() {
            this.snackbarText = '준비중 입니다'
            this.snackbar = true
        },
        prev() {
            this.current--;
        },
        loadMore() {
            this.currentPage += 1
        },
        copyText() {
            return this.email;
        },
        mailCopy() {
            this.snackbarOpen()
        },
        snackbarOpen() {
            this.snackbarText = '메일 주소가 복사되었습니다'
            this.snackbar = true
        },
    },
    created() {}
};
</script>
