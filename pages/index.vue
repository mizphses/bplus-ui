<template>
  <div>
    <NavBar />
    <div class="main-images">B plusでよりBetterな中大ライフを。</div>
    <div class="padding-2em">
      <p>「B plus」は中央大学で生活するために不可欠な情報をわかりやすくまとめたホームページです。</p>
      <p>また、自主開発の、中大生のための便利なツールも一部掲載しております。</p>
      <hr class="hr-width-1/2" />
      <h2 class="center">ご提供中のサービス</h2>
      <div class="services-wrap">
        <a href="/timetable" class="services-inside no-decorator">
          <p>
            <span class="material-symbols-outlined service-icon">event</span>
          </p>
          <p>Better時間割</p>
        </a>
        <a href="#" class="services-inside no-decorator">
          <p>
            <span class="material-symbols-outlined service-icon">menu_book</span>
          </p>
          <p>教材購入補助ツール</p>
        </a>
        <a href="#" class="services-inside no-decorator">
          <p>
            <span class="material-symbols-outlined service-icon">check_circle</span>
          </p>
          <p>卒業可否確認ツール</p>
        </a>
        <a href="#" class="services-inside no-decorator">
          <p>
            <span class="material-symbols-outlined service-icon">glyphs</span>
          </p>
          <p>e過去問</p>
        </a>
        <a href="#" class="services-inside no-decorator">
          <p>
            <span class="material-symbols-outlined service-icon">badge</span>
          </p>
          <p>Chuo.club 認証基盤</p>
        </a>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .main-images {
    height: 300px;
    width: calc(100vw - 4em);
    margin: 0;
    padding: 2em;
    display: flex;
    flex-direction: column;
    justify-content: center;
    background-image: url("@/assets/images/bg-chuo.jpg");
    background-size: cover;
    background-position: center;
    color: white;
    font-weight: bold;
    font-size: 2em;
    text-shadow: black 0 0 0.5em;
  }
  .padding-2em {
    padding: 2em;
  }

  .hr-width-1\/2{
    width: 50%;
    margin-top: 2em;
    margin-bottom: 2em;
  }

  .services-wrap{
    display: flex;
    justify-content: space-around;
  }

  .services-inside{
    box-shadow: rgba(0, 0, 0, 0.2) 0px 0px 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 15em;
    padding: 0.5em;
    margin: 0.5em;
    border-radius: 10px;
    border: 1px solid #f0f0f0;
    color: black;
    .service-icon{
      font-size: 3em;
    }
  }
  .services-inside:hover{
    background-color: #fdffdf;
    border: 1px solid #ffc422;
  }
  @media (max-width: 1024px) {
    .services-wrap{
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-content: center;
    }
    .services-inside{
      width: calc(100% - 4em);
      margin: 1em;
    }

  }
</style>