<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="">
      <div class="searchbar">
      <input type="text" name="" value="">
      <select class="" name="">
        <option value="">台灣</option>
        <option value="">中國</option>
      </select>
      <button type="button" name="button">開找</button>
      </div>
    </div>
    <div class="bumplist">
      <h1>{{where}} 必買</h1>
      <div class="list-grid">
        <div class="bumpitem" v-for="(item,index) in itemlist">
          <div class="item-grid">
            <div class="item-img cursor" @click="show(index)">
              <img :src="item.img">
              <span class="itemname">{{item.itemname}}</span>
            </div>
            <div v-show="item.showcontent" class="user">
              <div class="user-img">
                <img src="http://fakeimg.pl/250x100/ff0000/">
              </div>
              <div class="user-name">
                <h2>Yuly</h2>
              </div>
            </div>
            <div v-show="item.showcontent"class="content">
              <span>2017/10/31</span>
              <div class="">
                <p>hen好吃</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data () {
    return {
      msg: '找名產',
      where: '索瑪莉雅',
      itemlist: [
        {
          img: 'http://fakeimg.pl/200x200/ff3000/',
          itemname: 'testitem',
          showcontent: false
        },
        {
          img: 'http://fakeimg.pl/200x200/ff3000/',
          itemname: 'testitem',
          showcontent: false
        },
        {
          img: 'http://fakeimg.pl/200x200/ff3000/',
          itemname: 'testitem',
          showcontent: false
        },
        {
          img: 'http://fakeimg.pl/200x200/ff3000/',
          itemname: 'testitem',
          showcontent: false
        },
        {
          img: 'http://fakeimg.pl/200x200/ff3000/',
          itemname: 'testitem',
          showcontent: false
        },
        {
          img: 'http://fakeimg.pl/200x200/ff3000/',
          itemname: 'testitem',
          showcontent: false
        },
        {
          img: 'http://fakeimg.pl/200x200/ff3000/',
          itemname: 'testitem',
          showcontent: false
        },
        {
          img: 'http://fakeimg.pl/200x200/ff3000/',
          itemname: 'testitem',
          showcontent: false
        },
        {
          img: 'http://fakeimg.pl/200x200/ff3000/',
          itemname: 'testitem',
          showcontent: false
        }
      ]
    }
  },
  methods: {
    show: function (index) {
      let thisone = this.itemlist[index]
      thisone.showcontent = !thisone.showcontent
    }
  }
}
</script>

<style lang="scss">
h1, h2 {
  font-weight: normal;
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
}
.cursor{
  cursor: pointer;
}

.hello{
  padding:0 2%;
}

.bumpitem{
  display:flex;
  flex-wrap: wrap;
}
.list-grid{
  display:flex;
  flex-wrap: wrap;
  .item-img{
    position:relative;
    display:flex;
    align-items: center;
    justify-content: center;
  }
  .itemname{
    position:absolute;
  }
}
.item-grid{
  width:30vw;
}

</style>
