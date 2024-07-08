<script setup lang="ts">
import { nextTick, ref } from 'vue';
import { event, useQuasar } from 'quasar';
const $q = useQuasar();

const player = ref();
const playButton = ref();
const title = ref();
const year = ref();
const cover = ref();
const p1 = ref();
const t1 = ref();
const t2 = ref();
const p2 = ref();
const t3 = ref();
const t4 = ref();
const p3 = ref();
const p4 = ref();
const p5 = ref();
const t5 = ref();
const p6 = ref();
const p7 = ref();
const t6 = ref();
const p8 = ref();
const p9 = ref();
const p10 = ref();
const p11 = ref();
const p12 = ref();
const p13 = ref();
const t7 = ref();
const p14 = ref();
const p15 = ref();
const p16 = ref();
const p17 = ref();
const p18 = ref();
const p19 = ref();
const t8 = ref();
const p20 = ref();
const p21 = ref();
const t9 = ref();
const t10 = ref();
const t11 = ref();
const animateList = [
  {
    time: 0,
    fun: () => {
      playButton.value.classList.add('animate');
    },
  },
  {
    time: 12,
    fun: () => {
      title.value.classList.add('animate');
    },
  },
  {
    time: 38,
    fun: () => {
      year.value.classList.add('animate');
    },
  },
  {
    time: 50,
    fun: () => {
      cover.value.classList.add('animate');
    },
  },
  {
    time: 59,
    fun: () => {
      p1.value.classList.add('animate');
    },
  },
  {
    time: 60,
    fun: () => {
      t1.value.classList.add('animate');
    },
  },
  {
    time: 80,
    fun: () => {
      t2.value.classList.add('animate');
    },
  },
  {
    time: 94.5,
    fun: () => {
      p2.value.classList.add('animate');
    },
  },
  {
    time: 96,
    fun: () => {
      t3.value.classList.add('animate');
    },
  },
  {
    time: 113.5,
    fun: () => {
      t4.value.classList.add('animate');
    },
  },
  {
    time: 125.5,
    fun: () => {
      p3.value.classList.add('animate');
    },
  },
  {
    time: 127.5,
    fun: () => {
      p4.value.classList.add('animate');
    },
  },
  {
    time: 129.5,
    fun: () => {
      p5.value.classList.add('animate');
    },
  },
  {
    time: 132.5,
    fun: () => {
      t5.value.classList.add('animate');
    },
  },
  {
    time: 141.5,
    fun: () => {
      p6.value.classList.add('animate');
    },
  },
  {
    time: 143.5,
    fun: () => {
      p7.value.classList.add('animate');
    },
  },
  {
    time: 147,
    fun: () => {
      t6.value.classList.add('animate');
    },
  },
  {
    time: 163.5,
    fun: () => {
      p8.value.classList.add('animate');
    },
  },
  {
    time: 171.5,
    fun: () => {
      p9.value.classList.add('animate');
    },
  },
  {
    time: 179.5,
    fun: () => {
      p10.value.classList.add('animate');
    },
  },
  {
    time: 181,
    fun: () => {
      p11.value.classList.add('animate');
    },
  },
  {
    time: 183,
    fun: () => {
      p12.value.classList.add('animate');
    },
  },
  {
    time: 185.5,
    fun: () => {
      p13.value.classList.add('animate');
    },
  },
  {
    time: 190,
    fun: () => {
      t7.value.classList.add('animate');
    },
  },
  {
    time: 212,
    fun: () => {
      p14.value.classList.add('animate');
    },
  },
  {
    time: 214,
    fun: () => {
      p15.value.classList.add('animate');
    },
  },
  {
    time: 216,
    fun: () => {
      p16.value.classList.add('animate');
    },
  },
  {
    time: 218,
    fun: () => {
      p17.value.classList.add('animate');
    },
  },
  {
    time: 222,
    fun: () => {
      p18.value.classList.add('animate');
    },
  },
  {
    time: 228.5,
    fun: () => {
      p19.value.classList.add('animate');
    },
  },
  {
    time: 236,
    fun: () => {
      t8.value.classList.add('animate');
    },
  },
  {
    time: 246,
    fun: () => {
      p20.value.classList.add('animate');
    },
  },
  {
    time: 247.5,
    fun: () => {
      p21.value.classList.add('animate');
    },
  },
  {
    time: 260.5,
    fun: () => {
      t9.value.classList.add('animate');
    },
  },
  {
    time: 274,
    fun: () => {
      t10.value.classList.add('animate');
    },
  },
  {
    time: 285.5,
    fun: () => {
      t11.value.classList.add('animate');
    },
  },
];
const clickListener = () => {
  //$q.fullscreen.request();
  player.value.play();
  //player.value.currentTime = 260;
  const interval = setInterval(() => {
    console.log(player.value.currentTime);
    if (player.value.currentTime >= animateList[0].time) {
      animateList.shift()?.fun();
      if (animateList.length === 0) {
        clearInterval(interval);
      }
    }
  }, 100);
  removeEventListener('click', clickListener);
};

const egg1 = ref();
const egg2 = ref();

const firstEnd = () => {
  player.value.volume = 0.3;
  setTimeout(() => {
    egg1.value.classList.add('animate');
  }, 500);
};

let isEnded = $q.localStorage.getItem('isEnded');
let isEgged = $q.localStorage.getItem('isEgged');

nextTick(() => {
  if (isEnded) {
    cover.value.classList.add('invisible');
    p1.value.classList.add('invisible');
    p2.value.classList.add('invisible');
    p3.value.classList.add('invisible');
    p4.value.classList.add('invisible');
    p5.value.classList.add('invisible');
    p6.value.classList.add('invisible');
    p7.value.classList.add('invisible');
    p8.value.classList.add('invisible');
    p9.value.classList.add('invisible');
    p10.value.classList.add('invisible');
    p11.value.classList.add('invisible');
    p12.value.classList.add('invisible');
    p13.value.classList.add('invisible');
    p14.value.classList.add('invisible');
    p15.value.classList.add('invisible');
    p16.value.classList.add('invisible');
    p17.value.classList.add('invisible');
    p18.value.classList.add('invisible');
    p19.value.classList.add('invisible');
    p20.value.classList.add('invisible');
    p21.value.classList.add('invisible');
    t1.value.classList.add('invisible');
    t2.value.classList.add('invisible');
    t3.value.classList.add('invisible');
    t4.value.classList.add('invisible');
    t5.value.classList.add('invisible');
    t6.value.classList.add('invisible');
    t7.value.classList.add('invisible');
    t8.value.classList.add('invisible');
    t9.value.classList.add('invisible');
    t10.value.classList.add('invisible');
    t11.value.classList.add('invisible');
    firstEnd();
    egg1.value.classList.add('animated');
    addEventListener('click', () => {
      player.value.play();
    });
    if (isEgged) {
      egg2.value.classList.add('animate');
      egg2.value.classList.add('animated');
      setTimeout(() => {
        egg1.value.addEventListener('click', () => {
          egg1.value.classList.add('animate2');
          egg2.value.classList.add('animate2');
        });
        egg2.value.addEventListener('click', () => {
          egg1.value.classList.remove('animate2');
          egg2.value.classList.remove('animate2');
        });
      }, 4000);
    }
  } else {
    addEventListener('click', clickListener);
  }

  player.value.addEventListener('ended', () => {
    if (isEnded) {
      //第二次放完
      player.value.play();
      $q.localStorage.set('isEgged', true);
      isEgged = $q.localStorage.getItem('isEgged');
      egg1.value.classList.add('animate2');
      egg2.value.classList.add('animate');
      egg2.value.classList.add('animate2');
      egg1.value.addEventListener('click', () => {
        egg1.value.classList.add('animate2');
        egg2.value.classList.add('animate2');
      });
      egg2.value.addEventListener('click', () => {
        egg1.value.classList.remove('animate2');
        egg2.value.classList.remove('animate2');
      });
    } else {
      //第一次放完
      $q.localStorage.set('isEnded', true);
      isEnded = $q.localStorage.getItem('isEnded');
      setTimeout(() => {
        player.value.play();
        firstEnd();
      }, 2000);
    }
  });
});

const clothesURL = ref('https://www.123pan.com/s/y9W8Vv-b0QNv.html');
const signURL = ref('https://www.123pan.com/s/y9W8Vv-t0QNv.html');

const focusURL = (e: { target: { select: () => void } }) => {
  e.target.select();
  document.execCommand('copy');
};

const replay = () => {
  $q.localStorage.remove('isEnded');
  location.reload();
};

const anime = () => {
  location.href =
    'https://alist.jwyihao.top/%E7%95%AA%E5%89%A7%E5%BD%92%E6%A1%A3%EF%BC%88OneDrive%EF%BC%89/BD/%E6%9D%A5%E8%87%AA%E6%B7%B1%E6%B8%8A';
};

const gallery = () => {
  location.href = 'https://alist.jwyihao.top/29%E7%9B%B8%E5%86%8C';
};

const github = () => {
  location.href = 'https://github.com/jiwangyihao/graduation';
};
</script>

<template>
  <q-page class="row items-center justify-evenly main-page">
    <audio preload="auto" ref="player">
      <source src="/graduation/Gravity.mp3" type="audio/mp3" />
      <source src="/Gravity.mp3" type="audio/mp3" />
    </audio>
    <div class="cover" ref="cover">
      <div class="start">
        <div class="play-button" ref="playButton">
          <svg
            class="icon"
            viewBox="0 0 1024 1024"
            xmlns="http://www.w3.org/2000/svg"
            width="100%"
            height="100%"
          >
            <path
              d="M335.786667 907.946667c-33.706667 0-65.706667-8.106667-93.866667-24.32-66.56-38.4-103.253333-116.48-103.253333-219.306667V360.106667c0-103.253333 36.693333-180.906667 103.253333-219.306667 66.56-38.4 152.32-31.146667 241.92 20.48l263.253333 151.893333c89.173333 51.626667 138.666667 122.453333 138.666667 199.253334 0 76.8-49.066667 147.626667-138.666667 199.253333l-263.253333 151.893333c-51.626667 29.44-101.973333 44.373333-148.053333 44.373334z m0-727.893334c-23.04 0-43.52 5.12-61.866667 15.786667-46.08 26.453333-71.253333 84.906667-71.253333 164.266667v303.786666c0 79.36 25.173333 137.386667 71.253333 164.266667 46.08 26.88 109.226667 19.2 177.92-20.48l263.253333-151.893333c68.693333-39.68 106.666667-90.453333 106.666667-143.786667s-37.973333-104.106667-106.666667-143.786667l-263.253333-151.893333c-41.813333-23.893333-81.066667-36.266667-116.053333-36.266667z"
            ></path>
          </svg>
        </div>
        <div class="title" ref="title">
          <div class="naraku container">
            <span>に</span>
            <span>じ</span>
            <span>ゅ</span>
            <span>う</span>
            <span>き</span>
            <span>ゅ</span>
            <span>う</span>
            <span>ば</span>
            <span>ん</span>
            <span>そ</span>
            <span>つ</span>
            <span>ぎ</span>
            <span>ょ</span>
            <span>う</span>
            <span>き</span>
            <span>ね</span>
            <span>ん</span>
          </div>
          <div class="divide-line"></div>
          <div class="chinese container">
            <span>二</span>
            <span>十</span>
            <span>九</span>
            <span>班</span>
            <span>毕</span>
            <span>业</span>
            <span>纪</span>
            <span>念</span>
          </div>
        </div>
        <div class="year" ref="year">
          <div class="naraku container">
            <span>に</span>
            <span>せ</span>
            <span>ん</span>
            <span>に</span>
            <span>じ</span>
            <span>ゅ</span>
            <span>う</span>
            <span>さ</span>
            <span>ん</span>
            <span>ね</span>
            <span>ん</span>
          </div>
          <div class="chinese container">
            <span>二</span>
            <span>〇</span>
            <span>二</span>
            <span>三</span>
          </div>
        </div>
      </div>
    </div>
    <picture class="p1" ref="p1">
      <source srcset="../assets/p1.avif" type="image/avif" />
      <source srcset="../assets/p1.webp" type="image/webp" />
      <img src="../assets/p1.webp" alt="" />
    </picture>
    <section class="t1" ref="t1">
      <div>
        <div class="naraku container">
          <span>に</span>
          <span>せ</span>
          <span>ん</span>
          <span>に</span>
          <span>じ</span>
          <span>ゅ</span>
          <span>う</span>
          <span>ね</span>
          <span>ん</span>
          <span>の</span>
          <span>い</span>
          <span>ち</span>
          <span>に</span>
          <span>ち</span>
          <span>、</span>
          <span>わ</span>
          <span>た</span>
          <span>し</span>
          <span>は</span>
          <span>た</span>
          <span>ん</span>
          <span>ざ</span>
          <span>ん</span>
          <span>ち</span>
          <span>ゅ</span>
          <span>う</span>
          <span>が</span>
          <span>く</span>
          <span>の</span>
          <span>も</span>
          <span>ん</span>
          <span>を</span>
          <span>と</span>
          <span>お</span>
          <span>り</span>
          <span>ま</span>
          <span>し</span>
          <span>た</span>
        </div>
        <div class="chinese container">
          <span>二</span>
          <span>〇</span>
          <span>二</span>
          <span>〇</span>
          <span>年</span>
          <span>的</span>
          <span>一</span>
          <span>天</span>
          <span>，</span>
          <span>我</span>
          <span>走</span>
          <span>进</span>
          <span>了</span>
          <span>砀</span>
          <span>山</span>
          <span>中</span>
          <span>学</span>
          <span>的</span>
          <span>大</span>
          <span>门</span>
        </div>
      </div>
    </section>
    <section class="t2" ref="t2">
      <div>
        <div class="naraku container">
          <span>ほ</span>
          <span>う</span>
          <span>と</span>
          <span>う</span>
          <span>じ</span>
          <span>き</span>
          <span>に</span>
          <span>わ</span>
          <span>る</span>
          <span>い</span>
          <span>ク</span>
          <span>ラ</span>
          <span>ス</span>
          <span>に</span>
          <span>は</span>
          <span>い</span>
          <span>っ</span>
          <span>て</span>
          <span>し</span>
          <span>ま</span>
          <span>っ</span>
          <span>た</span>
          <span>け</span>
          <span>し</span>
          <span>き</span>
          <span>、</span>
          <span>こ</span>
          <span>う</span>
          <span>か</span>
          <span>よ</span>
          <span>う</span>
          <span>ひ</span>
          <span>に</span>
        </div>
        <div class="chinese container">
          <span>报</span>
          <span>到</span>
          <span>时</span>
          <span>走</span>
          <span>错</span>
          <span>班</span>
          <span>级</span>
          <span>的</span>
          <span>景</span>
          <span>象</span>
          <span>，</span>
          <span>恍</span>
          <span>如</span>
          <span>昨</span>
          <span>日</span>
        </div>
      </div>
    </section>
    <picture class="p2" ref="p2">
      <source srcset="../assets/p2.avif" type="image/avif" />
      <source srcset="../assets/p2.webp" type="image/webp" />
      <img src="../assets/p2.webp" alt="" />
    </picture>
    <section class="t3" ref="t3">
      <div>
        <div class="naraku container">
          <span>は</span>
          <span>ん</span>
          <span>と</span>
          <span>し</span>
          <span>の</span>
          <span>じ</span>
          <span>か</span>
          <span>ん</span>
          <span>が</span>
          <span>あ</span>
          <span>っ</span>
          <span>と</span>
          <span>い</span>
          <span>う</span>
          <span>ま</span>
          <span>に</span>
          <span>す</span>
          <span>ぎ</span>
          <span>、</span>
          <span>わ</span>
          <span>た</span>
          <span>し</span>
          <span>は</span>
          <span>あ</span>
          <span>た</span>
          <span>ら</span>
          <span>し</span>
          <span>い</span>
          <span>き</span>
          <span>ょ</span>
          <span>う</span>
          <span>し</span>
          <span>つ</span>
          <span>に</span>
          <span>は</span>
          <span>い</span>
          <span>っ</span>
          <span>た</span>
        </div>
        <div class="chinese container">
          <span>半</span>
          <span>年</span>
          <span>的</span>
          <span>时</span>
          <span>间</span>
          <span>眨</span>
          <span>眼</span>
          <span>即</span>
          <span>逝</span>
          <span>，</span>
          <span>我</span>
          <span>走</span>
          <span>进</span>
          <span>了</span>
          <span>一</span>
          <span>个</span>
          <span>新</span>
          <span>的</span>
          <span>教</span>
          <span>室</span>
        </div>
      </div>
    </section>
    <section class="t4" ref="t4">
      <div>
        <div class="naraku container">
          <span>こ</span>
          <span>こ</span>
          <span>で</span>
          <span>、</span>
          <span>わ</span>
          <span>た</span>
          <span>し</span>
          <span>た</span>
          <span>ち</span>
          <span>は</span>
          <span>で</span>
          <span>あ</span>
          <span>っ</span>
          <span>た</span>
        </div>
        <div class="chinese container">
          <span>在</span>
          <span>这</span>
          <span>里</span>
          <span>，</span>
          <span>我</span>
          <span>们</span>
          <span>相</span>
          <span>遇</span>
        </div>
      </div>
    </section>
    <picture class="p3" ref="p3">
      <source srcset="../assets/p3.avif" type="image/avif" />
      <source srcset="../assets/p3.webp" type="image/webp" />
      <img src="../assets/p3.webp" alt="" />
    </picture>
    <picture class="p4" ref="p4">
      <source srcset="../assets/p4.avif" type="image/avif" />
      <source srcset="../assets/p4.webp" type="image/webp" />
      <img src="../assets/p4.webp" alt="" />
    </picture>
    <picture class="p5" ref="p5">
      <source srcset="../assets/p5.avif" type="image/avif" />
      <source srcset="../assets/p5.webp" type="image/webp" />
      <img src="../assets/p5.webp" alt="" />
    </picture>
    <section class="t5" ref="t5">
      <div>
        <div class="naraku container">
          <span>あ</span>
          <span>の</span>
          <span>が</span>
          <span>っ</span>
          <span>し</span>
          <span>ょ</span>
          <span>う</span>
          <span>を</span>
          <span>お</span>
          <span>ぼ</span>
          <span>え</span>
          <span>て</span>
          <span>い</span>
          <span>ま</span>
          <span>す</span>
          <span>か</span>
        </div>
        <div class="chinese container">
          <span>还</span>
          <span>记</span>
          <span>得</span>
          <span>那</span>
          <span>次</span>
          <span>合</span>
          <span>唱</span>
        </div>
      </div>
    </section>
    <picture class="p6" ref="p6">
      <source srcset="../assets/p6.avif" type="image/avif" />
      <source srcset="../assets/p6.webp" type="image/webp" />
      <img src="../assets/p6.webp" alt="" />
    </picture>
    <picture class="p7" ref="p7">
      <source srcset="../assets/p7.avif" type="image/avif" />
      <source srcset="../assets/p7.webp" type="image/webp" />
      <img src="../assets/p7.webp" alt="" />
    </picture>
    <section class="t6" ref="t6">
      <div>
        <div class="naraku container">
          <span>あ</span>
          <span>の</span>
          <span>う</span>
          <span>ん</span>
          <span>ど</span>
          <span>う</span>
          <span>か</span>
          <span>い</span>
          <span>を</span>
          <span>お</span>
          <span>ぼ</span>
          <span>え</span>
          <span>て</span>
          <span>い</span>
          <span>ま</span>
          <span>す</span>
          <span>か</span>
        </div>
        <div class="chinese container">
          <span>还</span>
          <span>记</span>
          <span>得</span>
          <span>那</span>
          <span>场</span>
          <span>运</span>
          <span>动</span>
          <span>会</span>
        </div>
      </div>
    </section>
    <picture class="p8" ref="p8">
      <source srcset="../assets/p8.avif" type="image/avif" />
      <source srcset="../assets/p8.webp" type="image/webp" />
      <img src="../assets/p8.webp" alt="" />
    </picture>
    <picture class="p9" ref="p9">
      <source srcset="../assets/p9.avif" type="image/avif" />
      <source srcset="../assets/p9.webp" type="image/webp" />
      <img src="../assets/p9.webp" alt="" />
    </picture>
    <picture class="p10" ref="p10">
      <source srcset="../assets/p10.avif" type="image/avif" />
      <source srcset="../assets/p10.webp" type="image/webp" />
      <img src="../assets/p10.webp" alt="" />
    </picture>
    <picture class="p11" ref="p11">
      <source srcset="../assets/p11.avif" type="image/avif" />
      <source srcset="../assets/p11.webp" type="image/webp" />
      <img src="../assets/p11.webp" alt="" />
    </picture>
    <picture class="p12" ref="p12">
      <source srcset="../assets/p12.avif" type="image/avif" />
      <source srcset="../assets/p12.webp" type="image/webp" />
      <img src="../assets/p12.webp" alt="" />
    </picture>
    <picture class="p13" ref="p13">
      <source srcset="../assets/p13.avif" type="image/avif" />
      <source srcset="../assets/p13.webp" type="image/webp" />
      <img src="../assets/p13.webp" alt="" />
    </picture>
    <section class="t7" ref="t7">
      <div>
        <div class="naraku container">
          <span>た</span>
          <span>く</span>
          <span>さ</span>
          <span>ん</span>
          <span>、</span>
          <span>た</span>
          <span>く</span>
          <span>さ</span>
          <span>ん</span>
          <span>お</span>
          <span>ぼ</span>
          <span>え</span>
          <span>て</span>
          <span>い</span>
          <span>ま</span>
          <span>す</span>
          <span>か</span>
        </div>
        <div class="chinese container">
          <span>还</span>
          <span>记</span>
          <span>得</span>
          <span>很</span>
          <span>多</span>
          <span>，</span>
          <span>很</span>
          <span>多</span>
        </div>
      </div>
    </section>
    <picture class="p14" ref="p14">
      <source srcset="../assets/p14.avif" type="image/avif" />
      <source srcset="../assets/p14.webp" type="image/webp" />
      <img src="../assets/p14.webp" alt="" />
    </picture>
    <picture class="p15" ref="p15">
      <source srcset="../assets/p15.avif" type="image/avif" />
      <source srcset="../assets/p15.webp" type="image/webp" />
      <img src="../assets/p15.webp" alt="" />
    </picture>
    <picture class="p16" ref="p16">
      <source srcset="../assets/p16.avif" type="image/avif" />
      <source srcset="../assets/p16.webp" type="image/webp" />
      <img src="../assets/p16.webp" alt="" />
    </picture>
    <picture class="p17" ref="p17">
      <source srcset="../assets/p17.avif" type="image/avif" />
      <source srcset="../assets/p17.webp" type="image/webp" />
      <img src="../assets/p17.webp" alt="" />
    </picture>
    <picture class="p18" ref="p18">
      <source srcset="../assets/p18.avif" type="image/avif" />
      <source srcset="../assets/p18.webp" type="image/webp" />
      <img src="../assets/p18.webp" alt="" />
    </picture>
    <picture class="p19" ref="p19">
      <source srcset="../assets/p19.webp" type="image/webp" />
      <img src="../assets/p19.webp" alt="" />
    </picture>
    <section class="t8" ref="t8">
      <div>
        <div class="naraku container">
          <span>わ</span>
          <span>た</span>
          <span>し</span>
          <span>た</span>
          <span>ち</span>
          <span>は</span>
          <span>け</span>
          <span>ん</span>
          <span>き</span>
          <span>ょ</span>
          <span>に</span>
          <span>、</span>
          <span>と</span>
          <span>も</span>
          <span>に</span>
          <span>え</span>
          <span>い</span>
          <span>こ</span>
          <span>う</span>
          <span>を</span>
          <span>き</span>
          <span>ず</span>
          <span>き</span>
          <span>あ</span>
          <span>げ</span>
          <span>ま</span>
          <span>す</span>
        </div>
        <div class="chinese container">
          <span>我</span>
          <span>们</span>
          <span>脚</span>
          <span>踏</span>
          <span>实</span>
          <span>地</span>
          <span>，</span>
          <span>共</span>
          <span>铸</span>
          <span>辉</span>
          <span>煌</span>
        </div>
      </div>
    </section>
    <picture class="p20" ref="p20">
      <source srcset="../assets/p20.avif" type="image/avif" />
      <source srcset="../assets/p20.webp" type="image/webp" />
      <img src="../assets/p20.webp" alt="" />
    </picture>
    <picture class="p21" ref="p21">
      <source srcset="../assets/p21.avif" type="image/avif" />
      <source srcset="../assets/p21.webp" type="image/webp" />
      <img src="../assets/p21.webp" alt="" />
    </picture>
    <section class="t9" ref="t9">
      <div>
        <div class="naraku container">
          <span>つ</span>
          <span>い</span>
          <span>に</span>
          <span>こ</span>
          <span>の</span>
          <span>ひ</span>
          <span>が</span>
          <span>き</span>
          <span>た</span>
        </div>
        <div class="chinese container">
          <span>这</span>
          <span>一</span>
          <span>天</span>
          <span>，</span>
          <span>终</span>
          <span>于</span>
          <span>到</span>
          <span>来</span>
        </div>
      </div>
    </section>
    <section class="t10" ref="t10">
      <div>
        <div class="naraku container">
          <span>わ</span>
          <span>た</span>
          <span>し</span>
          <span>た</span>
          <span>ち</span>
          <span>は</span>
          <span>あ</span>
          <span>た</span>
          <span>ら</span>
          <span>し</span>
          <span>い</span>
          <span>た</span>
          <span>び</span>
          <span>に</span>
          <span>で</span>
          <span>か</span>
          <span>け</span>
          <span>て</span>
          <span>い</span>
          <span>ま</span>
          <span>す</span>
        </div>
        <div class="chinese container">
          <span>我</span>
          <span>们</span>
          <span>正</span>
          <span>踏</span>
          <span>上</span>
          <span>新</span>
          <span>的</span>
          <span>旅</span>
          <span>途</span>
        </div>
      </div>
    </section>
    <section class="t11" ref="t11">
      <div>
        <div class="naraku container">
          <span>こ</span>
          <span>の</span>
          <span>た</span>
          <span>び</span>
          <span>が</span>
          <span>、</span>
          <span>ほ</span>
          <span>し</span>
          <span>ぼ</span>
          <span>し</span>
          <span>に</span>
          <span>た</span>
          <span>ど</span>
          <span>り</span>
          <span>つ</span>
          <span>く</span>
          <span>こ</span>
          <span>と</span>
          <span>を</span>
          <span>ね</span>
          <span>が</span>
          <span>っ</span>
          <span>て</span>
          <span>い</span>
          <span>ま</span>
          <span>す</span>
        </div>
        <div class="chinese container">
          <span>愿</span>
          <span>此</span>
          <span>行</span>
          <span>，</span>
          <span>终</span>
          <span>抵</span>
          <span>群</span>
          <span>星</span>
        </div>
      </div>
    </section>

    <div class="egg" id="egg1" ref="egg1">
      <q-scroll-area>
        <p>啊哦</p>
        <p>还有一点小事要说哦</p>
        <p>还记得那身衣服吗</p>
        <picture>
          <source srcset="../assets/clothes.avif" type="image/avif" />
          <source srcset="../assets/clothes.webp" type="image/webp" />
          <img src="../assets/clothes.webp" alt="" />
        </picture>
        <p>说起来</p>
        <p>做这个礼物的最直接原因</p>
        <p>其实是</p>
        <p>班服上不印点什么实在遗憾呐</p>
        <p>这个设计最开始</p>
        <p>就是打算印在衣服上的说</p>
        <p>但是衣服太贵</p>
        <p>尺码面料什么的也特别麻烦</p>
        <p>于是就改成了立牌</p>
        <p>但我还是做了衣服的设计的</p>
        <p>衣服背面与立牌正面相同</p>
        <p>但是左胸处是不一样的设计哦</p>
        <picture>
          <source srcset="../assets/left.avif" type="image/avif" />
          <source srcset="../assets/left.webp" type="image/webp" />
          <img src="../assets/left.webp" alt="" />
        </picture>
        <p>如果想要的话</p>
        <p>自己去淘宝</p>
        <p>挑个喜欢的店家定做吧</p>
        <p>设计稿的链接放在下面了</p>
        <p>（直接发链接给卖家就好了）</p>
        <q-input
          v-model="clothesURL"
          outlined
          label="衣服设计稿链接"
          @focus="focusURL"
        />
        <p>衣服的底色随自己喜好就好</p>
        <p>设计的时候底色是白色来着</p>
        <p>总之自己取舍吧</p>
        <p>另外</p>
        <p>立牌的设计稿也放在下面好了</p>
        <q-input
          v-model="signURL"
          outlined
          label="立牌设计稿链接"
          @focus="focusURL"
        />
        <p>差不多就是这样啦</p>
        <p>你可以直接收藏当前页</p>
        <p>刷新会直接展示现在的卡片</p>
        <p>不会重放前面的动画</p>
        <p>当然</p>
        <p>如果你真的</p>
        <p>很想再看一遍</p>
        <q-btn color="primary" label="那就来再看一遍吧" @click="replay" />
        <p>这两天整理了一个相册来着</p>
        <q-btn color="primary" label="来看看吗" @click="gallery" />
        <p>另外提一句吧还是</p>
        <p>这个网站在 GitHub 上开源</p>
        <p>想学计算机的同学可以来看看呐</p>
        <p>（也给我点个 Star 吧）</p>
        <q-btn color="primary" label="点个 Star 吧" @click="github" />
        <p>（感觉看到的人会很少）</p>
        <p>所以给个提示好了</p>
        <p>等 BGM 再放完一遍再退出吧</p>
      </q-scroll-area>
    </div>
    <div class="egg" id="egg2" ref="egg2">
      <q-scroll-area>
        <p>阿拉阿拉</p>
        <p>你竟然把 BGM 听完了第二遍</p>
        <p>喜欢这首歌吗</p>
        <picture>
          <source srcset="../assets/cover.avif" type="image/avif" />
          <source srcset="../assets/cover.webp" type="image/webp" />
          <img src="../assets/cover.webp" alt="" />
        </picture>
        <p>我也很喜欢这首歌诶</p>
        <p>这首歌其实是</p>
        <p>《来自深渊》第二季的主题曲</p>
        <p>我很喜欢作品所表现的那种</p>
        <p>「朝闻道，夕死可矣」</p>
        <p>那样对未知的无尽探索的向往</p>
        <p>歌曲本身在传达一种「乡愁」</p>
        <p>但这亦是不存在于任何地方的</p>
        <p>是对未知中的「黄金乡」的向往</p>
        <p>所谓追忆亦是对未来的憧憬</p>
        <p>实际上设计前面的动画的时候</p>
        <p>倒是没有想太多</p>
        <p>仅仅是因为觉得节奏很合适</p>
        <p>就选了这首歌</p>
        <p>所以前奏1分钟真不是故意的啊</p>
        <p>（笑</p>
        <p>歌曲的前半部分是英语</p>
        <p>后半部分是冰岛语</p>
        <p>当然我配画面时完全没看歌词</p>
        <p>（全凭感觉）</p>
        <p>当然最后还有必不可少的</p>
        <p>作为一部</p>
        <p>第一季豆瓣9.2分</p>
        <p>第二季豆瓣9.1分</p>
        <p>的神作级作品</p>
        <p>强烈推荐去看一看</p>
        <q-btn color="primary" label="快来看吧" @click="anime" />
        <p>哦，最后还有一点小事</p>
        <p>如果你还没意识到的话</p>
        <p>就点一下这张卡片吧</p>
      </q-scroll-area>
    </div>
  </q-page>
</template>

<style lang="scss">
@font-face {
  font-family: 'naraku';
  src: url('../assets/NARAKU_MOJI.woff2') format('woff2');
}
@font-face {
  font-family: 'zcoolHappy';
  src: url('../assets/zcool_happy.woff2') format('woff2');
  font-weight: normal;
  font-style: normal;
}
body {
  overflow: hidden;
}

.naraku {
  font-family: naraku, serif;
}
.chinese {
  font-family: zcoolHappy, serif;
}

picture {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  transition: {
    property: opacity;
    duration: 4s;
    delay: 4s;
  }

  img {
    width: 80vmax;
    border: {
      color: rgba(255, 255, 255, 1);
      style: solid;
      width: 0.6vmax;
    }
    box-shadow: 0 0 3.6px rgba(0, 0, 0, 0.042), 0 0 10px rgba(0, 0, 0, 0.06),
      0 0 24.1px rgba(0, 0, 0, 0.078), 0 0 80px rgba(0, 0, 0, 0.12);
    opacity: 0;
    transform: scale(1.5) rotate(360deg);
    transition: {
      property: opacity, transform;
      duration: 4s;
    }
  }

  &.animate {
    opacity: 0;

    img {
      opacity: 1;
    }
  }
}

section {
  transition: {
    property: opacity;
    duration: 2s;
  }

  > div {
    position: absolute;
    top: 50%;
    left: 50%;
    padding: 4vmax 0;
    transform: translate(-50%, -50%) scaleX(0.01);
    opacity: 0;
    background-color: rgba(106, 21, 3, 0.4);
    border: {
      color: #1d1d1d;
      style: solid;
      top-width: 0.5vmax;
      bottom-width: 0.5vmax;
    }
    display: flex;
    align-items: center;
    transition: {
      property: opacity, transform;
      duration: 1s;
      timing-function: ease-out;
    }
  }

  .container {
    width: 90vmin;
    font-size: 4vmax;
    text-align: center;
    color: rgba(55, 22, 3, 0.8);

    &:nth-of-type(1) {
      transform: translateX(50%);
    }

    &:nth-of-type(2) {
      transform: translateX(-50%);
    }

    span {
      opacity: 0;
      transition: {
        property: opacity, color;
        duration: 1s;
        delay: calc(1s + var(--j-extra-delay)), calc(5s + var(--j-extra-delay));
      }

      @for $i from 1 through 100 {
        &:nth-child(#{$i}) {
          --j-extra-delay: calc(0.2s * #{$i});
        }
      }
    }
  }

  &.animate {
    opacity: 0;

    div {
      transform: translate(-50%, -50%);
      opacity: 1;
    }

    span {
      opacity: 1;
      color: rgba(0, 0, 0, 0);
    }
  }
}

.main-page {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-image: url('../assets/background.webp');
  background-image: -webkit-image-set(
    url('../assets/background.avif') type('image/avif'),
    url('../assets/background.webp') type('image/webp')
  );
  background-image: image-set(
    url('../assets/background.avif') type('image/avif'),
    url('../assets/background.webp') type('image/webp')
  );
  perspective: 200vmin;
  -webkit-perspective: 200vmin;
}
.cover {
  width: 100%;
  height: 100vh;
  background: rgba(0, 0, 0, 0.3);
  display: flex;
  justify-content: center;
  align-items: center;
  backdrop-filter: blur(4px);
  transition: {
    property: opacity;
    delay: 4s;
    duration: 6s;
    timing-function: ease-in;
  }

  .start {
    transition: {
      property: opacity, transform;
      duration: 8s;
      delay: 0s, 2s;
      timing-function: ease-in;
    }
  }

  &.animate {
    opacity: 0;

    .start {
      opacity: 0;
      transform: scale(1.5);
    }
  }
  .start {
    width: 90vmin;
    max-height: 80vh;
    background-position: left bottom;
    background-repeat: no-repeat;
    background-size: cover;
    background-image: url('../assets/letter-background.webp');
    background-image: -webkit-image-set(
      url('../assets/letter-background.avif') type('image/avif'),
      url('../assets/letter-background.webp') type('image/webp')
    );
    background-image: image-set(
      url('../assets/letter-background.avif') type('image/avif'),
      url('../assets/letter-background.webp') type('image/webp')
    );
    border: {
      color: #965103;
      style: solid;
      width: 0.5vmax;
      radius: 1vmax;
    }
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;

    &::before {
      background: rgba(0, 0, 0, 0.3);
      position: absolute;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
    }
    .play-button {
      position: absolute;
      width: 12vmax;
      height: 12vmax;
      border: {
        color: rgba(255, 255, 255, 0.6);
        style: solid;
        width: 0.6vmax;
        radius: 4vmax;
      }
      transition: {
        property: transform, opacity;
        duration: 16s;
      }

      .icon {
        fill: rgba(255, 255, 255, 0.6);
        transition: {
          property: transform;
          duration: 16s;
        }
      }

      &.animate .icon {
        transform: rotate(360deg) scale(0.6);
      }

      &.animate {
        transform: scale(3);
        opacity: 0;
      }
    }
  }
  .title {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;

    .container {
      width: 100%;
      flex-grow: 1;
      display: flex;
      align-items: center;
      flex-wrap: wrap;
      justify-content: space-evenly;

      span {
        margin: 2vmin 1vmin;
        font-size: 8.5vmin;
        min-height: 9vmin;
        line-height: 1ch;
        color: #965103;
        opacity: 0;
        transition: {
          property: opacity, color;
          duration: 1s;
          delay: calc(4s + var(--j-extra-delay)),
            calc(10s + var(--j-extra-delay));
        }

        @for $i from 1 through 20 {
          &:nth-child(#{$i}) {
            --j-extra-delay: calc(1s * #{$i});
          }
        }
      }

      &.chinese {
        span {
          transition-delay: calc(16s + var(--j-extra-delay)),
            calc(22s + var(--j-extra-delay));
        }
      }
    }

    .divide-line {
      width: 100%;
      height: 0.5vmax;
      background-color: #965103;
      transform: scaleX(0.001);
      opacity: 0;
      transition: {
        property: opacity, transform, background-color;
        duration: 3s;
        timing-function: ease-in;
        delay: 0s, 0s, 1.5s;
      }
    }

    &.animate {
      .divide-line {
        transform: unset;
        opacity: 1;
        background-color: rgba(0, 0, 0, 0);
      }

      .container span {
        opacity: 1;
        color: rgba(0, 0, 0, 0);
      }
    }
  }
  .year {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;

    .container {
      width: 100%;
      flex-grow: 1;
      display: flex;
      align-items: center;
      flex-wrap: wrap;
      justify-content: space-evenly;

      span {
        margin: 2vmin 1vmin;
        font-size: 8.5vmin;
        min-height: 9vmin;
        line-height: 1ch;
        color: #965103;
        opacity: 0;
        transition: {
          property: opacity, color;
          duration: 1s;
          delay: var(--j-extra-delay), calc(4s + var(--j-extra-delay));
        }

        @for $i from 1 through 20 {
          &:nth-child(#{$i}) {
            --j-extra-delay: calc(0.8s * #{$i});
          }
        }
      }

      &.chinese {
        span {
          transition-delay: calc(4s + var(--j-extra-delay)),
            calc(10s + var(--j-extra-delay));
        }
      }
    }

    &.animate {
      .container span {
        opacity: 1;
        color: rgba(0, 0, 0, 0);
      }
    }
  }
}

.p1.animate {
  img {
    transform: rotate(30deg);
  }
}

.t1 {
  transition-delay: 19s;

  .chinese span {
    transition-delay: calc(9s + var(--j-extra-delay)),
      calc(14s + var(--j-extra-delay));
  }
}

.t2 {
  transition-delay: 14s;

  .chinese span {
    transition-delay: calc(9s + var(--j-extra-delay)),
      calc(15s + var(--j-extra-delay));
  }
}

.p2 {
  img {
    width: 80vmin;
    transform: scale(1.5) rotate(-360deg);
  }

  &.animate {
    img {
      transform: rotate(-25deg);
    }
  }
}

.t3 {
  transition-delay: 16s;

  .chinese span {
    transition-delay: calc(10s + var(--j-extra-delay)),
      calc(16s + var(--j-extra-delay));
  }
}

.t4 {
  transition-delay: 11s;

  .chinese span {
    transition-delay: calc(6s + var(--j-extra-delay)),
      calc(12s + var(--j-extra-delay));
  }
}

.p3 {
  img {
    width: 70vmin;
  }

  &.animate {
    img {
      transform: rotate(25deg);
    }
  }
}

.p4 {
  img {
    width: 90vmin;
    transform: scale(1.5) rotate(-360deg);
  }

  &.animate {
    img {
      transform: rotate(-20deg);
    }
  }
}

.p5 {
  img {
    width: 110vmin;
    transform: scale(2);
    transition-duration: 4s;
  }

  &.animate {
    img {
      transform: none;
    }
  }
}

.t5 {
  transition-delay: 10s;

  .chinese span {
    transition-delay: calc(6.4s + var(--j-extra-delay)),
      calc(11s + var(--j-extra-delay));
  }
}

.p6 {
  img {
    width: 70vmin;
    transform: scale(1.5) rotate(-360deg);
  }

  &.animate {
    img {
      transform: rotate(-20deg);
    }
  }
}

.p7 {
  img {
    width: 90vmin;
  }

  &.animate {
    img {
      transform: rotate(25deg);
    }
  }
}

.t6 {
  transition-delay: 15s;

  .chinese span {
    transition-delay: calc(6.8s + var(--j-extra-delay)),
      calc(12.5s + var(--j-extra-delay));
  }
}

.p8 {
  img {
    width: 70vmin;
  }

  &.animate {
    img {
      transform: rotate(25deg) translateY(-30vmin);
    }
  }
}

.p9 {
  img {
    width: 60vmin;
    transform: scale(1.5) rotate(-360deg);
  }

  &.animate {
    img {
      transform: rotate(-20deg) translateY(30vmin);
    }
  }
}

.p10 {
  img {
    width: 60vmin;
  }

  &.animate {
    img {
      transform: rotate(25deg) translateX(30vmin);
    }
  }
}

.p11 {
  img {
    width: 60vmin;
    transform: scale(1.5) rotate(-360deg);
  }

  &.animate {
    img {
      transform: rotate(-20deg) translateX(-30vmin);
    }
  }
}

.p12 {
  img {
    width: 90vmin;
  }

  &.animate {
    img {
      transform: rotate(25deg);
    }
  }
}

.p13 {
  transition-duration: 6s;
  transition-delay: 6s;
  img {
    width: 110vmin;
    transform: scale(1.5) rotate(-180deg);
    transition-duration: 6s;
  }

  &.animate {
    img {
      transform: none;
    }
  }
}

.t7 {
  transition-delay: 19s;

  .chinese span {
    transition-delay: calc(10s + var(--j-extra-delay)),
      calc(16s + var(--j-extra-delay));
  }
}

.p14 {
  img {
    width: 90vmin;
  }

  &.animate {
    img {
      transform: rotate(25deg);
    }
  }
}

.p15 {
  img {
    width: 90vmin;
    transform: scale(1.5);
  }

  &.animate {
    img {
      transform: translateY(-10vmin);
    }
  }
}

.p16 {
  img {
    width: 90vmin;
    transform: scale(1.5) rotate(-360deg);
  }

  &.animate {
    img {
      transform: rotate(-20deg);
    }
  }
}

.p17 {
  img {
    width: 110vmin;
    transform: scale(1.5);
  }

  &.animate {
    img {
      transform: none;
    }
  }
}

.p18 {
  img {
    width: 130vmin;
    transform: scale(1.5) rotate(60deg);
  }

  &.animate {
    img {
      transform: none;
    }
  }
}

.p19 {
  transition-duration: 6s;
  transition-delay: 8s;
  img {
    width: 130vmin;
    transform: scale(1.5) rotate(60deg);
    transition-duration: 7s;
  }

  &.animate {
    img {
      transform: none;
    }
  }
}

.t8 {
  transition-delay: 10s;

  .naraku span {
    transition-delay: calc(0s + var(--j-extra-delay)),
      calc(3s + var(--j-extra-delay));
  }

  .chinese span {
    transition-delay: calc(6s + var(--j-extra-delay)),
      calc(10s + var(--j-extra-delay));
  }
}

.p20 {
  img {
    width: 130vmin;
    transform: scale(1.5) rotate(60deg);
  }

  &.animate {
    img {
      transform: none;
    }
  }
}

.p21 {
  transition-duration: 6s;
  transition-delay: 8s;
  img {
    width: 130vmin;
    transform: scale(1.5) rotate(-60deg);
    transition-duration: 7s;
  }

  &.animate {
    img {
      transform: none;
    }
  }
}

.t9 {
  transition-delay: 12s;

  .naraku span {
    transition-delay: calc(1s + var(--j-extra-delay)),
      calc(4s + var(--j-extra-delay));
  }

  .chinese span {
    transition-delay: calc(5s + var(--j-extra-delay)),
      calc(10s + var(--j-extra-delay));
  }
}

.t10 {
  transition-delay: 10.5s;

  .naraku span {
    transition-delay: calc(1s + var(--j-extra-delay)),
      calc(4s + var(--j-extra-delay));
  }

  .chinese span {
    transition-delay: calc(6s + var(--j-extra-delay)),
      calc(11s + var(--j-extra-delay));
  }
}

.t11 {
  transition-delay: 20s;

  .naraku span {
    transition-delay: calc(1s + var(--j-extra-delay)),
      calc(5s + var(--j-extra-delay));
  }

  .chinese span {
    transition-delay: calc(10s + var(--j-extra-delay)),
      calc(16s + var(--j-extra-delay));
  }
}

.egg {
  height: 80vh;
  width: calc(60vmin + 20vmax - 20vw);
  position: fixed;
  top: 50%;
  left: 50%;
  background-color: rgba(245, 222, 179, 0.5);
  border: {
    width: 1vmax;
    color: wheat;
    style: solid;
    radius: 1vmax;
  }
  backdrop-filter: blur(1vmin);
  transition: {
    property: transform, opacity;
    duration: 4s;
    timing-function: ease-out;
  }
  backface-visibility: hidden;

  .q-scrollarea {
    width: 100%;
    height: 100%;

    .q-scrollarea__content {
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: calc((60vmin + 20vmax - 20vw) / 36) 0;

      > * {
        transform: scale(0.9);
        opacity: 0;
        transition: {
          property: transform, opacity;
          duration: 3s;
          delay: var(--j-extra-delay);
          timing-function: ease-out;
        }

        @for $i from 1 through 200 {
          &:nth-child(#{$i}) {
            --j-extra-delay: calc(0.75s * #{$i});
          }
        }
      }
    }
  }

  p {
    font-family: zcoolHappy, serif;
    font-size: calc((60vmin + 20vmax - 20vw) / 16);
    line-height: 1.5ch;
    text-align: center;
    color: rgba(55, 22, 3, 0.8);
    margin: calc((60vmin + 20vmax - 20vw) / 30) 0;
  }

  picture {
    opacity: 1;
    position: static;
    transform: none;

    img {
      width: 60%;
      transform: translateX(33.3%);
      opacity: 1;
      border-radius: 1vmax;
    }
  }

  label {
    margin: calc((60vmin + 20vmax - 20vw) / 30)
      calc((60vmin + 20vmax - 20vw) / 8);
    width: -webkit-fill-available;
  }

  &.animate,
  &#egg1.animate {
    transform: translate(-50%, -50%);
    opacity: 1;

    .q-scrollarea__content > * {
      transform: none;
      opacity: 1;
    }
  }
}

#egg1 {
  transform: translate(-50%, -50%) rotate3d(3, 4, 0, 90deg);
  opacity: 0;
  z-index: 100;
}

#egg2 {
  transform: translate(-50%, -50%) rotateY(180deg);
}

.animate2 {
  &#egg1.egg {
    transform: translate(-50%, -50%) rotateY(180deg);
  }

  &#egg2 {
    transform: translate(-50%, -50%) rotateY(360deg);
    z-index: 100;
  }
}

.animated .q-scrollarea__content > * {
  transition-delay: 4s !important;
  transition-duration: 4s !important;
  transition-timing-function: ease-in-out;
}
</style>
