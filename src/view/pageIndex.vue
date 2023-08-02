<template>
  <div class="continer">
    <div class="title">
      <!-- <div class="header">
        <div class="lang">
          <span class="cn">中/</span>
          EN
        </div>
      </div> -->
      <div class="content">
        <img style="width:100px" class="titleImg1" src="@/assets/img/title.png">
        <img class="indexlogo" src="@/assets/img/logo_black.png">
        <div class="indexTitle">
          AI Drives the World and Expands Human Limits

        </div>
      </div>
    </div>
    <div class="allBox">

      <div class="subTitle">
        <div class="left">
          <div class="top">
            <div>Next-generation ADAS/AD System Solution</div>
            <div>Provider based on 3D Visual Understanding</div>
          </div>
          <div class="bottom">PhiGent Robotics</div>
        </div>
        <div class="right">
          <div>Leading the Value Creation of </div>
          <div>Autonomous Driving and Robotics</div>
        </div>
      </div>
      <div class="technology">
        <span class="sub">Technology</span>
        <div class="type">Vision-centered Perception Paradigm</div>

        <video class="videoBox" src="@/assets/video/technology.mp4" loop="loop" muted="muted" controls="controls">
          <source src="@/assets/video/technology.mp4" type="video/mp4">
        </video>
        <!-- <video  width="1280" height="573" controls src="@/assets/video/technology.mp4"></video> -->
        <div class="step">
          <div class="box">
            <img v-if="active == 0" class="point" src="@/assets/img/red_point.png">
            <img v-else class="point" src="@/assets/img/black_point.png">
            <div class="name1" hover="check" :class="active == 0 ? 'check' : ''">BEVDet
              <div @click="active = 0" class="box"></div>
            </div>
          </div>
          <div class="box">
            <img class="strip" src="@/assets/img/strip.png">
          </div>
          <div class="box">
            <img v-if="active == 1" class="point" src="@/assets/img/red_point.png">
            <img v-else class="point" src="@/assets/img/black_point.png">
            <div class="name" :class="active == 1 ? 'check' : ''">BEVDet4D
              <div @click="active = 1" class="box"></div>
            </div>
          </div>
          <div class="box">
            <img class="strip" src="@/assets/img/strip.png">
          </div>
          <div class="box">
            <img v-if="active == 2" class="point" src="@/assets/img/red_point.png">
            <img v-else class="point" src="@/assets/img/black_point.png">
            <div class="name" :class="active == 2 ? 'check' : ''">BEVerse
          <div @click="active = 2" class="box"></div>
        </div>
          </div>
          <div class="box">
            <img class="strip" src="@/assets/img/strip.png">
          </div>
          <div class="box">
            <img v-if="active == 3" class="point" src="@/assets/img/red_point.png">
            <img v-else class="point" src="@/assets/img/black_point.png">
            <div class="name" :class="active == 3 ? 'check' : ''">TPVFormer
          <div @click="active = 3" class="box"></div>
        </div>
          </div>
          <div class="box">
            <img class="mini" src="@/assets/img/mini_point.png">
          </div>
          <div class="box">
            <img class="mini" src="@/assets/img/mini_point.png">
          </div>
          <div class="box">
            <img class="mini" src="@/assets/img/mini_point.png">
          </div>
          <div class="box">
            <img class="mini" src="@/assets/img/mini_point.png">
          </div>
        </div>
        <!-- <div class="stepText">
        <div class="name" hover="check" :class="active == 0 ? 'check' : ''">BEVDet
          <div @click="active = 0" class="box"></div>
        </div>
        <div class="name" :class="active == 1 ? 'check' : ''">BEVDet4D
          <div @click="active = 1" class="box"></div>
        </div>
        <div class="name" :class="active == 2 ? 'check' : ''">BEVerse
          <div @click="active = 2" class="box"></div>
        </div>
        <div class="name" :class="active == 3 ? 'check' : ''">TPVFormer
          <div @click="active = 3" class="box"></div>
        </div>
        <div></div>
      </div> -->
        <div class="stepContent" v-if="active == 0">
          <div class="stepTitle">
            <a class="link" href="https://arxiv.org/abs/2112.11790" target="	_blank">BEVDet</a>：A New Paradigm of
            Vision-centered
            Autonomous Driving 3D Perception
          </div>
          <div class="tips">Through the vision-centered perception system, it can restore the three-dimensional structure
            of
            the whole
            space, and directly perceive and understand the environment. BEVDet has achieved the world's first (2021、2022)
            in nuScenes.</div>
        </div>
        <div class="stepContent" v-if="active == 1">
          <div class="stepTitle">
            <a class="link" href="https://arxiv.org/pdf/2203.17054.pdf" target="	_blank">BEVDet4D</a>: A New Paradigm of
            Vision-centered Autonomous Driving in the Spatial-Temporal 4D Space based on BEVDet
          </div>
          <div class="tips">BEVDet4D elevates the scalable BEVDet paradigm from the spatial-only 3D working space to the
            spatial-temporal 4D working space. By incorporating spatial-temporal 4D space modeling for autonomous driving
            target detection, it significantly enhances accuracy and robustness. BEVDet4D has achieved the world's first
            (2022) in nuScenes.</div>
        </div>
        <div class="stepContent" v-if="active == 2">
          <div class="stepTitle">
            <a class="link" href="https://arxiv.org/abs/2205.09743" target="	_blank">BEVerse</a>: Vision-centered Unified
            Giant Perception Framework
          </div>
          <div class="tips">BEVerse Integrated perception architecture combined with 3D Perception, Prediction and Local
            Road Structure Mapping. BEVerse has achieved the optimal performance of three tasks in nuScenes.</div>
        </div>
        <div class="stepContent" v-if="active == 3">
          <div class="stepTitle">
            <a class="link" href="https://arxiv.org/abs/2302.07817" target="	_blank">TPVFormer</a>: Vision-centric
            Semantic
            Occupancy Prediction Framework
          </div>
          <div class="tips">Vision-centric semantic occupancy prediction framework, which achieves comparable performance
            with LiDAR-based methods on the LiDAR segmentation task on nuScenes.</div>
        </div>
        <div class="type">End-to-end Scalable Capabilities</div>
        <div class="typeTip">
          Autonomous driving solutions are powered by end-to-end scalable capabilities from sensor layers to perception
          and
          planning & control layer.
        </div>
        <img class="car" src="@/assets/img/car.png">
        <div class="type">Data Closed-Loop Automation</div>
        <div class="cycle">
          <img class="cycleimg1" src="@/assets/img/cycle.png">
        </div>
        <el-row class="dataVideos" :gutter="0">
          <el-col style="margin-right: 10px;" :xs="24" :sm="12" :md="12" :lg="12" :xl="12">
            <video class="videoBoxs" src="@/assets/video/data1.mp4" loop="loop" muted="muted" controls="controls">
              <source src="@/assets/video/data1.mp4" type="video/mp4">
            </video>
            <div class="videoname">4D Labeling for video sequences</div>
          </el-col>
          <el-col :xs="24" :sm="12" :md="12" :lg="12" :xl="12">
            <video class="videoBoxs" src="@/assets/video/data2.mp4" loop="loop" muted="muted" controls="controls">
            </video>
            <div class="videoname">Automatically case mining</div>
          </el-col>
        </el-row>
        <!-- <div class="dataVideos">
        <div>
          <video class="videoBoxs" width="625" height="307" src="@/assets/video/data1.mp4" loop="loop" muted="muted"
            controls="controls">
            <source src="@/assets/video/data1.mp4" type="video/mp4">
          </video>
          <div class="videoname">4D Labeling for video sequences</div>
        </div>
        <div>
          <video class="videoBoxs" width="625" height="307" src="@/assets/video/data2.mp4" loop="loop" muted="muted"
            controls="controls">
          </video>
          <div class="videoname">Automatically case mining</div>
        </div>
      </div> -->
        <div class="typeTips">
          Autonomous driving solutions are powered by end-to-end scalable capabilities from sensor layers to perception
          and
          planning & control layer.
        </div>
        <div class="type">Heterogeneous Computing Development Paradigm</div>
        <img style="width:100%" class="four" src="@/assets/img/four.png">
        <ul class="ulBox">
          <li>Well layered and decoupled architecture designing of algorithm, inference, and multi-platform adaptor can
            significantly reduce their interdependence</li>
          <li>Unified algorithm and software architecture designed for heterogenous platforms</li>
          <li>Typical new platform porting time is 1~3 months</li>
        </ul>

      </div>
      <div class="solutions">
        <span class="sub">Solutions</span>
        <el-row class="boxs" :gutter="0">
          <el-col class="box1" :xs="24" :sm="24" :md="24" :lg="12" :xl="12">
            <div class="titbox">
              <div class="tit">PhiGo</div>
              <div class="sub">
                Intelligent Driving Solution
              </div>
            </div>
            <div class="content">
              With visual 3D understanding as the core, we insist on software and hardware co-optimization and AI
              data-driven, and do not rely on high-definition maps and LiDAR to create intelligent driving solutions with
              high performance, high cost-efficency and growth iteration.
            </div>
            <div class="videos" @click="playVideos(0)">
              <img class="icons" src="@/assets/img/solution_icon.png">
              <div class="play">watch video</div>
            </div>
          </el-col>
          <el-col class="box2" :xs="24" :sm="24" :md="24" :lg="12" :xl="12">
            <div class="titbox">

              <div class="tit">PhiGo Bi-Series</div>
              <div class="sub">
                Intelligent Driving Solution
              </div>
            </div>
            <div class="content">
              With self-developed inertial sensor stereo cameras as core, we built up a 3D vision perception capability
              for
              everything, creating a highly differentiated and cost-effective intelligent driving solution.
            </div>
            <div class="videos" @click="playVideos(1)">
              <img class="icons" src="@/assets/img/solution_icon.png">
              <div class="play">watch video</div>
            </div>
          </el-col>
          <el-col class="box3" :xs="24" :sm="24" :md="24" :lg="12" :xl="12">
            <div class="titbox">
              <div class="tit">PhiMotion</div>
              <div class="sub">
                Intelligent Chassis Perception Solution
              </div>
            </div>
            <div class="content">
              3D road information reconstruction with precise 3D perception and dense pixel-level point-cloud, contributes
              to various intelligent chassic applications, such as 'Magic-Carpet' Suspension, 3D Transparent Chassis,
              Driving-Mode Adaptive Adjustment, etc.
            </div>
            <div class="videos" @click="playVideos(2)">
              <img class="icons" src="@/assets/img/solution_icon.png">
              <div class="play">watch video</div>
            </div>
          </el-col>
          <el-col class="box4" :xs="24" :sm="24" :md="24" :lg="12" :xl="12">
            <div class="titbox">

              <div class="tit">PhiVision</div>
              <div class="sub">
                Intelligent Driving Vision Perception Products
              </div>
            </div>
            <div class="content">
              With the world's leading CV algorithm and self-developed AI data-driven closed-loop automation, we offer
              standardized vision 3D perception products with industry-leading performance and fast-paced interation, to
              empower the implementation of intelligent driving system.
            </div>
            <div class="videos" @click="playVideos(3)">
              <img class="icons" src="@/assets/img/solution_icon.png">
              <div class="play">watch video</div>
            </div>
          </el-col>
        </el-row>

      </div>
      <div class="massProduction">
        <div class="sub">Mass Production</div>
        <div class="content">
          <div> Achieve large-scale mass production in the shortest possible time, </div>
          <div>and promote vision products and intelligent driving solutions at the same time.</div>
        </div>
        <img class="img" src="@/assets/img/massProduction.png">
      </div>
      <div class="foundingTeam">
        <div class="sub">Founding Team</div>
        <div class="content">
          <div>More than 10 years’ experience in AI algorithm and chip R&D, mass production and service, </div>
          <div>multiple entrepreneurial successes in ADAS/AD domain.</div>
        </div>
        <div class="team">
          <div @click="changeActive(0)" :class="userActive == 0 ? 'userCheck' : 'userNoCheck'">
            <div class="user">
              <img class="img" src="@/assets/img/user1.png">
              <div class="name">Yi SHAN, PhD</div>
              <div class="titBox">
                <div class="tit">CEO, Co-Founder</div>
                <div class="icons">
                  <img v-if="userActive == 0" class="icon" src="@/assets/img/check_icon.png">
                  <img v-else class="icon" src="@/assets/img/user_icon.png">
                </div>
              </div>
            </div>
          </div>
          <div @click="changeActive(1)" :class="userActive == 1 ? 'userCheck' : 'userNoCheck'">
            <div class="user">
              <img class="img" src="@/assets/img/user2.png">
              <div class="name">DALONG DU, PhD</div>
              <div class="titBox">
                <div class="tit">CTO, Co-Founder</div>
                <div class="icons">
                  <img v-if="userActive == 1" class="icon" src="@/assets/img/check_icon.png">
                  <img v-else class="icon" src="@/assets/img/user_icon.png">
                </div>
              </div>
            </div>
          </div>
          <div @click="changeActive(2)" :class="userActive == 2 ? 'userCheck' : 'userNoCheck'">
            <div class="user">
              <img class="img" src="@/assets/img/user3.png">
              <div class="name">JINGXIU LIU </div>
              <div class="titBox">
                <div class="tit2">
                  <div>Partner, Head of Marketing and </div>
                  <div>
                    Business Development</div>
                </div>
                <div class="icons">
                  <img v-if="userActive == 2" class="icon" src="@/assets/img/check_icon.png">
                  <img v-else class="icon" src="@/assets/img/user_icon.png">
                </div>
              </div>
            </div>
          </div>
          <el-collapse-transition>
            <ul class="userInfo" v-if="userActive == 0">
              <li>Founded an AI chip startup, DeePhi Tech, acquired by Xilinx with $300 million. As a co-founder and CTO,
                he
                developed the first AI chip in China-Tingtao (28nm 8Tops computational capability), several design wins in
                ADAS.</li>
              <li>Former Vice President of Xilinx and Corporate Vice President of AMD, Head of Xilinx AI R&D. Led the team
                to launch the AMD (Xilinx) Vitis AI product line, has supported more than 10 world-level OEMs and Tier-1s,
                and has rich experience in research and development of ADAS technology and customer service.</li>
              <li>10# employee of Horizon Robotics, and work as FPGA tech lead for ADAS application.</li>
              <li>Undergraduate, Master and PhD in EE at Tsinghua University, Joint PhD at Imperial College London.</li>
              <li>The first completer of the first prize of technical invention in the 2017 Science and Technology Award
                of
                the China Computer Federation (CCF).</li>
            </ul>
            <ul class="userInfo" v-if="userActive == 1">
              <li>The former head of R&D of an AI company, former Algorithms director of Horizon Robotics, former
                architect
                of Baidu Research Institute.</li>
              <li>PhD in Innovation Leading Engineering, Tsinghua University; Master, Institute of Computing Technology,
                Chinese Academy of Sciences. </li>
              <li>R&D and scale implementation of the first Chinese AI chip product solution. R&D and scale implementation
                of AI2B software and hardware products for smart cities. </li>
              <li>Two consecutive times won the Baidu highest honor for Engineer-"Baidu Million Dollars Top Award":
                PaddlePaddle, large-scale image search landing. </li>
              <li>Lead the team to achieve world-class results in AI competitions such as MSCOCO and FRVT.</li>
              <li>Leading entrepreneurial talents in Gusu, Suzhou, Jiangsu Province, and Xiangcheng District, Suzhou,
                Jiangsu Province.</li>
            </ul>
            <ul class="userInfo" v-if="userActive == 2">
              <li>Former Xilinx AI global marketing director, responsible for market expansion in industries such as
                vehicles, medical, data center, etc., with cumulative total product cycle income of over 100 million US
                dollars, provided FPGA-based AI acceleration solutions to global head car manufacturers and mainstream
                parts
                suppliers during Xilinx. </li>
              <li>Former business VP of DeePhi, responsible for the implementation of business strategy, supporting the
                company's acquisition by Xilinx for hundreds of millions of dollars. </li>
              <li>Former business director of Nokia (China), more than ten years of experience in market expansion and
                industrial chain integration in the communications industry.</li>
              <li>Bachelor and Master of Electronic Engineering, Tsinghua University; Master of Business Administration,
                School of Economics and Management, Tsinghua University.</li>
            </ul>
          </el-collapse-transition>

        </div>
      </div>
      <div class="ourInvestors">
        <div class="sub">Our Investors</div>
        <div class="content">
          <div>Obtain investment from top venture capital and industry leaders.</div>
          <div> PhiGent Robotics is developing rapidly and continuously increasing in value.</div>
        </div>
        <div class="logos">
          <el-row style="width: 100%;" :gutter="0">
            <el-col style="min-height: 60px;" :xs="8" :sm="8" :md="8" :lg="3" :xl="3">
              <img class="logo1" src="@/assets/img/logo1.png">
            </el-col>
            <el-col style="min-height: 60px;" :xs="8" :sm="8" :md="8" :lg="3" :xl="3">
              <img class="logo2" src="@/assets/img/logo2.png">
            </el-col>
            <el-col style="min-height: 60px;" :xs="8" :sm="8" :md="8" :lg="3" :xl="3">
              <img class="logo3" src="@/assets/img/logo3.png">
            </el-col>
            <el-col style="min-height: 60px;" :xs="8" :sm="8" :md="8" :lg="3" :xl="3">
              <img class="logo4" src="@/assets/img/logo4.png">
            </el-col>
            <el-col style="min-height: 60px;" :xs="8" :sm="8" :md="8" :lg="3" :xl="3">
              <img class="logo5" src="@/assets/img/logo5.png">
            </el-col>
            <el-col style="min-height: 60px;" :xs="8" :sm="8" :md="8" :lg="3" :xl="3">
              <img class="logo6" src="@/assets/img/logo6.png">
            </el-col>
            <el-col style="min-height: 60px;" :xs="8" :sm="8" :md="8" :lg="3" :xl="3">
              <img class="logo7" src="@/assets/img/logo7.png">
            </el-col>
          </el-row>
        </div>
      </div>
    </div>
    <div class="footer">
      <div class="top">
        <el-row style="width: 100%;" :gutter="0">
          <el-col :xs="8" :sm="8" :md="8" :lg="8" :xl="8">
            <div class="left">
              <img class="logo" src="@/assets/img/logo_white.png">
              <div>Easy Mobility for Everyone</div>
            </div>
          </el-col>
          <el-col :xs="16" :sm="16" :md="16" :lg="16" :xl="16">
            <div class="right">
              <div class="emails">
                <span>Investment cooperation：invest@phigent.ai</span>
                <span>Business cooperation：bd@phigent.ai</span>
                <span>Other cooperation：mkt@phigent.ai</span>
              </div>
              <div class="address">
                <div>Business Address：</div>
                <div>
                  <div>25F, Tower B, Tsinghua Tongfang High-tech Plaza, No.1 Wangzhuang Road, Haidian District, Beijing , China</div>
                  <div>Room 5DE, WESTLINK Tower C, No.2337 Gudai Road, Minhang District, Shanghai</div>
                  <div>Room 4307, Building 2, Euro America Financial City, Cangqian Street, Yuhang District, Hangzhou City, Zhejiang Provinc</div>
                </div>
              </div>
            </div>
          </el-col>
        </el-row>
      </div>
      <div class="bottom">© Beijing PhiGent Robotics Technology Co., Ltd ｜Beijing ICP prepared No.2022009455-1</div>

    </div>
    <el-dialog :visible.sync="videoVisible" width="80%" :title="title" @close="closeDialog">
      <div style="height:600px;">
        <video v-if="curSrc == 0" width="100%" height="100%" src="@/assets/video/solution1.mp4" controls="controls"
          autoplay loop="loop" ref="video0"></video>
        <video v-if="curSrc == 1" width="100%" height="100%" src="@/assets/video/solution2.mp4" controls="controls"
          autoplay loop="loop" ref="video1"></video>
        <video v-if="curSrc == 2" width="100%" height="100%" src="@/assets/video/solution3.mp4" controls="controls"
          autoplay loop="loop" ref="video2"></video>
        <video v-if="curSrc == 3" width="100%" height="100%" src="@/assets/video/solution4.mp4" controls="controls"
          autoplay loop="loop" ref="video3"></video>
      </div>
    </el-dialog>
  </div>
</template>
  
<script>
export default {
  data() {
    return {
      active: 0,
      userActive: null,
      videoVisible: false,
      curSrc: '',
      title: ''
    }
  },
  methods: {

    changeActive(item) {
      if (this.userActive == null || this.userActive != item) {
        this.userActive = item
      } else if (this.userActive == item) {
        this.userActive = null
      }
    },
    playVideos(item) {
      this.videoVisible = true;
      this.curSrc = item;
      switch (item) {
        case 0:
          this.title = 'PhiGo'
          break;
        case 1:
          this.title = 'PhiGo Bi-Series'
          break;
        case 2:
          this.title = 'PhiMotion'
          break;
        case 3:
          this.title = 'PhiVision'
          break;
      }
      this.$refs['video' + item].play();//播放视频
    },
    closeDialog() {
      this.$refs['video' + this.curSrc].pause();//终止视频
      this.videoVisible = false;
    },
  }
}
</script>
<style lang="scss" scoped>
/* page {
  font-size: 16px;
} */

.continer {
  min-width: 1220px;
  box-sizing: border-box;
  max-width: 100%;
  width: 100%;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.allBox {
  max-width: 1440px;
}

.en-flex {
  display: flex;
  flex-direction: column;
}

/* .header {
  box-sizing: border-box;
  max-width: 90rem;
  position: absolute;
  top: 2.5rem;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
  padding: 0 5rem;

  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;

  .logo {
    width: 110px;
    height: 37px;
  }

  .lang {
    color: #000;
    font-family: Source Han Sans CN;
    font-size: 16px;
    font-style: normal;
    font-weight: 350;
    line-height: 17.631px;
  }

  .cn {
    color: rgba(0, 0, 0, 0.50);
    text-align: center;
    font-family: Source Han Sans CN;
    font-size: 16px;
    font-style: normal;
    font-weight: 350;
    line-height: 17.631px;
  }
} */

.videoBox,
.videoBoxs {
  background-color: #000;
}

.videoBox {
  width: 100%;
  height: 500px;
  /* max-height: 573rpx; */
}

.videoBoxs {
  width: 100%;
}

.title {
  min-width: 1220px;
  /* max-width: 1440px; */
  position: relative;
  width: 100%;
  box-sizing: border-box;
  /* width: 90rem; */
  /* min-height: 45.0625rem; */
  flex-shrink: 0;
  background: #F6F7FA;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  /* background: url('@/assets/img/title.png') no-repeat 100%/100%; */


  .content {
    min-width: 1220px;
    max-width: 1440px;
    width: 100%;
    color: #000;
    text-align: center;
    box-sizing: border-box;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 1.3125rem;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    /* 1.96875rem */
    letter-spacing: 0.01969rem;
    position: relative;

    .titleImg1 {
      width: 100%;
      max-width: 1440px;
      min-width: 1220px;
    }

    .indexTitle {
      /* margin-top: 47px; */
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
      top: 47px;
    }

    .indexlogo {
      position: absolute;
      top: 2.5rem;
      left: 2.5rem;
      width: 6.875rem;
      height: 2.3125rem;
    }
  }
}

.subTitle {
  width: 100%;
  height: 16.1875rem;
  padding: 0 6.88rem;
  box-sizing: border-box;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-start;

  .left {
    padding-top: 5rem;
    text-align: left;

    .top {
      color: #141414;
      font-family: Alibaba PuHuiTi 3.0;
      font-size: 1.5625rem;
      font-style: normal;
      font-weight: 500;
      line-height: 168%;
      /* 2.625rem */
      text-transform: capitalize;
      margin-bottom: 4.31rem;
    }

    .bottom {
      color: rgba(0, 0, 0, 0.40);
      font-family: PingFang SC;
      font-size: 1rem;
      font-style: normal;
      font-weight: 400;
      line-height: 162%;
      /* 1.62rem */
      letter-spacing: 0.02rem;
    }
  }

  .right {
    text-align: left;
    padding-top: 5.56rem;
    color: rgba(0, 0, 0, 0.60);
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 1rem;
    font-style: normal;
    font-weight: 400;
    line-height: 162%;
    /* 1.62rem */
    letter-spacing: 0.02rem;
  }
}

.technology {
  margin-top: 7.5rem;
  width: 100%;
  min-width: 1220px;
  padding: 0 5rem;
  box-sizing: border-box;

  .sub {
    color: #000;
    text-align: center;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 2.375rem;
    font-style: normal;
    font-weight: 500;
    line-height: 150%;
    /* 3.5625rem */

  }

  .type {
    text-align: left;
    margin-bottom: 1.87rpx;
    color: #000;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 2rem;
    font-style: normal;
    font-weight: 500;
    line-height: 150%;
    /* 3rem */
    letter-spacing: 0.01rem;
    margin-bottom: 1.87rem;
  }

  .step {
    width: 100%;
    height: 4.31rem;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    margin-bottom: 72px;

    .check {
      color: #E60012;
    }

    .box {
      display: flex;
      justify-content: center;
      align-content: center;
      flex-direction: column;
      height: 100%;
      position: relative;

      .name1 {
        position: absolute;
        left: 0;
        bottom: -1.44rem;
      }

      .name {
        position: absolute;
        left: -1.5rem;
        bottom: -1.44rem;
      }

      .box {
        cursor: pointer;
        content: '';
        width: 100%;
        height: 7rem;
        background-color: transparent;
        position: absolute;
        left: 0;
        top: -4rem;
        z-index: 999;
      }


    }

    .point {
      display: flex;
      flex-direction: row;
      width: 1rem;
      height: 1rem;

    }


    .strip {
      width: 100%;
      /* width: 20.3125rem; */
      height: 0.25rem;
      padding: 0 0.62rem;
      box-sizing: border-box;
    }

    .mini {
      margin-left: 2.38rem;
      width: 0.5rem;
      height: 0.5rem;
    }
  }

  /* .stepText {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    color: #000;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 1.5rem;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 0.0075rem;
    margin-bottom: 1.87rem;

    .check {
      color: #E60012;
    }

    .name {
      position: relative;
      margin-right: 10px;
    }

    .box {
      content: '';
      width: 100%;
      height: 7rem;
      background-color: transparent;
      position: absolute;
      left: 0;
      top: -4rem;
      z-index: 999;
    }
  } */

  .stepContent {
    text-align: left;
    margin-bottom: 3.75rem;
    min-height: 80px;

    .stepTitle {
      color: #000;
      text-align: justify;
      font-family: Alibaba PuHuiTi 3.0;
      font-size: 1.25rem;
      font-style: normal;
      font-weight: 500;
      line-height: 175.5%;
      /* 2.19375rem */
      letter-spacing: 0.00625rem;

      .link {
        color: #000;
      }
    }
  }

  .typeTip {
    color: #000;
    text-align: justify;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 1.25rem;
    font-style: normal;
    font-weight: 400;
    line-height: 175.5%;
    /* 2.19375rem */
    letter-spacing: 0.00625rem;
    margin-bottom: 1.87rem;
  }

  .car {
    width: 100%;
    /* height: 32.625rem; */
    flex-shrink: 0;
    margin-bottom: 3.75rem;

  }

  .cycle {
    box-sizing: border-box;
    width: 100%;
    max-width: 100vw;
    /* height: 35.125rem; */
    flex-shrink: 0;
    background: #F5F6FB;
    padding: 0 10.34rem;
    margin-bottom: 1.75rem;
    display: flex;
    flex: row;
    justify-content: center;
    align-items: center;


  }

  .cycleimg1 {
    width: 100%;
    /* height: 27.9375rem; */
    /* flex-shrink: 0; */
  }

  .dataVideos {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 100%;

    .videoname {
      margin-top: 1rem;
      margin-bottom: 1.87rem;
      text-align: left;
      color: #000;
      font-family: Alibaba PuHuiTi 3.0;
      font-size: 1.5rem;
      font-style: normal;
      font-weight: 400;
      line-height: 150%;
      /* 2.25rem */
      letter-spacing: 0.0075rem;
    }

  }

  .typeTips {
    color: #000;
    text-align: justify;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 1.25rem;
    font-style: normal;
    font-weight: 400;
    line-height: 175.5%;
    /* 2.19375rem */
    letter-spacing: 0.00625rem;
    margin-bottom: 5rem;
  }

  .four {
    width: 100%;
    max-width: 100vw;
    /* height: 28rem; */
    flex-shrink: 0;
    margin-bottom: 1.87rem;
  }

  .ulBox {
    text-align: left;
    color: #000;
    text-align: justify;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 1.25rem;
    font-style: normal;
    font-weight: 400;
    line-height: 175.5%;
    /* 2.19375rem */
    letter-spacing: 0.00625rem;
    margin-bottom: 7.5rem;
  }
}

.solutions {
  width: 100%;
  min-width: 1220px;
  box-sizing: border-box;

  .sub {
    color: #000;
    text-align: center;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 2.375rem;
    font-style: normal;
    font-weight: 500;
    line-height: 150%;
    /* 3.5625rem */
  }

  .boxs {
    width: 100%;
    min-width: 1220px;
    box-sizing: border-box;
    margin-top: 2.5rem;
    /* displa
    y: flex;
    flex-direction: row;
    flex-wrap: wrap;
    width: 100%; */

    .box1 {
      background: url('@/assets/img/solution1.png') no-repeat 100%, rgba(0, 0, 0, 0.30);
    }

    .box2 {
      background: url('@/assets/img/solution2.png') no-repeat 100%, rgba(0, 0, 0, 0.30);
    }

    .box3 {
      background: url('@/assets/img/solution3.png') no-repeat 100%, rgba(0, 0, 0, 0.30);
    }

    .box4 {
      background: url('@/assets/img/solution4.png') no-repeat 100%, rgba(0, 0, 0, 0.30);
    }

    .box1,
    .box2,
    .box3,
    .box4 {
      /* width: 720px;
      height: 510px; */
      /* width: 45rem;
      height: 32.25rem; */
      height: 31rem;
      padding: 7.06rem 5rem 7.12rem;
      box-sizing: border-box !important;
      color: #fff;
      text-align: left;
      display: flex;
      flex-direction: column;
      justify-content: space-between;

      .titbox {
        .tit {
          color: var(--unnamed, #FFF);
          font-family: Alibaba PuHuiTi 3.0;
          font-size: 2rem;
          font-style: normal;
          font-weight: 700;
          line-height: 150%;
          /* 3rem */
          text-align: left;
        }

        .sub {
          color: var(--unnamed, #FFF);
          font-family: Alibaba PuHuiTi 3.0;
          font-size: 1.625rem;
          font-style: normal;
          font-weight: 400;
          line-height: 150%;
          text-align: left;
        }

      }



      .content {
        margin: 1.5rem 0;
        color: rgba(255, 255, 255, 0.70);
        text-align: justify;
        font-family: Alibaba PuHuiTi 3.0;
        font-size: 1rem;
        font-style: normal;
        font-weight: 400;
        line-height: 190%;
        /* 1.9rem */
        letter-spacing: 0.01rem;
      }

      .videos {
        display: flex;
        flex-direction: row;
        align-content: center;
        cursor: pointer;

        .icons {
          width: 2.25rem;
          height: 2.25rem;
        }

        .play {
          display: flex;
          flex-direction: column;
          justify-content: center;
          margin-left: 1rem;
          color: var(--unnamed, #FFF);
          text-align: center;
          font-family: Alibaba PuHuiTi 3.0;
          font-size: 1rem;
          font-style: normal;
          font-weight: 400;
          line-height: 150%;
          /* 1.5rem */
        }
      }
    }
  }
}

.massProduction {
  min-width: 1220px;
  width: 100%;
  margin-top: 7.5rem;
  padding: 0 5rem;
  box-sizing: border-box;

  .sub {
    color: #000;
    text-align: center;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 2.375rem;
    font-style: normal;
    font-weight: 500;
    line-height: 150%;
    /* 3.5625rem */
  }

  .content {
    margin: 1.88rem 0;
    color: #000;
    text-align: center;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 1.125rem;
    font-style: normal;
    font-weight: 400;
    line-height: 169.5%;
    /* 1.90688rem */
    letter-spacing: 0.00563rem;

  }

  .img {
    width: 100%;
    /* height: 31.9375rem; */
  }
}

.foundingTeam {
  min-width: 1220px;
  margin-top: 7.5rem;
  padding: 0 5rem;
  box-sizing: border-box;
  width: 100%;

  .sub {
    color: #000;
    text-align: center;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 2.375rem;
    font-style: normal;
    font-weight: 500;
    line-height: 150%;
    /* 3.5625rem */

  }

  .content {
    margin: 1.87rem 0 2.31rem;
    color: #000;
    text-align: center;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 1.125rem;
    font-style: normal;
    font-weight: 400;
    line-height: 169.5%;
    /* 1.90688rem */
    letter-spacing: 0.00563rem;

  }

  .team {
    display: flex;
    flex-direction: row;
    align-content: center;
    justify-content: space-between;
    flex-wrap: wrap;
    margin: 0 5.5rem;

    .userCheck {
      cursor: pointer;
      box-sizing: border-box;
      width: 17.875rem;
      height: 27.5rem;
      flex-shrink: 0;
      background: #22406F;
      margin-bottom: 3.87rem;
      padding: 0.81rem 0.88rem 0 0.75rem;

      .name {
        color: #fff !important;
      }

      .tit,
      .tit2 {
        color: rgba(255, 255, 255, 0.80) !important;
      }
    }

    .userNoCheck {
      cursor: pointer;
      width: 17.875rem;
      height: 27.5rem;
      box-sizing: border-box;

      flex-shrink: 0;
      background: #fff;
      margin-bottom: 3.87rem;
      padding: 0.81rem 0.88rem 0 0.75rem;

      .name {
        color: #141414 !important;
      }

      .tit,
      .tit2 {
        color: rgba(0, 0, 0, 0.80) !important;
      }
    }

    .userNoCheck:hover {
      background: #22406F;

      .name {
        color: #fff !important;
      }

      .tit,
      .tit2 {
        color: rgba(255, 255, 255, 0.80) !important;
      }

    }

    .userInfo {
      color: #000;
      text-align: justify;
      font-family: Alibaba PuHuiTi 3.0;
      font-size: 1.125rem;
      font-style: normal;
      font-weight: 400;
      line-height: 218%;
      /* 2.4525rem */
      letter-spacing: 0.00563rem;
      text-align: left;
    }

    .user {
      width: 16.25rem;
      height: 24.9375rem;
      flex-shrink: 0;
      display: flex;
      flex-direction: column;
      align-items: flex-start;


      .img {
        width: 16.25rem;
        height: 19.125rem;
        flex-shrink: 0;
      }

      .name {
        margin-top: 1rem;
        color: #000;
        text-align: justify;
        font-family: Alibaba PuHuiTi 3.0;
        font-size: 1.4375rem;
        font-style: normal;
        font-weight: 500;
        line-height: 181.5%;
        /* 2.60906rem */
        text-transform: capitalize;
      }

      .titBox {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: flex-start;

        .tit {
          color: rgba(0, 0, 0, 0.80);
          font-family: Alibaba PuHuiTi 3.0;
          font-size: 1.25rem;
          font-style: normal;
          font-weight: 400;
          line-height: 181.5%;
          letter-spacing: 0.00625rem;
          text-transform: capitalize;
          text-align: left;

        }

        .tit2 {
          color: rgba(0, 0, 0, 0.80);
          font-family: Alibaba PuHuiTi 3.0;
          font-size: 0.875rem;
          font-style: normal;
          font-weight: 400;
          line-height: 181.5%;
          letter-spacing: 0.00438rem;
          text-transform: capitalize;
          text-align: left;

        }

        .icons {
          height: 100%;
          display: flex;
          flex-direction: row;
          justify-content: center;
          align-items: flex-start;
          padding-top: 4px;

          .icon {
            width: 1.5rempx;
            height: 1.5rempx;
          }
        }


      }
    }
  }
}

.ourInvestors {
  min-width: 1220px;
  margin-top: 7.5rem;
  padding: 0 5rem;
  box-sizing: border-box;
  width: 100%;

  .sub {
    color: #000;
    text-align: center;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 2.375rem;
    font-style: normal;
    font-weight: 500;
    line-height: 150%;
    /* 3.5625rem */
    /* 3.5625rem */

  }

  .content {
    margin: 1.87rem 0 5.09rem;
    color: #000;
    text-align: center;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 1.125rem;
    font-style: normal;
    font-weight: 400;
    line-height: 169.5%;
    /* 1.90688rem */
    letter-spacing: 0.00563rem;

  }

  .logos {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height: 45px;

    .logo1 {
      width: 6rem;
      height: 2.625rem;
    }

    .logo2 {
      width: 7.25rem;
      height: 2.8125rem;
    }

    .logo3 {
      width: 6.5625rem;
      height: 2.1875rem;
    }

    .logo4 {
      width: 6.75rem;
      height: 2.25rem;
    }

    .logo5 {
      width: 9.625rem;
      height: 1.8125rem;
    }

    .logo6 {
      width: 6.0625rem;
      height: 1.4375rem;
    }

    .logo7 {
      width: 7.4375rem;
      height: 2.75rem;
    }
  }
}

.footer {
  min-width: 1220px;
  margin-top: 7.25rem;
  padding: 4.06rem 5.25rem 0.62rem 7.5rem;
  background-color: #000;
  width: 100%;
  height: 19.875rem;
  flex-shrink: 0;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;

  .top {
    width: 100%;
    max-width: 1440px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    color: rgba(236, 236, 236, 1);

    .left {
      box-sizing: border-box;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-content: center;
      color: #FFF;
      font-family: Alibaba PuHuiTi 3.0;
      font-size: 0.875rem;
      font-style: normal;
      font-weight: 500;
      line-height: 150%;
      /* 1.3125rem */
      letter-spacing: 0.02625rem;
      margin-right: 1rem;
      text-align: left;

      .logo {
        width: 9.9375rem;
        height: 3.3515rem;
        flex-shrink: 0;
        margin-bottom: 1.59rem;

      }
    }

    .right {
      flex: 1;
      color: #ECECEC;
      font-variant-numeric: lining-nums proportional-nums;
      font-family: Alibaba PuHuiTi 3.0;
      font-size: 0.75rem;
      font-style: normal;
      font-weight: 400;
      line-height: 150%;
      /* 1.125rem */
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      text-align: left;

      .emails {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        margin-bottom: 2.06rem;
      }

      .address {
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        align-items: flex-start;
        text-align: left;
      }
    }
  }

  .bottom {
    max-width: 1440px;
    color: #9F9FA0;
    font-variant-numeric: lining-nums proportional-nums;
    font-family: Alibaba PuHuiTi 3.0;
    font-size: 0.625rem;
    font-style: normal;
    font-weight: 400;
    line-height: 140%;
    /* 0.875rem */

  }

}

/* h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  } */</style>
  