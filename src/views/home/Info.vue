<template>
  <div id="postsContainer">
  <div id="posts">
    <div class="each-post">
      <div class="title">
        Leanote Desktop v2.6 released 蚂蚁笔记桌面端2.6发布
      </div>
      <div class="created-time">
        <i class="fa fa-clock-o"></i> 2017-12-01 12:08:14
        &nbsp;&nbsp;
        <span class="fa fa-eye"></span> 2770
        &nbsp;&nbsp;
        <span class="fa fa-thumbs-o-up"></span> 1
        &nbsp;&nbsp;
        <span class="fa fa-comments-o"></span> 13
      </div>
      <div class="mobile-created-time">
        <img src="https://leanote.com/public/upload/520/52d26b4e99c37b609a000001/images/logo/8d8a1e1b0252aa4b11417b25ed87af35.png" id="userLogo">
        leanote
      </div>
      <div class="desc" id="content">
        <p>蚂蚁笔记桌面端2.6发布.</p><p>修复的问题:</p><ul><li>富文本编辑器查找替换高亮问题</li><li>启动有可能一直停留在Loading界面问题</li></ul><p>v2.4及以上版本可线上更新</p><p>下载地址:&nbsp;<a href="http://app.leanote.com/" data-mce-href="http://app.leanote.com">http://app.leanote.com</a></p>
      </div>
      <div class="pre-next-post">
        <p>
          上一篇: 无
        </p>
        <p>
          下一篇: <a href="http://leanote.leanote.com/post/unbind-third-account">如何解绑第三方账号</a>
        </p>
      </div>
      <div class="entry-controls clearfix">
        <div class="vote-section-wrapper clearfix">
          <button class="btn btn-default btn-zan" id="likeBtn"><i class="fa fa-thumbs-o-up"></i> <span id="likeNum">1</span> 赞</button>
          <span class="control-item read-counts"><i class="fa fa-eye"></i> 2770 人读过</span>
        </div>
        <div class="right-section">
          <div id="weixinQRCode"></div>
          <button class="btn btn-share btn-default btn-weibo"><i class="fa fa-weibo"></i> 新浪微博</button>
          <button class="btn btn-share btn-default btn-weixin"><i class="fa fa-wechat"></i> 微信</button>
          <div class="dropdown" style="display: inline-block; cursor: pointer; padding: 5px 10px; padding-right: 30px">
            <div class="dropdown-toggle" data-hover="dropdown" data-toggle="dropdown">
              <i class="fa fa-ellipsis-h"></i>
            </div>
            <ul class="dropdown-menu" role="menu">
              <li><a href="#" class="btn-share tencent-weibo"><i class="fa fa-tencent-weibo"></i> 腾讯微博</a></li>
              <li><a href="#" class="btn-share qq"><i class="fa fa-qq"></i> QQ空间</a></li>
              <li><a href="#" class="btn-share renren"><i class="fa fa-renren"></i> 人人网</a></li>
            </ul>
          </div>
        </div>
        <div class="voters clearfix" id="likers">
          <a id="liker_57f8407bab644107bb00b8b3" title="LoranceChen's Blog" href="http://blog.leanote.com/lorance" target="_blank" class="voter">
            <img alt="avatar" class="avatar-small" src="https://leanote.com/public/upload/619/57f8407bab644107bb00b8b3/images/logo/92e32fac604f6f1b995b8503d68db47f.png">
          </a>
        </div>
      </div>
      <div class="comment-box">
        <form class="comment-form comment-box-ft hide" id="commentForm">
          <div class="clearfix">
            <div class="avatar-wrap">
              <img class="avatar" id="visitUserLogo">
            </div>
            <div class="editor-wrap">
              <textarea class="editable" id="commentContent" name="commentContent" placeholder="评论" style="height: 100px;"></textarea>
            </div>
          </div>
          <div class="command clearfix" style="display: block;">
            <button id="commentBtn" class="reply-comment-btn save btn btn-primary">提交评论</button>
          </div>
        </form>
        <div class="needLogin" id="noLoginContainer">
          <a onclick="goLogin()">立即登录</a>, 发表评论.
          <br>
          没有帐号? <a onclick="goRegister()">立即注册</a>
        </div>
        <div class="box-header"><span class="counter"><i class="icon icon-comment"></i><span id="commentNum">13</span> 条评论</span></div>
         <ul>
          <li class="comment-item">
            <!-- 头像 -->
            <a ui-hovercard="" target="_blank" class="avatar-link" title="kybetter" href="http://cook.leanote.com">
              <img class="avatar" src="https://leanote.com/public/upload/582/56496cd6ab64416568000cbc/images/logo/afa4b5af8bd34acee076a7c6eac3c0b0.jpg">
            </a>
            <!-- 评论 -->
            <div class="comment-body">
              <div class="comment-hd">
                <a href="http://cook.leanote.com" target="_blank">kybetter</a>
                <!-- 回复其它人 -->
              </div>
              <div class="comment-content ng-binding" ng-bind-html="comment.content">
                leanote的服务端在使用go语言开发过程中体验怎么样？与java、node、python和php这几个相比，有什么不一样的地方？
              </div>
              <div class="comment-ft clearfix" data-comment-id="5a29f639ab644138c4000c13">
                <span title="" ui-time="" class="date">2 month ago </span>
                <span class="like-num " title="1 赞"><span class="like-num-i">1</span> 赞</span>
              </div>
            </div>
          </li>
        </ul>
      </div>
      <div id="moreComments">
        <div class="hide comments-more">
          <a>More...</a>
        </div>
        <div class="comments-loading hide">
          <img src="/images/loading-32.gif">
        </div>
      </div>
    </div>
  </div>
    </div>
</template>
<script>
export default {
  name: 'Info'
}
</script>
<style>
  .entry-controls {
    text-align: right;
    padding-top: 20px;
    margin-top: 20px;
    margin-bottom: 10px;
    border-top: 1px solid #f1f2f3;
  }
  .entry-controls .right-section {
    float: right;
    color: #9d9e9f;
  }
  .entry-controls .right-section a {
    color: #9d9e9f;
  }
  .post-menu-button {
    padding-bottom: 10px;
  }
  .ui-menu-button {
    position: relative;
    display: inline-block;
    cursor: pointer;
  }
  .entry-controls .control-item {
    margin-left: 15px;
    color: #9d9e9f;
    font-size: 15px;
    opacity: 1;
    -webkit-transition: all 0.05s ease-in-out;
    -moz-transition: all 0.05s ease-in-out;
    -o-transition: all 0.05s ease-in-out;
    transition: all 0.05s ease-in-out;
  }
  .vote-section-wrapper {
    display: inline-block;
    float: left;
  }
  .entry-controls .voters {
    display: block;
    margin-top: 52px;
    height: 25px;
    clear: both;
  }
  .entry-controls .voters .more-voters,
  .entry-controls .voters .voter {
    width: 25px;
    height: 25px;
    position: relative;
    margin: 0 8px 8px 0;
    float: left;
  }
  .entry-controls .voters .voter > img {
    float: left;
  }
  .avatar-small {
    width: 25px;
    height: 25px;
    border-radius: 50%;
  }
  .comment-box {
    margin: 0;
    padding: 0;
    font-size: 16px;
  }
  .comment-box a {
    font-size: 16px;
  }
  .comment-box .box-header {
    border-top: 1px solid #f1f2f3;
    font-size: 15px;
    color: #9d9e9f;
    padding: 30px 0 10px;
    position: relative;
  }
  .comment-box .box-header .icon {
    margin-right: 8px;
    vertical-align: -3px;
  }
  .comment-box .box-header a.comment-options {
    margin-left: 10px;
  }
  @media screen and (max-width: 600px) {
    .comment-box .box-header {
      padding-left: 17px;
      padding-right: 17px;
    }
  }
  .comment-box .load-more {
    height: 26px;
    margin-top: 15px;
    padding-top: 24px;
    text-align: center;
    font-size: 15px;
    border-top: solid 1px #f1f2f3;
  }
  .comment-box .load-more a {
    color: #9d9e9f;
  }
  .comment-box .ui-spinner {
    margin: 0 auto;
  }
  .comment-box .ui-spinner.small {
    position: relative;
    left: 10px;
  }
  .comment-box.empty.cannot-comment {
    border: 1px solid #dddddd;
  }
  .comment-box.cannot-comment .editable,
  .comment-box.cannot-comment .editable,
  .comment-box.comment-box.cannot-comment .command,
  .comment-box.comment-box.cannot-comment .op-link.reply {
    display: none !important;
  }
  .comment-box.empty.cannot-comment .comment-form {
    margin: 0;
  }
  .comment-box.empty.cannot-comment .comment-box-ft {
    background: #ffffff;
  }
  .comment-box.empty.cannot-comment .comment-box-ft,
  .comment-box .comment-box-ft {
    position: relative;
    margin-top: 0px;
  }
  .comment-box .avatar {
    width: 40px;
    height: 40px;
    border-radius: 20px;
    float: left;
  }
  .comment-box .message {
    margin-top: 24px;
    padding: 10px;
    border-radius: 4px;
    text-align: center;
    background: #F7F8F9;
    color: #9d9e9f;
  }
  .comment-item {
    position: relative;
    list-style: none;
    outline: 0;
    padding: 15px 0;
    border-bottom: solid 1px #f1f2f3;
  }
  .item-highlight * {
    border-radius: 5px;
    font-weight: bold;
  }
  @media screen and (max-width: 600px) {
    .comment-item {
      padding-left: 17px;
      padding-right: 17px;
    }
  }
  .comment-item > .avatar-link {
    float: left;
    margin: 4px 0 0;
  }
  .comment-item > .comment-body {
    margin: 0 0 0 60px;
  }
  .comment-item .comment-content {
    min-height: 22px;
    font-size: 15px;
    word-wrap: break-word;
    padding: 5px 0;
  }
  .comment-item .comment-hd,
  .comment-item .comment-ft {
    color: #9d9e9f;
  }
  .comment-item .comment-hd .desc,
  .comment-item .comment-ft .desc {
    font-size: 15px;
  }
  .comment-item .comment-ft {
    font-size: 15px;
  }
  .comment-item .op-link {
    color: #9d9e9f;
    font-size: 15px;
    margin-left: 12px;
  }
  .comment-item .op-link {
    visibility: hidden;
  }
  @media screen and (max-width: 420px) {
    .comment-item .op-link .icon {
      display: none;
    }
  }
  .comment-item .like-num {
    float: right;
  }
  .comment-item .like-num.nil {
    display: none;
  }
  .comment-item:hover .op-link {
    visibility: visible;
  }
  .comment-form.comment-reply-form {
    padding: 20px 0;
  }
  .comment-form .row {
    margin: 0;
  }
  .comment-form .editable {
    padding: 6px 12px;
    font-size: 16px;
    min-height: 18px;
    line-height: 26px;
    white-space: pre-wrap;
    width: 100%;
    color: #222;
    cursor: text;
    border: 1px solid #DDD;
    border-radius: 4px;
    box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05) inset;
    background: #e6eaed;
    color: #747f8c;
  }
  #commentForm {
    border-top: solid 1px #f1f2f3;
    padding: 10px 0;
  }
  .comment-form .editable:focus {
    outline: none;
    border: 1px solid #cccccc;
  }
  .comment-form > .command {
    display: none;
    margin-top: 20px;
    padding-bottom: 0;
    text-align: right;
  }
  .comment-form > .command .save {
    float: right;
  }
  .comment-form > .command .cancel {
    color: #9d9e9f;
    vertical-align: -7px;
    margin-right: 10px;
  }
  .comment-form.expanded .command {
    display: block;
  }
  .comment-form > .avatar + .editable {
    margin-left: 60px;
  }
  #comments {
    padding: 0;
  }
  #comments form {
    display: none;
    margin-top: 5px;
  }
  @media screen and (max-width: 600px) {
    .comment-form {
      padding-left: 17px;
      padding-right: 17px;
    }
  }
  .btn-zan {
    border-radius: 50px;
  }
  .btn-weibo {
    border-radius: 50px;
    color: #d44137;
    border-color: #d44137;
  }
  .btn-weibo:hover {
    color: #fff;
    background: #d44137;
  }
  .btn-weixin {
    color: #38ad5a;
    border-color: #38ad5a;
    border-radius: 50px;
  }
  .btn-weixin:hover {
    color: #fff;
    background: #38ad5a;
  }
  .reply-comment-btn {
    width: 100px;
  }
  .avatar-wrap {
    float: left;
  }
  .editor-wrap {
    margin-left: 60px;
  }
  #weixinQRCode {
    text-align: center;
  }
  .report-form ul {
    margin: 0;
    padding: 0;
  }
  .report-form .options > li {
    list-style: none;
    display: block;
    line-height: 2;
    color: #666768;
  }
  .report-form .options input {
    margin-right: 10px;
    vertical-align: 1px;
  }
  .footnote {
    color: red;
  }
  #moreComments {
    padding: 20px 0;
    text-align: center;
  }
  .needLogin {
    padding: 20px 0;
    text-align: center;
    font-size: 18px;
    border-top: 1px solid #f1f2f3;
  }
  .needLogin a {
    font-size: 18px;
  }
</style>
