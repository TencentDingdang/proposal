该 H5 页面承担的责任是 FM 资源的信息的展示。涉及到播控流程需要按照播控对应的方法进行实现和处理。</br>
 __1.DMSDK__ </br>
接入 DMSDK 保证主账号登入。</br>
(详情：[https://dingdang.qq.com/doc/page/365/](https://dingdang.qq.com/doc/page/365)  __帐号接入__ ）</br>
 __2.接入 URL 地址__ </br>
通过 DMSDK 打开对应得 URL ：</br>
正式环境：</br>
[https://ddsdk.html5.qq.com/v2m/fmControl/](https://ddsdk.html5.qq.com/v2m/musicControl)</br>
体验环境:</br>
[https://ddsdkgray.html5.qq.com/v2m/fmControl/](https://ddsdk.html5.qq.com/v2m/musicControl)</br>
测试环境:</br>
 https://sdk.sparta.html5.qq.com/v2m/fmControl/ </br>
 __3. 点击 H5 页面通讯协议__ 
播放器和播放条需要客户端实现，本说明文档不包含播放器和播放条实现方式。</br>
下面是关于 H5 和 app native 之间的通讯，当在 H5 点击某一个 fm 的资源，需要将当前的资源信息传递给 native 进行处理。这边主要包括：点击具体的某一个首，点击全部播放按钮，取消（全屏的搜索框，需要实现返回）。同时需要同步的是，设备当前播放得资源 id 需要同步给 H5 页面进行显示。</br>
其中通讯的ProxyData协议的可以查看：</br>
Android：https://dingdang.qq.com/doc/page/303</br>
iOS：https://dingdang.qq.com/doc/page/351</br>
下面是具体的协议信息。(这边得通讯方法和定义的字段信息和音乐点播一样，接入音乐点播之后可直接共用)</br>
__（__  __1__  __）播放某一首 FM 资源节目__
#### cmd: DDApi.proxydata 
#### data.action: playMusic 
#### data.data: 
{
sId sPic sAlbumId
sAlbumName
sSingerId
sSingerName
sSongId
sSongName
semantic
}</br>
例子：</br>
 ```json
{"cmd":"DDApi.proxydata","data":{"action":"playMusic","data":{"sId":"1_rd000M9dh94AzeBj","sPic":"http://imgcache.qq.com/fm/photo/album/rmid_album_360/B/j/000M9dh94AzeBj.jpg?time=1533460912","sSongId":"1_rd002vYGDk3luxcr","sSongName":"成长需要时间，可长大只是瞬间","semantic":"{ \"bubble_transform_query\": \"\", \"confidence\": -1, \"domain\": \"fm\", \"extra_semantic\": [ ], \"ifttt_this\":\"\", \"intent\": \"play_show\", \"invocation_name\": \"\", \"is_semantic_only\": true, \"nlu_match_info\": { \"is_single_entity\": true,\"matched_type\": 0 }, \"query\": \"\", \"query_source_type\": 1, \"query_type\": 2, \"session_complete\": false, \"skill_id\": \"\", \"skill_trigger_type\":1, \"slots\": [ { \"confirm_state\": 0, \"json_values\": [ ], \"name\": \"albumid\", \"prompt\": { \"prompt_type\": 0, \"show_text\": \"\", \"slot_name\":\"\", \"slot_type\": \"\", \"speak_text\": \"\" }, \"sInteractionType\": 0, \"sPrompt\": { \"intent_name\": \"\", \"show_text\": \"\", \...114, 100, 48, 48,48, 77, 57, 100, 104, 57, 52, 65, 122, 101, 66, 106, 22, 0, 44, 60, 70, 0, 92 ] ] }, { \"confirm_state\": 0, \"json_values\": [ ], \"name\": \"showid\",\"prompt\": { \"prompt_type\": 0, \"show_text\": \"\", \"slot_name\": \"\", \"slot_type\": \"\", \"speak_text\": \"\" }, \"sInteractionType\": 0,\"sPrompt\": { \"intent_name\": \"\", \"show_text\": \"\", \"skill_id\": \"\", \"slot_name\": \"\", \"slot_options\": \"\", \"slot_type\": \"\",\"speak_text\": \"\" }, \"selectResult\": { \"all_no\": false, \"index\": -1, \"indexes\": [ ], \"type\": 0, \"value\": \"\" }, \"select_state\": 0, \"slot_struct\":1, \"type\": \"\", \"values\": [ [ 6, 18, 49, 95, 114, 100, 48, 48, 50, 118, 89, 71, 68, 107, 51, 108, 117, 120, 99, 114, 22, 0, 44, 60, 70, 0, 92 ] ] } ],\"slots_v2\": [ ], \"type\": 0, \"voice_query\": { \"asr_results\": [ ], \"compress_type\": 1, \"pre_itn_query\": \"\", \"raw_data\": [ ], \"sample_rate\": 8000 } }"}},"id":"10_1564557808278_DDApi.proxydata"}
``` 
__（__  __2__  __）播放全部节目__
#### cmd: DDApi.proxydata
#### data.action: playAllMusic 
data.data:
{ 
sId sPic sAlbumI d 
sAlbumName 
sSingerId 
sSingerName 
sSongId 
sSongName 
}</br>
例子：</br>
  ```json
{"cmd":"DDApi.proxydata","data":{"action":"playAllMusic","data":{"sId":"1_rd000M9dh94AzeBj","sPic":"http://imgcac he.qq.com/fm/photo/album/rmid_album_360/B/j/000M9dh94AzeBj.jpg?time=1533460912","sSongId":"1_rd002vYGDk3luxcr","sSongName":"成长需要时间，可长大只是瞬间","semantic":"{ \"bubble_transform_query\": \"\", \"confidence\": -1, \"domain\": \"fm\", \"extra_semantic\": [ ], \"ifttt_this\": \"\", \"intent\": \"play_show\", \"invocation_name\": \"\", \"is_semantic_only\": true, \"nlu_match_info\": { \"is_single_entity\": true, \"matched_type\": 0 }, \"query\": \"\", \"query_source_type\": 1, \"query_type\": 2, \"session_complete\": false, \"skill_id\": \"\", \"skill_trigger_type\": 1, \"slots\": [ { \"confirm_state\": 0, \"json_values\": [ ], \"name\": \"albumid\", \"prompt\": { \"prompt_type\": 0, \"show_text\": \"\", \"slot_name\": \"\", \"slot_type\": \"\", \"speak_text\": \"\" }, \"sInteractionType\": 0, \"sPrompt\": { \"intent_name\": \"\", \"show_text\": \"\"...114, 100, 48, 48, 48,77, 57, 100, 104, 57, 52, 65, 122, 101, 66, 106, 22, 0, 44, 60, 70, 0, 92 ] ] }, { \"confirm_state\": 0, \"json_values\": [ ], \"name\": \"showid\", \"prompt\":{ \"prompt_type\": 0, \"show_text\": \"\", \"slot_name\": \"\", \"slot_type\": \"\", \"speak_text\": \"\" }, \"sInteractionType\": 0, \"sPrompt\":{ \"intent_name\": \"\", \"show_text\": \"\", \"skill_id\": \"\", \"slot_name\": \"\", \"slot_options\": \"\", \"slot_type\": \"\", \"speak_text\": \"\" },\"selectResult\": { \"all_no\": false, \"index\": -1, \"indexes\": [ ], \"type\": 0, \"value\": \"\" }, \"select_state\": 0, \"slot_struct\": 1, \"type\": \"\",\"values\": [ [ 6, 18, 49, 95, 114, 100, 48, 48, 50, 118, 89, 71, 68, 107, 51, 108, 117, 120, 99, 114, 22, 0, 44, 60, 70, 0, 92 ] ] } ], \"slots_v2\": [ ], \"type\":0, \"voice_query\": { \"asr_results\": [ ], \"compress_type\": 1, \"pre_itn_query\": \"\", \"raw_data\": [ ], \"sample_rate\": 8000 } }"}},"id":"10_1564558064005_DDApi.proxydata"}
 ```
__（__  __3__  __）取消关闭页面（应用在全屏的搜索框，取消按钮）__
#### cmd: DDApi.proxydata"
#### data.action: cancel
例子：</br>
  ```json
{"cmd":"DDApi.proxydata","data":{"action":"cancel","data":""},"id":"10_1555504265707_DDApi.proxydata"}
  ```
 __（__  __4__  __）回调正在播放的节目__ 
#### cmd: DDApi.proxydata"
#### data.action:  __getPlaySongId__ 
需要实现对应的回调函数：_ddSdkCbPlaySong（songId）</br>
将节目的 id，回调给 H5 页面，通知正在播放得页面。同时，播放器和播控条切换节目的时候，也需要调用该回调函数，告知 H5 当前播放的节目 Id。</br>
