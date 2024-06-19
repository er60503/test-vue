<template>
  <v-app>
    <div class="main">
      <v-app-bar app color="black" v-if="isMobile">
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
        <v-toolbar-title></v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn text href="https://www.youtube.com">
          <img src="/img/shopicon/mail-48.png" alt="YouTube" width="24">
          YouTube
        </v-btn>
        <v-btn text href="#github">
          <v-icon left>mdi-github</v-icon>
          GitHub
        </v-btn>
        <v-btn text href="#profilo">
          <v-icon left>mdi-file-document</v-icon>
          Resume
        </v-btn>
      </v-app-bar>

      <v-navigation-drawer color="#FFF8F0" app v-model="drawer" right class="d-md-none">
        <v-list dense>
          <v-list-item href="https://www.youtube.com">
            <v-list-item-icon>
              <v-icon>mdi-youtube</v-icon>
            </v-list-item-icon>
            <v-list-item-title>YouTube</v-list-item-title>
          </v-list-item>
          <v-list-item href="#github">
            <v-list-item-icon>
              <v-icon>mdi-github</v-icon>
            </v-list-item-icon>
            <v-list-item-title>GitHub</v-list-item-title>
          </v-list-item>
          <v-list-item href="#profilo">
            <v-list-item-icon>
              <v-icon>mdi-file-document</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Resume</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>

      <v-main>
        <div class="main-container" >
          <div id="main-container-inner" class="main-container-inner hover" >
            <div id="svg-wrapper"  >
              <!-- Original SVG on top left -->
                 <svg class="svg-top-left" width="300" height="300" xmlns="http://www.w3.org/2000/svg" v-if="!isMobile" >
            <defs>
              <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="100%">
                <stop offset="0%" :stop-color="color1"></stop>
                <stop offset="50%" :stop-color="color2"></stop>
                <stop offset="100%" :stop-color="color1"></stop>
              </linearGradient>
            </defs>
            <path fill="url(#grad1)" d="M8 0h292l-20 20H25a5 5 0 0 0-5 5v255L0 300V8a8 8 0 0 1 8-8Z"></path>
          </svg>

          <!-- New SVG for Projects -->
          <svg class="svg-projects" width="100" height="100" xmlns="http://www.w3.org/2000/svg" v-if="!isMobile" >
            <defs>
              <linearGradient id="grad1-small" x1="0%" y1="0%" x2="100%" y2="100%">
                <stop offset="0%" stop-color="rgb(88,76,168)"></stop>
                <stop offset="50%" stop-color="rgb(131,194,83)"></stop>
                <stop offset="100%" stop-color="rgb(88,76,168)"></stop>
              </linearGradient>
            </defs>
            <path fill="url(#grad1-small)" d="M2.67 0H97.33L90 6.67H8.33A1.67 1.67 0 0 0 6.67 8.33V85L0 100V2.67A2.67 2.67 0 0 1 2.67 0Z"></path>
          </svg>

          <!-- New SVG on bottom right -->
          <svg class="svg-bottom-right" width="300" height="500" xmlns="http://www.w3.org/2000/svg" v-if="!isMobile" >
            <defs>
              <linearGradient id="grad2" x1="0%" y1="0%" x2="100%" y2="100%">
                <stop offset="0%" :stop-color="color1"></stop>
                <stop offset="50%" :stop-color="color2"></stop>
                <stop offset="100%" :stop-color="color1"></stop>
              </linearGradient>
            </defs>
            <path fill="url(#grad2)" d="M8 0h292l-20 20H25a5 5 0 0 0-5 5v255L0 300V8a8 8 0 0 1 8-8Z"></path>
          </svg>

              <div class="toolbar-style d-none d-md-flex">
                <div class="yt">
                  <a href="https://www.youtube.com">
                    <img src="/img/shopicon/mail-48.png" alt="">
                  </a>
                </div>
                <div class="git">
                  <a href="#github">
                    <img src="/img/shopicon/github.png" alt="">
                  </a>
                </div>
                <div class="res">
                  <a href="#profilo">
                    <img src="/img/shopicon/resume.png" alt="">
                  </a>
                </div>
              </div>

              <main class="project-overview">
                <div class="main-massage">
                  <span>
                    <p class="text-name">
                      My name is Ian Dunkerley, I'm a front-end developer based in Torquay, Devon, UK.
                      <br> I have developed many types of front-ends from well know DJ applications to
                      <br> Ecommerce booking platforms.
                    </p>
                    <p class="text-about">I'm passionate about cutting-edge, pixel-perfect, beautiful interfaces and intuitively
                      <br> implemented UX.
                    </p>
                  </span>
                </div>
                <div class="main-projects" v-if="!isMobile" >
                  <h2>Projects</h2>
                  <div class="project-wrapper">
                    <div class="ecommerce">
                      <a rel="noopener" target="_blank" href="https://domposer.com">
                        <span>ecommerce</span>
                      </a>
                    </div>
                    <div class="travel">
                      <a rel="noopener" target="_blank" href="https://bayjs.org">
                        <span>travel</span>
                      </a>
                    </div>
                    <div class="shop">
                      <a rel="noopener" target="_blank" href="https://cookiemunch.dunks1980.com">
                        <span>shop</span>
                      </a>
                    </div>
                    <div class="sushi">
                      <a rel="noopener" target="_blank" href="https://screentimeconverter.com" class="">
                        <span>sushi</span>
                      </a>
                    </div>
                    <div class="bakery">
                      <a rel="noopener" target="_blank" href="https://inlinesvg.dunks1980.com/">
                        <span>bakery</span>
                      </a>
                    </div>
                  </div>
                </div>
                <svg id="welcomelogo" width="400" height="73" viewBox="0 0 400 73" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M357.521 30.9728L357.521 30.9738C355.594 35.1027 354.634 39.7987 354.634 45.0568C354.634 50.2923 355.594 54.9658 357.521 59.0721C359.448 63.1786 362.181 66.4194 365.722 68.7873C369.268 71.1591 373.431 72.3409 378.202 72.3409C381.684 72.3409 384.721 71.7568 387.305 70.5799C389.897 69.41 392.038 67.9497 393.723 66.1959C395.419 64.4306 396.676 62.6577 397.486 60.8762L397.594 60.6389L397.352 60.541L393.568 59.0069L393.356 58.9207L393.252 59.1253C392.606 60.3946 391.644 61.7165 390.36 63.0907C389.09 64.4501 387.447 65.6146 385.424 66.5809C383.443 67.5158 381.038 67.9886 378.202 67.9886C374.246 67.9886 370.866 67.0004 368.05 65.0341C365.226 63.0395 363.05 60.3379 361.521 56.9215C360.099 53.6741 359.346 50.031 359.266 45.9886H398.963H399.213V45.7386V43.1477C399.213 39.2369 398.63 35.7069 397.459 32.5613C396.313 29.4207 394.717 26.7329 392.671 24.5019C390.648 22.2729 388.302 20.5702 385.633 19.3967C382.987 18.2002 380.179 17.6023 377.213 17.6023C372.846 17.6023 368.955 18.7984 365.547 21.1932C362.144 23.5842 359.47 26.8467 357.521 30.9728ZM394.553 41.7045H359.344C359.597 38.3991 360.379 35.3715 361.689 32.6194C363.263 29.3581 365.385 26.7788 368.052 24.8739L368.052 24.8737C370.735 22.9507 373.786 21.9886 377.213 21.9886C380.483 21.9886 383.423 22.8724 386.039 24.639C388.661 26.4091 390.735 28.7962 392.263 31.8063C393.755 34.7462 394.52 38.044 394.553 41.7045Z" stroke="white" stroke-width="0.5"/>
                  <path d="M276.25 71V71.25H276.5H280.659H280.909V71V36.6364C280.909 33.7823 281.448 31.2644 282.52 29.0768C283.614 26.8885 285.14 25.1741 287.1 23.9272C289.076 22.6836 291.426 22.0568 294.159 22.0568C298.194 22.0568 301.182 23.3206 303.168 25.8148L303.169 25.8157C305.17 28.3067 306.182 31.554 306.182 35.5795V71V71.25H306.432H310.591H310.841V71V36.1932C310.841 32.0601 311.985 28.6779 314.258 26.0263C316.519 23.3889 319.761 22.0568 324.023 22.0568C328.014 22.0568 331.003 23.2874 333.035 25.7172C335.078 28.159 336.114 31.5273 336.114 35.8523V71V71.25H336.364H340.523H340.773V71V35.8523C340.773 30.268 339.422 25.8408 336.692 22.6009C333.975 19.3273 330.033 17.7045 324.909 17.7045C320.982 17.7045 317.657 18.6351 314.949 20.5104L314.948 20.5109C312.316 22.3485 310.473 24.7902 309.423 27.8295H309.407C308.366 24.7547 306.676 22.3029 304.336 20.4847C301.962 18.6234 298.846 17.7045 295.011 17.7045C291.519 17.7045 288.516 18.4862 286.015 20.0612C283.575 21.5969 281.837 23.6661 280.807 26.2643V18.6364V18.3864H280.557H276.5H276.25V18.6364V71Z" stroke="white" stroke-width="0.5"/>
                  <path d="M228.144 68.8188L228.145 68.8195C231.553 71.1681 235.444 72.3409 239.81 72.3409C244.175 72.3409 248.066 71.1681 251.474 68.8195L251.475 68.8188C254.878 66.4504 257.553 63.1989 259.502 59.0727C261.452 54.9436 262.423 50.2471 262.423 44.9886C262.423 39.7302 261.452 35.0337 259.502 30.9046C257.553 26.7784 254.878 23.5268 251.475 21.1584C248.067 18.7867 244.176 17.6023 239.81 17.6023C235.443 17.6023 231.552 18.7867 228.144 21.1584C224.741 23.5268 222.066 26.7782 220.118 30.9043C218.168 35.011 217.196 39.7077 217.196 44.9886C217.196 50.2471 218.168 54.9436 220.118 59.0727C222.066 63.1989 224.741 66.4504 228.144 68.8188ZM249.239 64.9366L249.238 64.9372C246.557 66.97 243.418 67.9886 239.81 67.9886C236.201 67.9886 233.05 66.9701 230.346 64.9367C227.658 62.8977 225.558 60.139 224.051 56.6514C222.566 53.1636 221.821 49.2772 221.821 44.9886C221.821 40.7003 222.577 36.8257 224.084 33.3611L224.085 33.3605C225.592 29.8725 227.692 27.1133 230.381 25.0742L230.382 25.0734C233.063 23.0182 236.202 21.9886 239.81 21.9886C243.418 21.9886 246.556 23.0182 249.237 25.0734L249.238 25.0742C251.927 27.1133 254.027 29.8725 255.535 33.3605L255.535 33.3611C257.042 36.8257 257.798 40.7003 257.798 44.9886C257.798 49.277 257.042 53.1631 255.535 56.6508L255.534 56.6521C254.049 60.1391 251.95 62.8976 249.239 64.9366Z" stroke="white" stroke-width="0.5"/>
                  <path d="M174.826 68.7845L174.827 68.7852C178.258 71.1574 182.229 72.3409 186.73 72.3409C190.174 72.3409 193.293 71.6404 196.081 70.2346C198.866 68.8305 201.159 66.884 202.956 64.3964C204.753 61.9073 205.903 59.0287 206.409 55.7655L206.454 55.4773H206.162H201.935H201.726L201.689 55.6829C201.24 58.1701 200.312 60.3373 198.906 62.1898C197.498 64.0444 195.745 65.4735 193.645 66.479L193.644 66.4795C191.567 67.4843 189.264 67.9886 186.73 67.9886C183.144 67.9886 179.992 66.9812 177.265 64.9693C174.531 62.9525 172.398 60.2161 170.868 56.7516C169.339 53.2651 168.571 49.3228 168.571 44.9204C168.571 40.4501 169.361 36.4979 170.935 33.0585L170.935 33.058C172.51 29.5928 174.666 26.8908 177.398 24.9422L177.399 24.9414C180.128 22.9733 183.235 21.9886 186.73 21.9886C190.631 21.9886 193.901 23.1417 196.555 25.439L196.557 25.4405C199.24 27.7215 200.916 30.6026 201.587 34.0927L201.626 34.2954H201.832H206.06H206.352L206.307 34.0069C205.801 30.7651 204.627 27.9084 202.783 25.4418C200.964 22.9779 198.66 21.0547 195.876 19.6739C193.111 18.2915 190.049 17.6023 186.696 17.6023C182.239 17.6023 178.291 18.7978 174.86 21.1927C171.434 23.5838 168.759 26.8469 166.833 30.9738C164.906 35.1024 163.946 39.7757 163.946 44.9886C163.946 50.2012 164.895 54.8741 166.799 59.0024L166.799 59.0034C168.725 63.1304 171.4 66.3934 174.826 68.7845Z" stroke="white" stroke-width="0.5"/>
                  <path d="M150.128 1.18182V0.931824H149.878H145.719H145.469V1.18182V71V71.25H145.719H149.878H150.128V71V1.18182Z" stroke="white" stroke-width="0.5"/>
                  <path d="M89.9586 30.9728L89.9581 30.9738C88.0313 35.1027 87.071 39.7987 87.071 45.0568C87.071 50.2923 88.0314 54.9658 89.9583 59.0721C91.8854 63.1786 94.6189 66.4194 98.1593 68.7873C101.705 71.1591 105.869 72.3409 110.639 72.3409C114.121 72.3409 117.158 71.7568 119.743 70.5799C122.335 69.41 124.476 67.9497 126.16 66.1959C127.857 64.4306 129.114 62.6577 129.924 60.8762L130.031 60.6389L129.79 60.541L126.006 59.0069L125.793 58.9207L125.689 59.1253C125.043 60.3946 124.081 61.7165 122.797 63.0907C121.527 64.4501 119.884 65.6146 117.862 66.5809C115.88 67.5158 113.476 67.9886 110.639 67.9886C106.683 67.9886 103.303 67.0004 100.488 65.0341C97.6639 63.0395 95.4872 60.3379 93.9587 56.9215C92.5368 53.6741 91.7835 50.031 91.7032 45.9886H131.401H131.651V45.7386V43.1477C131.651 39.2369 131.067 35.7069 129.896 32.5613C128.75 29.4207 127.155 26.7329 125.108 24.5019C123.086 22.2729 120.739 20.5702 118.071 19.3967C115.424 18.2002 112.617 17.6023 109.651 17.6023C105.284 17.6023 101.392 18.7984 97.9841 21.1932C94.5815 23.5842 91.907 26.8467 89.9586 30.9728ZM126.99 41.7045H91.7816C92.0342 38.3991 92.8165 35.3715 94.126 32.6194C95.7005 29.3581 97.8222 26.7788 100.489 24.8739L100.489 24.8737C103.173 22.9507 106.223 21.9886 109.651 21.9886C112.921 21.9886 115.86 22.8724 118.477 24.639C121.098 26.4091 123.173 28.7962 124.7 31.8063C126.192 34.7462 126.957 38.044 126.99 41.7045Z" stroke="white" stroke-width="0.5"/>
                  <path d="M20.4408 71.0663L20.4913 71.25H20.6818H25.5909H25.7824L25.8323 71.0651L42.7216 8.43535L59.6109 71.0651L59.6608 71.25H59.8523H64.7614H64.9519L65.0024 71.0663L84.1956 1.24809L84.2825 0.931824H83.9545H79.5568H79.3653L79.3154 1.11676L62.3198 64.1705H62.2946L45.5712 1.11773L45.5219 0.931824H45.3295H40.1477H39.9554L39.9061 1.11773L23.1827 64.1705H23.1574L6.16184 1.11676L6.11199 0.931824H5.92045H1.48863H1.16063L1.24757 1.24809L20.4408 71.0663Z" stroke="white" stroke-width="0.5"/>
                </svg>
              </main>

              <footer>©2024 http://localhost:3000/.com</footer>
            </div>
          </div>
        </div>
      </v-main>
    </div>
  </v-app>
</template>

<style scoped>
.main {
  min-height: 100vh;
  background-color: #000; /* Set the background to black */
  color: #fff; /* Set the text color to white */
}

.toolbar-style {
display: flex;
  justify-content: right;
  align-items: center;
  padding: 0.93vh 0; /* 10px to vh */
  
}

.toolbar-style a {
  color: white;
  text-decoration: none;
   padding: 0.93vh 1.04vw; /* 10px to vh and 20px to vw */
}

.toolbar-style a:hover {
  background-color: black;
}

.toolbar-style img {
  transition: transform 0.3s ease; /* Add transition for smooth effect */
}

.toolbar-style img:hover {
  transform: scale(1.2); /* Scale image to 1.2 times its original size */
}

.yt img {
  width: 48px;
}

.git img {
  margin: 0px 8px 0px 2px;
  width: 44px;
}

.res img {
  margin: 0px 300px 0px 0px;
  width: 40px;
}

#welcomelogo {
  animation: fill 0.5s ease forwards 2s;
  position: fixed;
top: 32.6vh; /* 300px to vh */
  left: 26.04vw; /* 500px to vw */
}

#welcomelogo path:nth-child(1) {
  stroke-dasharray: 319px;
  stroke-dashoffset: 319px;
  animation: line-anim 2s ease forwards;
}

#welcomelogo path:nth-child(2) {
  stroke-dasharray: 425px;
  stroke-dashoffset: 425px;
  animation: line-anim 2s ease forwards;
}

#welcomelogo path:nth-child(3) {
  stroke-dasharray: 275px;
  stroke-dashoffset: 275px;
  animation: line-anim 2s ease forwards;
}

#welcomelogo path:nth-child(4) {
  stroke-dasharray: 253px;
  stroke-dashoffset: 253px;
  animation: line-anim 2s ease forwards;
}

#welcomelogo path:nth-child(5) {
  stroke-dasharray: 163px;
  stroke-dashoffset: 163px;
  animation: line-anim 2s ease forwards;
}

#welcomelogo path:nth-child(6) {
  stroke-dasharray: 319px;
  stroke-dashoffset: 319px;
  animation: line-anim 2s ease forwards;
}

#welcomelogo path:nth-child(7) {
  stroke-dasharray: 541px;
  stroke-dashoffset: 541px;
  animation: line-anim 2s ease forwards;
}

@keyframes line-anim {
  to {
    stroke-dashoffset: 0;
  }
}

@keyframes fill {
  from {
    fill: transparent;
  }
  to {
    fill: white;
  }
}

.text-name {
  position: fixed;
  padding-left: 20px; 
  top: 52.4vh;
  left: 21.61vw;
  
}

.text-about {
  position: fixed;
   top: 63.1vh; /* 580px to vh */
  left: 22.71vw; /* 436px to vw */
 
}

h2 {
  position: fixed;
top: 38.1vh; /* 350px to vh */
  left: 62.5vw; /* 1200px to vw */
}

a {
  text-decoration: none;
}

.project-wrapper {
  position: fixed;
   top: 49vh; /* 450px to vh */
  left: 62.5vw; /* 1200px to vw */
}

.ecommerce, .travel, .sushi, .shop, .bakery {
  padding: 1.6vh 0; /* 15px to vh */
}

.ecommerce a:after {
  content: '';
  display: block;
  width: 86px; /* 底線的寬度 */
  height: 1px; /* 底線的粗細 */
  background: linear-gradient(to left, rgb(88, 76, 168), rgb(131, 194, 83)); /* 左邊紅色漸變到右邊藍色 */
  position: absolute;
}

.ecommerce a:hover {
  letter-spacing: 1.1px;
  transition: 1s 0.1s;
}

.ecommerce a:hover::after {
  display: block;
  width: 95px; /* 底線的寬度 */
  height: 1px; /* 底線的粗細 */
  background: linear-gradient(to left, rgb(88, 76, 168), rgb(131, 194, 83)); /* 左邊紅色漸變到右邊藍色 */
  position: absolute;
  transition: 1s 0.1s;
}

.shop a:after {
  content: '';
  display: block;
  width: 35px; /* 底線的寬度 */
  height: 1px; /* 底線的粗細 */
  background: linear-gradient(to left, rgb(88, 76, 168), rgb(131, 194, 83)); /* 左邊紅色漸變到右邊藍色 */
  position: absolute;
}

.shop a:hover {
  letter-spacing: 1.1px;
  transition: 1s 0.1s;
}

.shop a:hover::after {
  display: block;
  width: 41px; /* 底線的寬度 */
  height: 1px; /* 底線的粗細 */
  background: linear-gradient(to left, rgb(88, 76, 168), rgb(131, 194, 83)); /* 左邊紅色漸變到右邊藍色 */
  position: absolute;
  transition: 1s 0.1s;
}

.sushi a:after {
  content: '';
  display: block;
  width: 40px; /* 底線的寬度 */
  height: 1px; /* 底線的粗細 */
  background: linear-gradient(to left, rgb(88, 76, 168), rgb(131, 194, 83)); /* 左邊紅色漸變到右邊藍色 */
  position: absolute;
}

.sushi a:hover {
  letter-spacing: 1.1px;
  transition: 1s 0.1s;
}

.sushi a:hover::after {
  display: block;
  width: 46px; /* 底線的寬度 */
  height: 1px; /* 底線的粗細 */
  background: linear-gradient(to left, rgb(88, 76, 168), rgb(131, 194, 83)); /* 左邊紅色漸變到右邊藍色 */
  position: absolute;
  transition: 1s 0.1s;
}

.bakery a:after{
  content: '';
  display: block;
  width: 47px; /* 底線的寬度 */
  height: 1px; /* 底線的粗細 */
  background: linear-gradient(to left, rgb(88, 76, 168), rgb(131, 194, 83)); /* 左邊紅色漸變到右邊藍色 */
  position: absolute;
}
.bakery a:hover
{
  letter-spacing: 1.1px;
  transition: 1s 0.1s;
}
.bakery a:hover::after{
  display: block;
  width: 53px; /* 底線的寬度 */
  height: 1px; /* 底線的粗細 */
  background: linear-gradient(to left, rgb(88, 76, 168), rgb(131, 194, 83)); /* 左邊紅色漸變到右邊藍色 */
  position: absolute;
  transition: 1s 0.1s;
}
.travel a:after {
  content: '';
  display: block;
  width: 40px; /* 底線的寬度 */
  height: 1px; /* 底線的粗細 */
  background: linear-gradient(to left, rgb(88, 76, 168), rgb(131, 194, 83)); /* 左邊紅色漸變到右邊藍色 */
  position: absolute;
}

.travel a:hover {
  letter-spacing: 1.1px;
  transition: 1s 0.1s;
}

.travel a:hover::after {
  display: block;
  width: 53px; /* 底線的寬度 */
  height: 1px; /* 底線的粗細 */
  background: linear-gradient(to left, rgb(88, 76, 168), rgb(131, 194, 83)); /* 左邊紅色漸變到右邊藍色 */
  position: absolute;
  transition: 1s 0.1s;
}

.ecommerce a,
.travel a,
.shop a,
.sushi a,
.bakery a {
  color: #fff;
}

#svg-wrapper {
  position: relative;
  height: 100vh;
  fill: #fff; /* Set the SVG fill to white if needed */
}

/* Add other style changes here to match the black theme of dunks1980.com */

.svg-top-left {
  position: fixed;
top: 7.1vh; /* 65px to vh */
  left: 16.67vw; /* 320px to vw */
}


.svg-projects {
  position: fixed;
 top: 32.6vh; /* 300px to vh */
  left: 60.42vw; /* 1160px to vw */
}

.svg-bottom-right {
  position: fixed;
  bottom: 6.5vh; /* 60px to vh */
  right: 15.63vw; /* 300px to vw */
  transform: rotate(180deg);
  z-index: 10;
}

.toolbar-style {
  position: absolute;
  top: 10.9vh; /* 100px to vh */
  left: 1.3vw; /* 25px to vw */
  width: calc(100% - 25px * 2);
}



.text-name::before {
  content: '';
  position: absolute; /* Position it absolutely to place it exactly where you need it */
  left: 0; /* Align it to the left edge of the .text-name element */
  top: 0; /* Align it to the top of the .text-name element */
  bottom: 0; /* Stretch it to the bottom of the .text-name element */
  width: 3px; /* Width of the line */
  background: linear-gradient(to bottom, rgb(88, 76, 168), rgb(131, 194, 83)); /* Gradient from red to blue */
}

footer {
  position: fixed;
  right: 17.71vw; /* 340px to vw */
  bottom: 9vh; /* 80px to vh */
  padding: 1.85vh 0; /* 20px to vh */
  color: #666; /* Set the footer text color */
  z-index: 10;
}

/* Media Query for Mobile Devices */
@media (max-width: 768px) {
  .svg-top-left {
    width: 150px;
    height: 150px;
    top: 20px;
    left: 10px;
  }

  .svg-projects {
    width: 60px;
    height: 60px;
    top: 350px;
    left: 20px;
  }

  .text-name {
    top: 200px;
    left: 10px;
    font-size: 14px;
  }

  .text-about {
    top: 260px;
    left: 10px;
    font-size: 14px;
  }

  h2 {
    top: 400px;
    left: 10px;
    font-size: 18px;
  }

  .project-wrapper {
    top: 450px;
    left: 10px;
  }

  .ecommerce, .travel, .sushi, .shop {
    padding: 10px 0px;
  }

  .toolbar-style {
    top: 10px;
    left: 0;
    width: 100%;
    justify-content: center;
  }

  #welcomelogo {
    width: 200px;
    height: 36.5px;
    top: 100px;
    left: 50px;
  }

  footer {
    right: 10px;
    bottom: 10px;
    font-size: 12px;
  }
}
</style>

<script>
export default {
  data() {
    return {
      drawer: false,
      isMobile: false,
      color1: 'rgb(88,76,168)', // 修正括號問題
      color2: 'rgb(131,194,83)' // 修正後
    }
  },
  mounted() {
    this.checkIfMobile();
    window.addEventListener('resize', this.checkIfMobile);

    const welcomelogo = document.querySelectorAll('#welcomelogo path');
    for (let i = 0; i < welcomelogo.length; i++) {
      console.log(`Letter ${i} is ${welcomelogo[i].getTotalLength()}`);
    }
  },
  beforeDestroy() {
    window.removeEventListener('resize', this.checkIfMobile);
  },
  methods: {
    checkIfMobile() {
      this.isMobile = window.innerWidth <= 768;
    }
  }
}
</script>
