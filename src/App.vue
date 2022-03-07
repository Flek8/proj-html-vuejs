<template>
  <div id="app">
      <MyHeader :menuList="headerList"/>
      <MyMain/>
      <MyFooter :lists="footerLists"/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';
import MyFooter from './components/MyFooter.vue';
import "@fontsource/open-sans";

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MyFooter,
  },
  data() {
        return {
            headerList: ['HOME','ABOUT','SERVICES','PROCESS','TEAM','BLOG'],
            footerLists: [
                {
                    name: 'About',
                    items: [
                        'The Company',
                        'Institutional',
                        'Social & Events',
                        'Innovation',
                        'Environment',
                        'Technology'
                    ]
                },
                {
                    name: 'Services',
                    items: [
                        'Audit & Assurance',
                        'Financial Advisory',
                        'Analytics M&A',
                        'Middle Marketing',
                        'Legal Consulting',
                        'Regulatory Risk'
                    ]
                },
                {
                    name: 'Support',
                    items: [
                        'Responsibility',
                        'Terms of Use',
                        'About Cookies',
                        'Privacy Policy',
                        'Accessibility',
                        'Information'
                    ]
                }
            ]
        }
    }
}
</script>

<style lang="scss">

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "open-sans", sans-serif;
  }
  .boxed-text {
    padding: 5px 7px;
    background-color: #72b1b43a;
    border-radius: 3px;
  }
  .boxed-text-dark {
    padding: 5px 7px;
    background-color: #0483835e;
    border-radius: 3px;
  }
  i {
      color: #048383;
  }
</style>
