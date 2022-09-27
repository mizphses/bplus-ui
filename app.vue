<template>
  <div>
    <NuxtLayout>
      <NuxtPage class="baseheight"/>
      <footer class="footer">
        <p>(c)2022 &nbsp;</p>
        <img src="~/assets/images/chips-logo.svg" alt="中央大学高度情報化計画学生実行委員会" width="220">
      </footer>
    </NuxtLayout>
  </div>
</template>

<style>
  .baseheight {
    min-height: 100vh;
  }
  .footer {
    height: 4em;
    padding: 1em 2em;
    background-color: #f5f5f5;
    display: flex;
    justify-content: start;
    align-items: center;
  }

  @media print{
    .baseheight {
      min-height: 0;
      padding-bottom: 1em;
    }
    .footer {
      height: 2em;
    }
  }
</style>