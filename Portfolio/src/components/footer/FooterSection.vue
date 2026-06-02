<template>
  <section id="footer">
    <div class="content">
      <img src="@/assets/navbar/Manoj_logo-removebg-preview.png" alt="Manoj logo" />
      <p>manojsreekumar2000@gmail.com</p>
      <h5>Web designer and front-end developer</h5>
    </div>
    <div class="links">
      <div class="networks">
        <div class="netbox">
          <a
            class="icon"
            href="https://www.linkedin.com/in/manoj-sreekumar"
            data-tip="I share some interesting posts about Tech in Linkedln"
          >
            <img src="@/assets/navbar/icons8-linkedin.svg" alt="linkedln" /></a
          ><a
            class="icon"
            href="https://www.freelancer.in/u/manojsreekumar20?sb=t"
            data-tip="Do you like my work?  Hire me!"
            ><img src="@/assets/navbar/freelancer-icon.svg" alt="freelancer" /></a
          ><a
            class="icon"
            href="https://github.com/ManojSreekumarK"
            data-tip="I've written a lot of lines of code, take a look :)"
            ><img src="@/assets/navbar/icons8-github.svg" alt="github"
          /></a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
@import '@/styles/varables';
#footer {
  width: $layout-col1;
  max-width: $max-width;
  border-top: 1px solid #abb2bf;
  margin: 32px auto;
  padding: 30px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  .content {
    margin-top: 40px;
    img {
      width: 72px;
      height: 21px;
    }
  }
}
.networks {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 84px;
  img {
    width: 30px;
    height: 30px;
  }
}

.netbox {
  position: relative;
  width: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid #abb2bf;
  color: $secondary-color;
}
.netbox .icon {
  padding: 0.6rem 0.6rem;
  margin: 0 0.4rem;
}
.netbox .icon:after {
  position: absolute;
  right: 0;
  bottom: 3.5rem;
  z-index: 20;
  content: attr(data-tip);
  display: block;
  width: auto;
  font-size: 0.6rem;
  color: $secondary-color;
  background-color: transparent;
  border: 1px solid #eb7132;
  padding: 1rem;
  opacity: 0;
  pointer-events: none;
  transform: translateY(1rem);
  margin-bottom: 20px;
  transition: all 300ms ease 200ms;
}
.netbox .icon:hover {
  color: #ffe082;
}
.netbox .icon:hover:after {
  opacity: 1;
  transform: translateY(0);
}
.netbox:before {
  position: absolute;
  top: -0.5rem;
  left: 0;
  content: '';
  display: block;
  width: 40%;
  height: 1px;
  background-color: #eb7132;
}
.netbox:after {
  position: absolute;
  top: -0.8rem;
  right: 0;
  content: 'Find me on my networks!';
  font-size: 0.5rem;
  padding-left: 10px;
  background-color: transparent;
}
</style>
