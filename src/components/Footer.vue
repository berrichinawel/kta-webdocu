<template>
  <div class="footer">
    <audio ref="audioElm" class="audio" autoplay loop src="@/assets/sound/audioKta.mp3"></audio>
    <div class="footer__icones">
      <div @click="toogleFullScreen()" class="footer__screen">
        <svg
          v-if="isFullScreen"
          class="smallScreenIcon"
          width="25"
          height="25"
          viewBox="0 0 25 25"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g clip-path="url(#clip0)">
            <path
              d="M8.30018 0.869812H15.9653V8.78424L24.0239 8.89143V16.6408H15.9653V24.749H8.30018V16.6408H0.151794L0.223177 8.78424H8.30018V0.869812Z"
              fill="#393939"
            />
            <path
              d="M8.29974 0.771973C7.99824 0.771973 7.75427 1.01594 7.75427 1.31744V8.40838H0.663392C0.361892 8.40832 0.11792 8.6523 0.11792 8.9538C0.11792 9.2553 0.361892 9.49927 0.663392 9.49927H8.29974C8.60124 9.49927 8.84522 9.2553 8.84522 8.9538V1.31744C8.84522 1.01594 8.60124 0.771973 8.29974 0.771973ZM15.9361 9.49927H23.5724C23.8739 9.49927 24.1179 9.2553 24.1179 8.9538C24.1179 8.6523 23.8739 8.40832 23.5724 8.40832H16.4816V1.31744C16.4816 1.01594 16.2376 0.771973 15.9361 0.771973C15.6346 0.771973 15.3906 1.01594 15.3906 1.31744V8.9538C15.3907 9.2553 15.6346 9.49927 15.9361 9.49927ZM23.5725 16.0447H15.9361C15.6346 16.0447 15.3906 16.2887 15.3906 16.5902V24.2266C15.3906 24.5281 15.6346 24.772 15.9361 24.772C16.2376 24.772 16.4816 24.5281 16.4816 24.2266V17.1356H23.5725C23.874 17.1356 24.118 16.8916 24.118 16.5901C24.118 16.2886 23.874 16.0447 23.5725 16.0447ZM8.29974 16.0447H0.663392C0.361892 16.0447 0.11792 16.2887 0.11792 16.5901C0.11792 16.8916 0.361892 17.1356 0.663392 17.1356H7.75432V24.2266C7.75432 24.5281 7.9983 24.772 8.2998 24.772C8.6013 24.772 8.84527 24.5281 8.84527 24.2266V16.5901C8.84522 16.2887 8.60124 16.0447 8.29974 16.0447Z"
              fill="url(#a)"
            />
            <path
              d="M8.29974 16.0447H0.663392C0.361892 16.0447 0.11792 16.2887 0.11792 16.5902C0.11792 16.8916 0.361892 17.1356 0.663392 17.1356H7.75432V24.2266C7.75432 24.5281 7.9983 24.772 8.2998 24.772C8.6013 24.772 8.84527 24.5281 8.84527 24.2266V16.5902C8.84522 16.2887 8.60124 16.0447 8.29974 16.0447Z"
              fill="#FFCE1F"
            />
            <path
              d="M15.9361 9.49927H23.5724C23.8739 9.49927 24.1179 9.2553 24.1179 8.9538C24.1179 8.6523 23.8739 8.40832 23.5724 8.40832H16.4816V1.31744C16.4816 1.01594 16.2376 0.771973 15.9361 0.771973C15.6346 0.771973 15.3906 1.01594 15.3906 1.31744V8.9538C15.3907 9.2553 15.6346 9.49927 15.9361 9.49927Z"
              fill="#FFCE1F"
            />
          </g>
          <defs>
            <linearGradient
              id="a"
              x1="35.8766"
              y1="-13.5383"
              x2="-35.1774"
              y2="60.0761"
              gradientUnits="userSpaceOnUse"
            >
              <stop stop-color="#FFCE1F" />
              <stop offset="0.333819" stop-color="#FAF0CE" />
              <stop offset="0.569189" stop-color="#F5BC87" stop-opacity="0.651083" />
              <stop offset="1" stop-color="white" stop-opacity="0" />
            </linearGradient>
            <clipPath id="clip0">
              <rect width="24" height="24" fill="white" transform="translate(0.11792 0.771973)" />
            </clipPath>
          </defs>
        </svg>
        <svg
          v-else
          class="fullScreenIcon"
          width="25"
          height="25"
          viewBox="0 0 25 25"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g clip-path="url(#clip0)">
            <rect x="0.11792" y="0.771973" width="24" height="24.0001" fill="#393939" />
            <path
              d="M8.29974 0.771973H0.663392C0.361892 0.771973 0.11792 1.01594 0.11792 1.31744V8.9538C0.11792 9.2553 0.361892 9.49927 0.663392 9.49927C0.964892 9.49927 1.20881 9.2553 1.20881 8.9538V1.86287H8.29974C8.60124 1.86287 8.84522 1.61889 8.84522 1.31739C8.84522 1.01589 8.60124 0.771973 8.29974 0.771973ZM23.5725 0.771973H15.9361C15.6346 0.771973 15.3906 1.01594 15.3906 1.31744C15.3906 1.61894 15.6346 1.86292 15.9361 1.86292H23.027V8.9538C23.027 9.2553 23.271 9.49927 23.5725 9.49927C23.874 9.49927 24.118 9.2553 24.118 8.9538V1.31744C24.1179 1.01594 23.874 0.771973 23.5725 0.771973ZM23.5725 16.0447C23.271 16.0447 23.027 16.2887 23.027 16.5902V23.6811H15.9361C15.6346 23.6811 15.3906 23.9251 15.3906 24.2266C15.3906 24.5281 15.6346 24.772 15.9361 24.772H23.5724C23.8739 24.772 24.1179 24.5281 24.1179 24.2266V16.5901C24.1179 16.2887 23.874 16.0447 23.5725 16.0447ZM8.29974 23.6811H1.20881V16.5901C1.20881 16.2886 0.964841 16.0447 0.663341 16.0447C0.361841 16.0447 0.11792 16.2887 0.11792 16.5901V24.2265C0.11792 24.528 0.361892 24.772 0.663392 24.772H8.29974C8.60124 24.772 8.84522 24.528 8.84522 24.2265C8.84522 23.9251 8.60124 23.6811 8.29974 23.6811Z"
              fill="url(#a2)"
            />
            <path
              d="M8.29974 23.6811H1.20881V16.5902C1.20881 16.2887 0.964841 16.0447 0.663341 16.0447C0.361841 16.0447 0.11792 16.2887 0.11792 16.5902V24.2265C0.11792 24.528 0.361892 24.772 0.663392 24.772H8.29974C8.60124 24.772 8.84522 24.528 8.84522 24.2265C8.84522 23.9251 8.60124 23.6811 8.29974 23.6811Z"
              fill="#FFCE1F"
            />
            <path
              d="M15.9362 1.86286L23.0271 1.86286L23.0271 8.95379C23.0271 9.25529 23.2711 9.49927 23.5726 9.49927C23.8741 9.49927 24.118 9.25524 24.118 8.95379L24.118 1.31744C24.118 1.01594 23.874 0.77197 23.5725 0.77197L15.9362 0.771969C15.6347 0.771969 15.3907 1.01594 15.3907 1.31744C15.3907 1.61889 15.6347 1.86286 15.9362 1.86286Z"
              fill="#FFCE1F"
            />
          </g>
          <defs>
            <linearGradient
              id="a2"
              x1="35.8766"
              y1="-13.5383"
              x2="-35.1774"
              y2="60.0761"
              gradientUnits="userSpaceOnUse"
            >
              <stop stop-color="#FFCE1F" />
              <stop offset="0.333819" stop-color="#FAF0CE" />
              <stop offset="0.569189" stop-color="#F5BC87" stop-opacity="0.651083" />
              <stop offset="1" stop-color="white" stop-opacity="0" />
            </linearGradient>
            <clipPath id="clip0">
              <rect width="24" height="24" fill="white" transform="translate(0.11792 0.771973)" />
            </clipPath>
          </defs>
        </svg>
      </div>
      <div @click="toggleIsMute()" class="footer__sound">
        <svg
          v-if="isMute"
          class="soundOffIcon"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g clip-path="url(#clip0)">
            <path
              d="M0.518066 7.51698H5.44314L10.7622 3.03519L12.486 2.24718V21.8489L10.7622 20.9131L5.44314 16.1851L0.518093 15.9388L0.518066 7.51698Z"
              fill="#393939"
            />
            <path
              d="M20.6284 11.5555L23.8698 8.3142C24.0435 8.14042 24.0435 7.85953 23.8698 7.68575C23.696 7.51198 23.4151 7.51198 23.2413 7.68575L20 10.9271L16.7587 7.68575C16.5849 7.51198 16.304 7.51198 16.1302 7.68575C15.9564 7.85953 15.9564 8.14042 16.1302 8.3142L19.3715 11.5555L16.1302 14.7969C15.9564 14.9706 15.9564 15.2515 16.1302 15.4253C16.2169 15.512 16.3307 15.5555 16.4444 15.5555C16.5582 15.5555 16.672 15.512 16.7587 15.4253L20 12.184L23.2413 15.4253C23.328 15.512 23.4418 15.5555 23.5555 15.5555C23.6693 15.5555 23.7831 15.512 23.8698 15.4253C24.0435 15.2515 24.0435 14.9706 23.8698 14.7969L20.6284 11.5555Z"
              fill="url(#b)"
            />
            <path
              d="M12.624 1.95555C12.1907 1.71022 11.6769 1.71822 11.2507 1.97511C11.2302 1.98711 11.2107 2.00133 11.1929 2.01644L5.17067 7.11111H0.444444C0.198667 7.11111 0 7.30978 0 7.55555V16C0 16.1182 0.0466667 16.2311 0.130222 16.3142C0.213778 16.3973 0.326222 16.4444 0.444444 16.4444L5.16 16.4422L11.1791 21.9711C11.2013 21.9916 11.2253 22.0093 11.2507 22.0244C11.4693 22.1564 11.7116 22.2227 11.9538 22.2227C12.1836 22.2222 12.4129 22.1631 12.624 22.044C13.068 21.7933 13.3333 21.3356 13.3333 20.8196V3.18044C13.3333 2.66444 13.068 2.20666 12.624 1.95555ZM12.4444 20.8196C12.4444 21.0111 12.348 21.1796 12.1871 21.2707C12.1182 21.3093 11.9436 21.384 11.7427 21.2822L5.77778 15.8027V13.7778C5.77778 13.532 5.57911 13.3333 5.33333 13.3333C5.08755 13.3333 4.88889 13.532 4.88889 13.7778V15.5538L0.888889 15.5556V8H4.88889V9.77778C4.88889 10.0236 5.08755 10.2222 5.33333 10.2222C5.57911 10.2222 5.77778 10.0236 5.77778 9.77778V7.76178L11.7356 2.72178C11.94 2.61422 12.1178 2.69066 12.1871 2.72978C12.348 2.82089 12.4444 2.98889 12.4444 3.18044V20.8196Z"
              fill="url(#b1)"
            />
            <path
              d="M0.444444 7.11108H5.17067L5.77778 7.76175V9.77775C5.77778 10.0235 5.57911 10.2222 5.33333 10.2222C5.08756 10.2222 4.88889 10.0235 4.88889 9.77775V7.99997H0.888889V15.5555L4.88889 15.5538V13.7778C4.88889 13.532 5.08756 13.3333 5.33333 13.3333C5.57911 13.3333 5.77778 13.532 5.77778 13.7778V15.8026L5.16 16.4422L0.444444 16.4444C0.326222 16.4444 0.213778 16.3973 0.130222 16.3142C0.0466667 16.2311 0 16.1182 0 16V7.55553C0 7.30975 0.198667 7.11108 0.444444 7.11108Z"
              fill="#FFCE1F"
            />
            <path
              d="M4.88892 8.00025V13.778C4.88892 14.0238 5.08758 13.3336 5.33336 13.3336C5.57914 13.3336 5.77781 14.0238 5.77781 13.778V7.76202L4.88892 8.00025Z"
              fill="#FFCE1F"
            />
            <path
              d="M5.77781 15.8029V13.778C5.77781 13.5322 5.57914 13.3336 5.33336 13.3336C5.08758 13.3336 4.88892 13.5322 4.88892 13.778V15.554L5.77781 15.8029Z"
              fill="#FFCE1F"
            />
          </g>
          <defs>
            <linearGradient
              id="b"
              x1="27.9197"
              y1="2.78528"
              x2="4.23482"
              y2="27.324"
              gradientUnits="userSpaceOnUse"
            >
              <stop stop-color="#FFCE1F" />
              <stop offset="0.333819" stop-color="#FAF0CE" />
              <stop offset="0.569189" stop-color="#F5BC87" stop-opacity="0.651083" />
              <stop offset="1" stop-color="white" stop-opacity="0" />
            </linearGradient>
            <linearGradient
              id="b1"
              x1="19.8659"
              y1="-10.4141"
              x2="-36.3279"
              y2="27.5521"
              gradientUnits="userSpaceOnUse"
            >
              <stop stop-color="#FFCE1F" />
              <stop offset="0.333819" stop-color="#FAF0CE" />
              <stop offset="0.569189" stop-color="#F5BC87" stop-opacity="0.651083" />
              <stop offset="1" stop-color="white" stop-opacity="0" />
            </linearGradient>
            <clipPath id="clip0">
              <rect width="24" height="24" fill="white" />
            </clipPath>
          </defs>
        </svg>
        <svg
          v-else
          class="soundOnIcon"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M0.935669 7.46895H5.86074L11.1798 2.98716L12.9036 2.19915V21.8008L11.1798 20.8651L5.86074 16.137L0.935696 15.8908L0.935669 7.46895Z"
            fill="#393939"
          />
          <path
            d="M13.103 1.57445C12.6528 1.31981 12.1199 1.32812 11.6775 1.59475C11.6563 1.60721 11.636 1.62197 11.6176 1.63765L5.36686 6.92563H0.461308C0.206205 6.92563 0 7.13183 0 7.38693V16.1518C0 16.2745 0.0484373 16.3917 0.135163 16.4779C0.221889 16.5642 0.3386 16.6131 0.461308 16.6131L5.35578 16.6108L11.6033 22.3495C11.6263 22.3707 11.6513 22.3891 11.6775 22.4048C11.9045 22.5418 12.1559 22.6106 12.4073 22.6106C12.6458 22.6101 12.8839 22.5487 13.103 22.4251C13.5638 22.1649 13.8392 21.6898 13.8392 21.1542V2.84582C13.8392 2.31024 13.5638 1.83509 13.103 1.57445ZM12.9166 21.1542C12.9166 21.353 12.8165 21.5279 12.6495 21.6224C12.578 21.6626 12.3967 21.7401 12.1882 21.6344L5.997 15.947V13.8452C5.997 13.5901 5.7908 13.3839 5.53569 13.3839C5.28059 13.3839 5.07439 13.5901 5.07439 13.8452V15.6886L0.922616 15.6905V7.84824H5.07439V9.69347C5.07439 9.94858 5.28059 10.1548 5.53569 10.1548C5.7908 10.1548 5.997 9.94858 5.997 9.69347V7.60098L12.1808 2.36975C12.3935 2.25811 12.5776 2.33746 12.6495 2.37805C12.8165 2.47262 12.9166 2.64746 12.9166 2.84582V21.1542Z"
            fill="url(#c)"
          />
          <path
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M5.36685 6.9256H0.461308C0.206205 6.9256 0 7.1318 0 7.38691V16.1518C0 16.2745 0.0484373 16.3916 0.135163 16.4779C0.221889 16.5642 0.3386 16.6131 0.461308 16.6131L5.35578 16.6108L5.997 15.9469V13.8452V9.69345V7.60095L5.36685 6.9256ZM5.07439 13.8452V15.6886L0.922616 15.6904V7.84821H5.07439V9.69345V13.8452Z"
            fill="#FFCE1F"
          />
          <path
            d="M5.0744 7.84827V9.69351C5.0744 9.94861 5.28061 10.1548 5.53571 10.1548C5.79081 10.1548 5.99702 9.94861 5.99702 9.69351V7.60101L5.0744 7.84827Z"
            fill="#FFCE1F"
          />
          <path
            d="M5.99702 15.947V13.8453C5.99702 13.5902 5.79081 13.384 5.53571 13.384C5.28061 13.384 5.0744 13.5902 5.0744 13.8453V15.6887L5.99702 15.947Z"
            fill="#FFCE1F"
          />
          <path
            d="M17.8974 3.2596C17.6561 3.17794 17.3941 3.30711 17.312 3.54837C17.2303 3.78918 17.3595 4.05166 17.6007 4.13377C20.8765 5.24599 23.0774 8.31461 23.0774 11.7698C23.0774 15.2218 20.8806 18.2908 17.6114 19.4063C17.3705 19.4884 17.2414 19.7504 17.324 19.9922C17.3895 20.1836 17.5685 20.3045 17.7604 20.3045C17.8097 20.3045 17.86 20.2966 17.9094 20.2795C21.5518 19.0372 23.9995 15.6176 23.9995 11.7703C24 7.9188 21.5477 4.49913 17.8974 3.2596Z"
            fill="url(#c2)"
          />
          <path
            d="M19.8482 11.7693C19.8482 9.0144 17.9988 6.55563 15.3509 5.78986C15.105 5.7202 14.8509 5.85998 14.7798 6.10539C14.7092 6.34989 14.8499 6.60591 15.0953 6.67649C17.3507 7.32832 18.926 9.42266 18.926 11.7693C18.926 14.116 17.3507 16.2103 15.0953 16.8622C14.8504 16.9327 14.7092 17.1888 14.7798 17.4333C14.8384 17.6353 15.0225 17.7668 15.2231 17.7668C15.2656 17.7668 15.3085 17.7608 15.3509 17.7488C17.9993 16.983 19.8482 14.5243 19.8482 11.7693Z"
            fill="url(#c3pO)"
          />
          <defs>
            <linearGradient
              id="c"
              x1="20.6196"
              y1="-11.2646"
              x2="-37.7063"
              y2="28.1422"
              gradientUnits="userSpaceOnUse"
            >
              <stop stop-color="#FFCE1F" />
              <stop offset="0.333819" stop-color="#FAF0CE" />
              <stop offset="0.569189" stop-color="#F5BC87" stop-opacity="0.651083" />
              <stop offset="1" stop-color="white" stop-opacity="0" />
            </linearGradient>
            <linearGradient
              id="c2"
              x1="27.2881"
              y1="-6.94264"
              x2="-8.04831"
              y2="7.45316"
              gradientUnits="userSpaceOnUse"
            >
              <stop stop-color="#FFCE1F" />
              <stop offset="0.333819" stop-color="#FAF0CE" />
              <stop offset="0.569189" stop-color="#F5BC87" stop-opacity="0.651083" />
              <stop offset="1" stop-color="white" stop-opacity="0" />
            </linearGradient>
            <linearGradient
              id="c3pO"
              x1="22.3403"
              y1="-1.38005"
              x2="-3.83127"
              y2="10.1184"
              gradientUnits="userSpaceOnUse"
            >
              <stop stop-color="#FFCE1F" />
              <stop offset="0.333819" stop-color="#FAF0CE" />
              <stop offset="0.569189" stop-color="#F5BC87" stop-opacity="0.651083" />
              <stop offset="1" stop-color="white" stop-opacity="0" />
            </linearGradient>
          </defs>
        </svg>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      isMute: false,
      isFullScreen: false,
      full: this.$attrs,
    };
  },
  props: {
    screen: {
      type: HTMLDivElement,
      default: () => {},
    },
  },
  methods: {
    toggleIsMute() {
      var audio = this.$refs.audioElm;
      this.isMute = !this.isMute;
      if (this.isMute) {
        audio.pause();
      } else {
        audio.play();
      }
    },
    toogleFullScreen() {
      this.isFullScreen = !this.isFullScreen;

      if(this.isFullScreen){
        document.documentElement.requestFullscreen()
      }
      else {
        document.exitFullscreen()
      }
    },
  },
  mounted() {
    this.$refs.audioElm.muted = false;
    this.$refs.audioElm.volume = 0.1;
  }
};
</script>

<style lang="scss" scoped>
.footer {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  bottom: 0;
  width: 100%;
  position: fixed;
  background: linear-gradient(
    0deg,
    rgba(0, 0, 0, 0.7) 0%,
    rgba(5, 5, 5, 0.56472) 39.03%,
    rgba(5, 5, 5, 0.378) 63.23%,
    rgba(26, 26, 26, 0) 105.55%,
    rgba(26, 26, 26, 0) 105.56%
  );
  height: 48px;

  @include tablet-portrait {
    height: 93px;
  }
}

.footer__icones {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  padding-top: 10px;
}

.footer__play {
  display: none;

  @include tablet-portrait {
    display: none;
    width: 20px;
    height: 20px;
  }
}

.footer__screen {
  display: none;
  transition: all 0.2s ease-in-out;
  &:hover {
    filter: drop-shadow(0px 0px 8px $yellow);
    transform: scale(1.3);
  }

  @include tablet-portrait {
    cursor: pointer;
    display: flex;
    margin-right: 35px;
  }

  svg {
    @include tablet-portrait {
      width: 30px;
      height: 30px;
    }
  }
}

.footer__sound {
  margin-right: 20px;
  cursor: pointer;
  transition: all 0.2s ease-in-out;
  &:hover {
    filter: drop-shadow(0px 0px 8px $yellow);
    transform: scale(1.3);
  }

  @include tablet-portrait {
    margin-right: 35px;
  }

  svg {
    @include tablet-portrait {
      width: 35px;
      height: 35px;
    }
  }
}
</style>
