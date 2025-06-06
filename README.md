<!DOCTYPE html>
<html lang="zh-TW">
<head>
  <meta charset="UTF-8" />
  <title>AR 流浪狗故事</title>
  <script src="https://cdn.jsdelivr.net/npm/aframe@1.4.2/dist/aframe.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/mind-ar@1.1.4/dist/mindar-image-aframe.prod.js"></script>
  <style>
    body, html {
      margin: 0;
      overflow: hidden;
      background-color: black;
    }
  </style>
</head>
<body>
  <a-scene
    mindar-image="imageTargetSrc: 1.mind; autoStart: true;"
    vr-mode-ui="enabled: false"
    device-orientation-permission-ui="enabled: true"
    embedded
  >
    <a-assets>
      <a-asset-item id="dogText" src="dog-text.glb"></a-asset-item>
    </a-assets>

    <a-camera position="0 0 0" look-controls="enabled: false"></a-camera>

    <a-entity mindar-image-target="targetIndex: 0">
      <a-text 
        value="
狗媽媽生下了四個小孩，漸漸地小狗們一天一天地被奶大開始東爬西爬，飼主擔心他們被車輾壓，因此把他們全部放進一個小狗籠....
鄰居看這樣下去也不是個辦法，便好心幫他們通報動保單位，才讓這個狗媽媽和小狗們脫離了不適當的環境和飼養方法，重新開展新狗生。
賓莎有著一雙大眼睛以及一身烏黑亮麗、長短不齊的黑色毛髮，讓她乍看之下很低調但細看其實很不平凡！好適合稱她「暗黑搖滾甜心」呀！
不過別看她長得很有個性，其實她有點‘必速’，常常會躲在角落靜靜的看著大家，仔仔細細的觀察你是不是一個可以靠近的人。
        " 
        position="0 0 0" 
        scale="0.5 0.5 0.5" 
        color="white"
        align="center"
      ></a-text>
    </a-entity>
  </a-scene>

  <script>
    if(location.protocol === 'file:') {
      alert('請用本地伺服器開啟此頁面，以避免檔案載入失敗（404）問題。\n推薦使用 VSCode Live Server 或 Node.js http-server');
    }
  </script>
</body>
</html>
