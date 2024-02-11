<template>
  <div class="d-flex row justify-center align-center mt-10">
    <v-row>
      <v-col lg="6" xs="12" class="hide-on-mobile" style="padding: 0;">
        <div class="img-container">
          <sportman1 class="img-sportman1" />
          <div class="text-header nearby"></div>
          <div class="subject"></div>
          <div class="subject" style=" --bg-color: #F5F4F9"></div>
          <div class="subject" style="--bg-color: #5E3DB3"></div>
        </div>
      </v-col>
      <v-col lg="6" xs="12" style="padding: 0;">
        <div class="text-header">ATHLETES</div>
        <div v-for="(v, index) in ATHLETES" class="subject" :key="index" :style="`--bg-color: ${v.background}`">
          <div class="d-flex align-center">
            <span class="number"
              :style="v.dark ? `--underline: #fff; --text-color: #603EBE ` : `--underline: #603EBE;  --text-color : #000`">{{
                v.number }}</span>
            <span class="text-title">{{ v.title }}</span>
          </div>
          <div class="text-desc mt-2 mb-6" :style="v.dark ? `--text: #fff` : `--text: #000 `">{{ v.desc }}</div>
        </div>
        <div class="show-only-mobile">
          <div class="img-container">
            <sportman1 class="img-sportman1" />
            <v-carousel :show-arrows="false" style="height: 250px;">
              <v-carousel-item v-for="(item, i) in ATHLETES" :key="i">
                <v-sheet :color="item.background" height="250">
                  <v-row class="fill-height" align="center" justify="center">
                    <div class="pa-10">
                      <div class="d-flex align-center">
                        <span class="number"
                          :style="item.dark ? `--underline: #fff; --text-color: #603EBE ` : `--underline: #603EBE; --text-color : #000`">{{
                            item.number }}</span>
                        <span class="text-title">{{ item.title }}</span>

                      </div>
                      <div>
                        <div class="text-desc mt-2 mb-6" :style="item.dark ? `--text: #fff` : `--text: #000 `">{{
                          item.desc }}
                        </div>
                      </div>
                    </div>
                  </v-row>
                </v-sheet>
              </v-carousel-item>
            </v-carousel>
          </div>
        </div>
      </v-col>
    </v-row>
    <v-row>
      <v-col lg="6" xs="12" style="padding: 0;">
        <div class="text-header">PLAYERS</div>
        <div v-for="(v, index) in PLAYERS" class="subject" :key="index" :style="`--bg-color: ${v.background}`">
          <div class="d-flex align-center">
            <span class="number"
              :style="v.dark ? `--underline: #fff; --text-color: #603EBE ` : `--underline: #603EBE; --text-color : #000`">{{
                v.number }}</span>
            <span class="text-title
            ">{{ v.title }}</span>
          </div>
          <div class="text-desc mt-2 mb-6" :style="v.dark ? `--text: #fff` : `--text: #000 `">{{ v.desc }}</div>
        </div>
        <div class="show-only-mobile">
          <div class="img-container">
            <sportman2 class="img-sportman2" />
            <v-carousel :show-arrows="false" style="height: 250px;">
              <v-carousel-item v-for="(item, i) in PLAYERS" :key="i">
                <v-sheet :color="item.background" height="250">
                  <v-row class="fill-height" align="center" justify="center">
                    <div class="pa-10">
                      <div class="d-flex align-center">
                        <span class="number"
                          :style="item.dark ? `--underline: #fff; --text-color: #603EBE ` : `--underline: #603EBE; --text-color : #000`">{{
                            item.number }}</span>
                        <span class="text-title">{{ item.title }}</span>

                      </div>
                      <div>
                        <div class="text-desc mt-2 mb-6" :style="item.dark ? `--text: #fff` : `--text: #000 `">{{
                          item.desc }}
                        </div>
                      </div>
                    </div>
                  </v-row>
                </v-sheet>
              </v-carousel-item>
            </v-carousel>
          </div>
        </div>
      </v-col>
      <v-col lg="6" xs="12" style="padding: 0;" class="hide-on-mobile">
        <div class="img-container">
          <sportman2 class="img-sportman2" />
          <div class="text-header nearby"></div>
          <div class="subject"></div>
          <div class="subject" style=" --bg-color: #F5F4F9"></div>
          <div class="subject" style="--bg-color: #090C35"></div>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      ATHLETES: [
        {
          number: '01',
          title: 'CONNECTION',
          desc: 'Connect with coaches directly, you can ping coaches to view profile.',
          background: '#fff',
          dark: false
        },
        {
          number: '02',
          title: 'COLLABORATION',
          desc: 'Work with other student athletes to increase visability. When you share and like other players videos it will increase your visability as a player. This is the team work aspect to Surface 1.',
          background: '#F5F4F9',
          dark: false
        },
        {
          number: '03',
          title: 'GROWTH',
          desc: 'Resources and tools for you to get better as a student Athelte. Access to training classes, tutor sessions, etc',
          background: '#5E3DB3',
          dark: true
        }
      ],
      PLAYERS: [
        {
          number: '01',
          title: 'CONNECTION',
          desc: 'Connect with talented athlete directly, you can watch their skills through video showreels directly from Surface 1.',
          background: '#fff',
          dark: false
        },
        {
          number: '02',
          title: 'COLLABORATION',
          desc: 'Work with recruiter to increase your chances of finding talented athlete.',
          background: '#F5F4F9',
          dark: false
        },
        {
          number: '03',
          title: 'GROWTH',
          desc: 'Save your time, recruit proper athlets for your team.',
          background: '#090C35',
          dark: true
        }
      ]
    }
  }
}
</script>
<style>
.text-header {
  font-weight: 400;
  font-size: 90px;
  line-height: 105.47px;
  color: #E7E7E7;
  margin-bottom: 60px;
  height: 105.48px;
}

.number {
  font-size: 18px;
  font-weight: 400;
  line-height: 21px;
  letter-spacing: 1.5px;
  text-align: left;
  padding-right: 5px;
  text-decoration: underline var(--underline) 5px;
  color: var(--text-color);
}

.text-title {
  font-size: 36px;
  font-weight: 400;
  line-height: 42px;
  letter-spacing: 1.5px;
  text-align: left;
  color: #C2C2C2;
}

.text-desc {
  font-size: 20px;
  font-weight: 400;
  line-height: 28px;
  letter-spacing: 0px;
  text-align: left;
  color: var(--text);
}

.subject {
  height: 210px;
  display: grid;
  align-content: center;
  background-color: var(--bg-color);
  width: 100%;
  padding-left: 20px;
  z-index: -1;
}

.img-sportman1 {
  width: 678px;
  height: 950px;
  top: -50px;
  left: 175px;
  position: absolute;
}

.img-sportman2 {
  width: 991px;
  height: 815px;
  top: 0px;
  left: -50px;
  position: absolute;
}

/* Base font size */
.text-title {
  font-size: 36px;
}

.img-container {
  position: relative;
}

.show-only-mobile {
  display: none;
}

/* Smaller font size on smaller screens */
@media (max-width: 768px) {

  .img-sportman1 {
    width: 518px;
    height: 719px;
    top: 20px;
    left: -161px;
    position: absolute;
  }

  .img-sportman2 {
    width: 518px;
    height: 719px;
    top: 20px;
    left: -161px;
    position: absolute;
  }

  .text-header {
    font-weight: 400;
    font-size: 60px;
    line-height: 70px;
    color: #E7E7E7;
    margin-bottom: 60px;
  }

  .number {
    font-size: 18px;
    font-weight: 400;
    line-height: 21px;
    letter-spacing: 1.5px;
    text-align: left;
    padding-right: 5px;
    text-decoration: underline var(--underline) 5px;
    color: var(--text-color);
  }

  .text-title {
    font-size: 24px;
    font-weight: 400;
    line-height: 28px;
    letter-spacing: 1.5px;
    text-align: left;
    color: #C2C2C2;
  }

  .text-desc {
    font-size: 20px;
    font-weight: 400;
    line-height: 28px;
    letter-spacing: 0px;
    text-align: left;
    color: var(--text);
  }

  .subject {
    height: 210px;
    display: grid;
    align-content: center;
    background-color: var(--bg-color);
    z-index: -1;
  }

}

@media screen and (max-width: 320px) {
  .subject {
    display: none;
  }

  .text-header {
    display: flex;
    justify-content: start;
    ;
    margin: 0;
    font-size: 50px;
    font-weight: 400;
    line-height: 59px;
    letter-spacing: 0px;
    text-align: left;
    height: 300px;
    padding-left: 20px;
  }

  .text-header.nearby {
    display: none;
  }

  .img-sportman1 {
    display: none;
  }

  .img-sportman2 {
    display: none;
  }

  .hide-on-mobile {
    display: none;
  }

  .show-only-mobile .img-sportman1 {
    position: absolute;
    width: 218px;
    height: 281px;
    top: -250px;
    left: 51px;
    display: block;
    z-index: 1;
  }

  .show-only-mobile .img-sportman2 {
    position: absolute;
    width: 218px;
    height: 281px;
    top: -250px;
    left: 51px;
    display: block;
    z-index: 1;
  }

  .show-only-mobile {
    display: block;
  }

  .text-desc {
    font-size: 15px;
    font-weight: 400;
    line-height: 18px;
    letter-spacing: 0em;
    text-align: left;
  }
}
</style>
