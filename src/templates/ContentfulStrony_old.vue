<template>
  <Layout>
    <g-link  to="/"><p  class='zamykacz'  @click="ruszaj" >X</p></g-link>
    <div class="podstrona">
      <div class="" v-html="$page.contentfulStrony.trescstrony">
    </div>
    </div>
  </Layout>
</template>

<page-query>
  query ($id: ID!){
    contentfulStrony  (id: $id) {
    nazwa
    id
    trescstrony
  }
}

</page-query>
<script>
import { documentToHtmlString } from '@contentful/rich-text-html-renderer'

export default {

}
</script>

<style>
.podstrona {

  color: #000;
  background-color: #fff;;
  margin: 0 auto;
  min-height: 85vh;
  overflow: visible;




  text-align: center;
  display: flex;
  flex-direction: column;

  width: 100vw;
  position: absolute;
  right: 0;

  z-index: 1011;
  font-size: 2.3em;


}
</style>
