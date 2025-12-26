<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <link rel="shortcut icon" href="https://download3.dfrobot.com.cn/website/image/title.ico" />
    <title>Mind+ sb3文件在线修复工具</title>
    <link rel="stylesheet" type="text/css" href="./common/css/repairTool.css?version=20200930" />
  </head>
  <body>
    <div>
      <header>
        <h3 id="title">sb3文件在线修复工具</h3>
      </header>
      <section>
        <div class="form flex column left-center">
          <div class="topTab">
            <a class="href-nav" href="./transformTool.html"><img class="href-nav-img" src="/images/mindplusone/href.png" />转换工具</a>
            <a class="href-nav active" href="#"><!-- <img class="href-nav-img" src="./image/href.png"> -->修复工具</a>
          </div>
          <section class="uploadWrapper uploadSb3">
            <span>请先上传附件:</span>
            <label for="uploadFile" class="uploadFileContent pointer" title="选择文件">
              <input type="file" id="uploadFile" accept=".sb3" />
              <span id="showFileName"></span>
            </label>
          </section>
          <section class="uploadWrapper downloadFile">
            <label id="downloadFile">
              <span>下载修复后的文件</span>
            </label>
          </section>
          <section class="promptWrapper">
            <span>如果以上还没有解决您的问题，我们非常抱歉，您可以在Mind+软件内部提交反馈，我们会及时解决您的问题!!!</span>
          </section>
        </div>
      </section>
      <!-- <footer></footer> -->
    </div>
    <script src="https://cdn.bootcss.com/jquery/3.4.1/jquery.min.js"></script>
    <script type="text/javascript" src="./common/js/bundle.js"></script>
  </body>
  <script>
    var _hmt = _hmt || [];
    (function () {
      var hm = document.createElement('script');
      hm.src = 'https://hm.baidu.com/hm.js?45e3c5cdc2d69a451ef3d3a6ae902f24';
      var s = document.getElementsByTagName('script')[0];
      s.parentNode.insertBefore(hm, s);
    })();
  </script>
  <script type="text/javascript">
    window.alert = tips;
    /*var shouldRM = false;
    $("body").on("click",function(){
      if(!shouldRM){
        shouldRM = !shouldRM;
        return;
      }

      $(".tips")?$(".tips").delay(2000).hide(0,function(){
            $(this).remove();
      }):null;
    })*/

    // 提示框
    function tips(msg, delay) {
      var tip_cont = '<div class="tips"><span>';
      tip_cont += msg;
      tip_cont += '</span></div>';
      if (!$('.tips')[0]) {
        $('body').append(tip_cont);
      } else {
        $('.tips>span').html(msg);
      }
      $('.tips').show().addClass('in');

      $('.tips').on('click', (e) => {
        // console.log(e.target.tagName);
        if (e.target.tagName == 'SPAN') {
          return;
        } else {
          $('.tips').removeClass('in');
          setTimeout(() => {
            $('.tips').remove();
          }, 1000);
        }
      });
    }
  </script>
</html>
