�� H5 ҳ��е��������� FM ��Դ����Ϣ��չʾ���漰������������Ҫ���ղ��ض�Ӧ�ķ�������ʵ�ֺʹ���
 __1.DMSDK__ 
���� DMSDK ��֤���˺ŵ��롣
(���飺[https://dingdang.qq.com/doc/page/365/](https://dingdang.qq.com/doc/page/365)  __�ʺŽ���__ ��
 __2.���� URL ��ַ__ 
ͨ�� DMSDK �򿪶�Ӧ�� URL ��
��ʽ������
[https://ddsdk.html5.qq.com/v2m/fmControl/](https://ddsdk.html5.qq.com/v2m/musicControl)
���黷��:
[https://ddsdkgray.html5.qq.com/v2m/fmControl/](https://ddsdk.html5.qq.com/v2m/musicControl)
���Ի���:
 https://sdk.sparta.html5.qq.com/v2m/fmControl/ 
 __3. ��� H5 ҳ��ͨѶЭ��__ 
�������Ͳ�������Ҫ�ͻ���ʵ�֣���˵���ĵ��������������Ͳ�����ʵ�ַ�ʽ��
�����ǹ��� H5 �� app native ֮���ͨѶ������ H5 ���ĳһ�� fm ����Դ����Ҫ����ǰ����Դ��Ϣ���ݸ� native ���д��������Ҫ��������������ĳһ���ף����ȫ�����Ű�ť��ȡ����ȫ������������Ҫʵ�ַ��أ���ͬʱ��Ҫͬ�����ǣ��豸��ǰ���ŵ���Դ id ��Ҫͬ���� H5 ҳ�������ʾ��
����ͨѶ��ProxyDataЭ��Ŀ��Բ鿴��
Android��https://dingdang.qq.com/doc/page/303
iOS��https://dingdang.qq.com/doc/page/351
�����Ǿ����Э����Ϣ��(��ߵ�ͨѶ�����Ͷ�����ֶ���Ϣ�����ֵ㲥һ�����������ֵ㲥֮���ֱ�ӹ���)
__��__  __1__  __������ĳһ�� FM ��Դ��Ŀ__
####cmd: DDApi.proxydata 
####data.action: playMusic 
####data.data: 
{
sId sPic sAlbumId
sAlbumName
sSingerId
sSingerName
sSongId
sSongName
semantic
}
���ӣ�
 ```json
[{"cmd":"DDApi.proxydata","data":{"action":"playMusic","data":{"sId":"1_rd000M9dh94AzeBj","sPic":"http://imgcache.qq.com/fm/photo/album/rmid_album_360/B/j/000M9dh94AzeBj.jpg?time=1533460912","sSongId":"1_rd002vYGDk3luxcr","sSongName":"�ɳ���Ҫʱ�䣬�ɳ���ֻ��˲��","semantic":"{ \"bubble_transform_query\": \"\", \"confidence\": -1, \"domain\": \"fm\", \"extra_semantic\": [ ], \"ifttt_this\":\"\", \"intent\": \"play_show\", \"invocation_name\": \"\", \"is_semantic_only\": true, \"nlu_match_info\": { \"is_single_entity\": true,\"matched_type\": 0 }, \"query\": \"\", \"query_source_type\": 1, \"query_type\": 2, \"session_complete\": false, \"skill_id\": \"\", \"skill_trigger_type\":1, \"slots\": [ { \"confirm_state\": 0, \"json_values\": [ ], \"name\": \"albumid\", \"prompt\": { \"prompt_type\": 0, \"show_text\": \"\", \"slot_name\":\"\", \"slot_type\": \"\", \"speak_text\": \"\" }, \"sInteractionType\": 0, \"sPrompt\": { \"intent_name\": \"\", \"show_text\": \"\", \...114, 100, 48, 48,48, 77, 57, 100, 104, 57, 52, 65, 122, 101, 66, 106, 22, 0, 44, 60, 70, 0, 92 ] ] }, { \"confirm_state\": 0, \"json_values\": [ ], \"name\": \"showid\",\"prompt\": { \"prompt_type\": 0, \"show_text\": \"\", \"slot_name\": \"\", \"slot_type\": \"\", \"speak_text\": \"\" }, \"sInteractionType\": 0,\"sPrompt\": { \"intent_name\": \"\", \"show_text\": \"\", \"skill_id\": \"\", \"slot_name\": \"\", \"slot_options\": \"\", \"slot_type\": \"\",\"speak_text\": \"\" }, \"selectResult\": { \"all_no\": false, \"index\": -1, \"indexes\": [ ], \"type\": 0, \"value\": \"\" }, \"select_state\": 0, \"slot_struct\":1, \"type\": \"\", \"values\": [ [ 6, 18, 49, 95, 114, 100, 48, 48, 50, 118, 89, 71, 68, 107, 51, 108, 117, 120, 99, 114, 22, 0, 44, 60, 70, 0, 92 ] ] } ],\"slots_v2\": [ ], \"type\": 0, \"voice_query\": { \"asr_results\": [ ], \"compress_type\": 1, \"pre_itn_query\": \"\", \"raw_data\": [ ], \"sample_rate\": 8000 } }"}},"id":"10_1564557808278_DDApi.proxydata"}]
``` 
__��__  __2__  __������ȫ����Ŀ__
####cmd: DDApi.proxydata
####data.action: playAllMusic 
####data.data:
{ 
sId sPic sAlbumI d 
sAlbumName 
sSingerId 
sSingerName 
sSongId 
sSongName 
}
���ӣ�
  ```json
[{"cmd":"DDApi.proxydata","data":{"action":"playAllMusic","data":{"sId":"1_rd000M9dh94AzeBj","sPic":"http://imgcac he.qq.com/fm/photo/album/rmid_album_360/B/j/000M9dh94AzeBj.jpg?time=1533460912","sSongId":"1_rd002vYGDk3luxcr","sSongName":"�ɳ���Ҫʱ�䣬�ɳ���ֻ��˲��","semantic":"{ \"bubble_transform_query\": \"\", \"confidence\": -1, \"domain\": \"fm\", \"extra_semantic\": [ ], \"ifttt_this\": \"\", \"intent\": \"play_show\", \"invocation_name\": \"\", \"is_semantic_only\": true, \"nlu_match_info\": { \"is_single_entity\": true, \"matched_type\": 0 }, \"query\": \"\", \"query_source_type\": 1, \"query_type\": 2, \"session_complete\": false, \"skill_id\": \"\", \"skill_trigger_type\": 1, \"slots\": [ { \"confirm_state\": 0, \"json_values\": [ ], \"name\": \"albumid\", \"prompt\": { \"prompt_type\": 0, \"show_text\": \"\", \"slot_name\": \"\", \"slot_type\": \"\", \"speak_text\": \"\" }, \"sInteractionType\": 0, \"sPrompt\": { \"intent_name\": \"\", \"show_text\": \"\"...114, 100, 48, 48, 48,77, 57, 100, 104, 57, 52, 65, 122, 101, 66, 106, 22, 0, 44, 60, 70, 0, 92 ] ] }, { \"confirm_state\": 0, \"json_values\": [ ], \"name\": \"showid\", \"prompt\":{ \"prompt_type\": 0, \"show_text\": \"\", \"slot_name\": \"\", \"slot_type\": \"\", \"speak_text\": \"\" }, \"sInteractionType\": 0, \"sPrompt\":{ \"intent_name\": \"\", \"show_text\": \"\", \"skill_id\": \"\", \"slot_name\": \"\", \"slot_options\": \"\", \"slot_type\": \"\", \"speak_text\": \"\" },\"selectResult\": { \"all_no\": false, \"index\": -1, \"indexes\": [ ], \"type\": 0, \"value\": \"\" }, \"select_state\": 0, \"slot_struct\": 1, \"type\": \"\",\"values\": [ [ 6, 18, 49, 95, 114, 100, 48, 48, 50, 118, 89, 71, 68, 107, 51, 108, 117, 120, 99, 114, 22, 0, 44, 60, 70, 0, 92 ] ] } ], \"slots_v2\": [ ], \"type\":0, \"voice_query\": { \"asr_results\": [ ], \"compress_type\": 1, \"pre_itn_query\": \"\", \"raw_data\": [ ], \"sample_rate\": 8000 } }"}},"id":"10_1564558064005_DDApi.proxydata"}]
 ```
__��__  __3__  __��ȡ���ر�ҳ�棨Ӧ����ȫ����������ȡ����ť��__
####cmd: DDApi.proxydata"
####data.action: cancel
���ӣ�
  ```json
[{"cmd":"DDApi.proxydata","data":{"action":"cancel","data":""},"id":"10_1555504265707_DDApi.proxydata"}]
  ```
 __��__  __4__  __���ص����ڲ��ŵĽ�Ŀ__ 
####cmd: DDApi.proxydata"
####data.action:  __getPlaySongId__ 
��Ҫʵ�ֶ�Ӧ�Ļص�������_ddSdkCbPlaySong��songId��
����Ŀ�� id���ص��� H5 ҳ�棬֪ͨ���ڲ��ŵ�ҳ�档ͬʱ���������Ͳ������л���Ŀ��ʱ��Ҳ��Ҫ���øûص���������֪ H5 ��ǰ���ŵĽ�Ŀ Id��
