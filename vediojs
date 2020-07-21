 var options = {
        width: 680,
        height: 360
    }
    var player = videojs('live-stream', options);
    player.play();

    player.addClass('vjs-matrix');

    player.on(['loadstart', 'play', 'playing', 'firstplay', 'pause', 'ended', 'adplay', 'adplaying', 'adfirstplay', 'adpause', 'adended', 'contentplay', 'contentplaying', 'contentfirstplay', 'contentpause', 'contentended', 'contentupdate'], function (e) {
//        console.warn('VIDEOJS player event: ', e.type);
//        if(e.type == "play"){
//            console.log('开始播放');
//        }else if(e.type == "playing"){
//            console.log('正在播放...');
//        }else if(e.type == "pause"){
//            console.log('暂停视频播放');
//        }else if(e.type == "firstplay"){
//            console.log('firstplay播放');
//        }else{
//            console.log('1111111111111');
//        }
    });
    player.one('canplay', function() {
        console.log('player11111111111111');
    });
    console.log("暂停播放测哦错"+player.pause())
    console.log("暂停播放测哦错"+player.currentTime())
    /**
     * 获取状态
     * state值：1.playing播放中 2.paused停止 3.idle空闲 4. completed结束
     */
    $('.player-status').click(function () {
        var state = player.getState();
        console.log(state);
        var msg;
        switch (state){
            case 'buffering':
                msg = '加载中...';
                break;
            case 'playing':
                msg = '播放中...';
                break;
            case 'paused':
                msg = '暂停';
                break;
            case 'idle':
                msg = '停止';
                break;
            case 'completed':
                msg = '结束';
                break;
        }
        alert(msg);
    });
    //停止
    $('.player-stop').click(function () {
        player.pause();
    });
    //播放
    $('.player-play').click(function () {
       console.log('11111111'+ player.currentTime());
    });
