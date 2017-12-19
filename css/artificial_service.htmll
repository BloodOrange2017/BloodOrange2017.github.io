<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>首页</title>
    <meta name="author" content="">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black">
    <meta name="format-detection" content="telephone=no">
    <meta http-equiv="content-type" content="text/html;charset=utf-8">
    <meta http-equiv="Expires" CONTENT="-1">
    <meta http-equiv="Cache-Control" CONTENT="no-cache">
   <!--  <link rel="stylesheet" type="text/css" href="https://bloodorange2017.github.io/css/chat/index.css" /> -->
    <link rel="stylesheet" type="text/css" href="https://bloodorange2017.github.io/css/artificial_css.css" />
</head>

<body>
    <div class="chat-container">
        <div class="chat-top-wrap">
            <div class="chat-board-wrap">
                <div class="chat-board-main">
                    <div class="dropload-load"><span class="loading"></span>加载中...</div>
                    <div class="js-main-board">
                        <div class="js-old-wrap">
                            <div class="chat-board-item"></div>
                        </div>
                        <div class="js-evaluate-wrap">
                            <ul class="chat-board-subItem clearfix"></ul>
                        </div>
                        <div class="js-today-wrap">
                            <div class="chat-board-item">
                                <ul class="chat-board-subItem clearfix"></ul>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="chat-btm-wrap clearfix">
            <div class="chat-comment-box">
                <textarea class="chat-textarea" placeholder="请在此输入..." maxlength="100"></textarea>
            </div>
            <div class="chat-btn-wrap">
                <p class="fl chat-error-tips"></p>
                <a href="javascript:;" class="fr chat-icons chat-send-btn"></a>
                <p class="fr chat-count-wrap">字数 <span class="js-num-count">0</span>/100</p>
            </div>
        </div>
    </div>
</body>
<script type="text/javascript" src="https://bloodorange2017.github.io/css/artificial_js.jss"></script>
<script type="text/x-handlebars-template" id="itemTpl">
    <li class="it {{#equal source 2}}chat-board-custom{{/equal}} {{#equal send_user_type 4}}chat-board-custom{{/equal}} {{#equal source 1}}chat-board-user{{/equal}} {{#if isShowTips}}chat-send-error{{/if}} clearfix" data-id="{{sn}}">
        <div class="chat-main-fluid">
            <div class="chat-item-inner clearfix">
                <div class="chat-info-wrap clearfix">
                    <div class="name">{{user_name}}</div>
                    <div class="date">{{time}}</div>
                    <div class="error clearfix">
                        <i class="fl chat-icons"></i>
                        <u class="fl">消息发送失败</u>
                    </div>
                </div>
                <div class="chat-cont-wrap clearfix">
                    <div>{{{contents}}}</div>
                    {{#if robot}}
                    <div class="chat-question-main">
                        {{#each robot}}
                        <p class="chat-question-link">
                            <a href="javascript:;" data-answer="{{answer}}" {{#if isCustom}}data-type="custom" {{/if}} data-brain="false" nt="qa-question-btn">{{question}}</a>
                        </p>
                        {{/each}}
                    </div>
                    {{/if}} {{#if evaluate}}
                    <div class="chat-question-main">
                        {{#each evaluate}}
                        <p class="chat-question-link">
                            <a href="javascript:;" data-id="{{ID}}" data-session="{{../msg_session_id}}" data-name="{{../user_name}}" nt="evaluate-btn">{{VALUE}}</a>
                        </p>
                        {{/each}}
                    </div>
                    {{/if}} {{#if reason}}
                    <div class="chat-question-main">
                        {{#each reason}}
                        <p class="chat-question-link">
                            <a href="javascript:;" data-id="{{ID}}" data-level="{{../satisfaction_level}}" data-session="{{../msg_session_id}}" data-name="{{../user_name}}" nt="reason-btn">{{VALUE}}</a>
                        </p>
                        {{/each}}
                    </div>
                    {{/if}}
                </div>
            </div>
        </div>
        <div class="chat-user-header">
            {{#equal source 2}}
            <img src="https://bloodorange2017.github.io/images/kefu.jpg" width="100%" /> {{/equal}} {{#equal source 4}}
            <img src="https://bloodorange2017.github.io/images/kefu.jpg" width="100%" /> {{/equal}} {{#equal source 1}} {{#equal jobs_id '10'}}
            <img src="https://bloodorange2017.github.io/images/guijian.png" width="100%" /> {{/equal}} {{#equal jobs_id '20'}}
            <img src="https://bloodorange2017.github.io/images/nanqiang.png" width="100%" /> {{/equal}} {{#equal jobs_id '30'}}
            <img src="https://bloodorange2017.github.io/images/mofashi.png" width="100%" /> {{/equal}} {{#equal jobs_id '50'}}
            <img src="https://bloodorange2017.github.io/images/shenqiang.png" width="100%" /> {{/equal}} {{/equal}}
        </div>
    </li>
</script>
<script type="text/x-handlebars-template" id="historyTpl">
    <ul class="chat-board-subItem chat-history-subItem clearfix">
        {{#each list}}
        <li class="it {{#equal send_user_type 2}}chat-board-custom{{/equal}} {{#equal send_user_type 4}}chat-board-custom{{/equal}} {{#equal send_user_type 1}}chat-board-user{{/equal}} clearfix">
            <div class="chat-main-fluid">
                <div class="chat-item-inner clearfix">
                    <div class="chat-info-wrap clearfix">
                        <div class="name">{{send_user_name}}</div>
                        <div class="date">{{formatTime timestamp}}</div>
                    </div>
                    <div class="chat-cont-wrap clearfix">
                        <div>{{{msg_content}}}</div>
                    </div>
                </div>
            </div>
            <div class="chat-user-header">
                {{#equal send_user_type 2}}
                <img src="https://bloodorange2017.github.io/images/kefu.jpg" width="100%" /> {{/equal}} {{#equal send_user_type 4}}
                <img src="https://bloodorange2017.github.io/images/kefu.jpg" width="100%" /> {{/equal}} {{#equal send_user_type 1}} {{#equal jobs_id '10'}}
                <img src="https://bloodorange2017.github.io/images/guijian.png" width="100%" /> {{/equal}} {{#equal jobs_id '20'}}
                <img src="https://bloodorange2017.github.io/images/nanqiang.png" width="100%" /> {{/equal}} {{#equal jobs_id '30'}}
                <img src="https://bloodorange2017.github.io/images/mofashi.png" width="100%" /> {{/equal}} {{#equal jobs_id '50'}}
                <img src="https://bloodorange2017.github.io/images/shenqiang.png" width="100%" /> {{/equal}} {{/equal}}
            </div>
        </li>
        {{/each}}
    </ul>
</script>
<script type="text/x-handlebars-template" id="evaluateTpl">
    <li class="it chat-board-custom clearfix">
        <div class="chat-main-fluid">
            <div class="chat-item-inner clearfix">
                <div class="chat-info-wrap clearfix">
                    <div class="name">{{supporter_user_name}}</div>
                    <div class="date">{{formatTime time}}</div>
                </div>
                <div class="chat-cont-wrap clearfix">
                    <div>{{{contents}}}</div>
                    {{#equal step 0}}
                    <div class="chat-question-main">
                        {{#each evaluate}}
                        <p class="chat-question-link">
                            <a href="javascript:;" data-id="{{ID}}" data-session="{{../msg_session_id}}" data-name="{{../supporter_user_name}}" nt="evaluate-btn">{{VALUE}}</a>
                        </p>
                        {{/each}}
                    </div>
                    {{/equal}} {{#equal step 1}}
                    <div class="chat-question-main">
                        {{#each reason}}
                        <p class="chat-question-link">
                            <a href="javascript:;" data-id="{{ID}}" data-level="{{../satisfaction_level}}" data-session="{{../msg_session_id}}" data-name="{{../supporter_user_name}}" nt="reason-btn">{{VALUE}}</a>
                        </p>
                        {{/each}}
                    </div>
                    {{/equal}}
                </div>
            </div>
        </div>
        <div class="chat-user-header">
            <img src="https://bloodorange2017.github.io/images/kefu.jpg" width="100%" />
        </div>
    </li>
</script>

</html>