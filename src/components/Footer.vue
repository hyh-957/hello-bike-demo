<template>
  <div class="footer">
    <div class="content">
      <div class="logo__wrapper">
        <img class="logo" src="../../public/static/image/QgoaP_header__logo--colored.png"
          alt="Hellobike">
        <div class="tel">
          <p>上海钧正网络科技有限公司</p>
        </div>
        <div class="record">
          <div>© hello-inc.com&nbsp;<a target="_blank" href="https://beian.miit.gov.cn/">沪ICP备16050850号-19</a></div>
          <div>增值电信业务经营许可证编号：沪B2-20201172</div>
          <div>
            <img src="../../public/static/image/wangan.png" alt="">
            <a href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=31011202007567" target="_blank">沪公网安备
              31011202007567号 </a>
            &nbsp;|&nbsp;
            <a target="_blank"
              href="http://wap.scjgj.sh.gov.cn/businessCheck/verifKey.do?showType=extShow&amp;serial=9031000020181213104636000003456828-SAIC_SHOW_310000-20191202135717172087&amp;signData=MEYCIQC5EVgJ/BryKrcZB6jOcLNw7HAWn6rPJlIit8jg6ug8mgIhAOg1vF3DUfVJkMPpsiUfdm+6+40Z88mYrIELcvoDlsKK"><img
                src="../../public/static/image/license-logo.jpg" alt="">
            </a>
          </div>
        </div>
      </div>
      <div class="footer-columns">
        <div class="know footer-column">
          <h3>了解哈啰</h3>
          <p><a href="javascript:void(0);">哈啰科技</a></p>
          <p><a href="javascript:void(0);">哈啰单车</a></p>
          <p><a href="javascript:void(0);">哈啰助力车</a></p>
          <p><a href="javascript:void(0);">哈啰电动车</a></p>
          <p><a href="javascript:void(0);">小哈换电</a></p>
        </div>
        <div class="about footer-column">
          <h3>关于哈啰</h3>
          <p><a href="javascript:void(0);">哈啰简介</a></p>
          <p><a href="javascript:void(0);">领导团队</a></p>
          <p><a href="javascript:void(0);">荣誉奖项</a></p>
          <p><a href="javascript:void(0);">社会责任</a></p>
          <p><a href="javascript:void(0);">资讯中心</a></p>
        </div>
        <div class="join footer-column">
          <h3>联系我们</h3>
          <p><a href="javascript:void(0);">联系我们</a></p>
          <p class="li_join_us"><a href="https://careers.hellobike.com">加入我们</a></p>
        </div>
        <div class="social footer-column">
          <h3>社交网络</h3>

          <div class="icon">
            <a href="javascript:void(0);"></a>
            <a href="javascript:void(0);"></a>
            <a href="javascript:void(0);"></a>
            <a href="javascript:void(0);"></a>
            <a href="javascript:void(0);"></a>
            <a href="javascript:void(0);"></a>

          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>

</script>


<style scoped lang="less">
a {
  text-decoration: none;
  color: #999;
}

.footer {
  width: 100%;
  font-size: 12px;
}

.content {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 950px;
  margin: 0 auto;
}

.logo {
  height: 32px;
  width: 140px;
}

.tel {
  color: #666;
}

.record {
  display: flex;
  flex-direction: column;
  color: #999;
}

.footer .record img {
  width: 16px;
}

.footer-columns {
  display: flex;
  justify-content: space-between;
  margin-left: 94px;
  flex: 1;
  font-size: 12px;
}

.footer-column>h3 {
  font-size: 14px;
  font-weight: 500;
  color: #333;
}

.footer-column>p {
  color: #999;
}

.icon {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 5px;
}
.icon>a {
  height: 26px;
  width: 26px;
  background-image: url(https://www.hello-inc.com/online-public/layout/layout__footer--sina.png);
  background-size: contain;
}
</style>
