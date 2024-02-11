<template>
  <div class="d-flex row justify-center align-center mt-10">
    <v-row>
      <v-col>
        <sportman1 class="img-sportman" />
      </v-col>
      <v-col>
        <div class="text-header">ATHLETES</div>
        <div v-for="(v, index) in ATHLETES" class="subject" :key="index" :style="`--bg-color: ${v.background}`">
          <div class="d-flex align-center">
            <span class="number" :style="v.dark ? `--underline: #fff` : `--underline: #603EBE `">{{ v.number }}</span>
            <span class="text-title">{{ v.title }}</span>
          </div>
          <div class="text-desc mt-2 mb-6" :style="v.dark ? `--text: #fff` : `--text: #000 `">{{ v.desc }}</div>
        </div>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <div class="text-header">PLAYERS</div>
        <div v-for="(v, index) in PLAYERS" class="subject" :key="index" :style="`--bg-color: ${v.background}`">
          <div class="d-flex align-center">
            <span class="number" :style="v.dark ? `--underline: #fff` : `--underline: #603EBE `">{{ v.number }}</span>
            <span class="text-title
            ">{{ v.title }}</span>
          </div>
          <div class="text-desc mt-2 mb-6" :style="v.dark ? `--text: #fff` : `--text: #000 `">{{ v.desc }}</div>
        </div>
      </v-col>
      <v-col>
        <sportman2 class="img-sportman" />
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
          desc: 'Work with other student athletes to  increase visability. When you share and like other players videos it will increase your visability as a player. This is the team work aspect to Surface 1.',
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
          background: '#5E3DB3',
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
}

.number {
  font-size: 18px;
  font-weight: 400;
  line-height: 21px;
  letter-spacing: 1.5px;
  text-align: left;
  padding-right: 5px;
  text-decoration: underline var(--underline) 5px;
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
}

.img-sportman {
  width: 100%;
  height: 100%;
}
</style>
