---
title: 会話の追跡
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: '最終更新日: 2011 年 7 月 23 日'
localization_priority: Priority
ms.openlocfilehash: 3a59a7a15b4647832634adc4757544876b8841b1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706222"
---
# <a name="tracking-conversations"></a>会話の追跡

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
会話の追跡とは、メッセージに対する応答を収集することです。クライアントでは、会話の追跡に役立つ次の 2 つのプロパティを設定する必要があります。
  
- **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))
    
    **PR_CONVERSATION_TOPIC** は、メッセージの正規化された件名 (プレフィックス文字列のない件名) です。 このプロパティは、メッセージの **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) プロパティの値に設定します。 
    
- **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))
    
    **PR_CONVERSATION_INDEX**�ł́A����̃X���b�h��ŁA���b�Z�[�W�̈ʒu������܂��B�V�������b�Z�[�W�A�]�����ꂽ���b�Z�[�W�A�܂��͕ԐM���邩�ǂ����́A���M���b�Z�[�W���Ƃ� **PR_CONVERSATION_INDEX**��ݒ肷��ڋq�� reponsibility ���܂��B�N���C�A���g�ł́A�蓮�ł��̃v���p�e�B��ݒ肵����A [ScCreateConversationIndex](sccreateconversationindex.md)�AMAPI �ɂ���Ē񋟂���郆�[�e�B���e�B����Ăяo�����Ƃ��ł��܂��B 
    
 **ScCreateConversationIndex**�ɂ́A���ׂĂ̑��M���b�Z�[�W�̃X���b�h �C���f�b�N�X�̒l����������܂��B **ScCreateConversationIndex**�w�b�_�[�̃u���b�N�̒����A0 ������ 22 �o�C�g�Ƃ��āA�C���f�b�N�X���������܂��͂��̑��̎q���e 5 �o�C�g�̒�����u���b�N���܂��B 
  
�w�b�_�[�̃u���b�N 22 �o�C�g�A�g�݂� 3 �̕����ō\������܂��B
  
- 1 �͗\��o�C�g�ł��B���̒l�� 1 �ł��B
    
- �V�X�e���̌��݂̎����� 5 �o�C�g�́A [FILETIME](filetime.md)�\���`���ɕϊ����܂��B 
    
- 16 バイトを保持する [GUID](guid.md) (グローバル一意識別子)。
    
�e�q�u���b�N 5 �o�C�g�A���̂悤�ɕ����ō\������܂��B
  
- 1 �r�b�g���A���݂̎����ƁA�w�b�_�[�̃u���b�N�Ɋi�[����Ă��鎞�Ԃ̍��ق�\���R�[�h���܂܂�Ă��܂��B���� 2 �ڂ� 2 �N�ԂƂ̍��� 1 �b�����ł���ꍇ�� 1 ���傫�� 56 �N�𒴂���.02 �����ł���ꍇ�́A���̃r�b�g�� 0 �ɂȂ�܂��B
    
- 30 �̂����ꂩ�̃r�b�g�� **FILETIME**�P�ʂŃw�b�_�[�̃u���b�N�̌��݂̎����Ǝ��Ԃ̈Ⴂ���܂܂�Ă��܂��B�ŏ��̃r�b�g�̒l�ɉ����āA2 �̕��@�̂����ꂩ��g�p���Ďq�u���b�N�̂��̕�������������܂��B���̃r�b�g�� 0 �̏ꍇ�́A��� 15 �r�b�g�Ɖ��� 18 �r�b�g **ScCreateConversationIndex**��j�����܂��B���̃r�b�g�� 1 �̏ꍇ�́A���̊��́A��� 10 �r�b�g�Ɖ��� 23 �r�b�g��j�����܂��B 
    
- 4 �r�b�g��[GetTickCount](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx)Win32 ����Ăяo���ɂ���Đ��������A�����_���Ȕԍ����܂܂�Ă��܂��B
    
- �V�[�P���X��܂� 4 �r�b�g�̐��̓����_���Ȕԍ��̕�������擾�������܂��B
    
���b�Z�[�W�̃X���b�h �C���f�b�N�X��蓮�Őݒ肷��ꍇ�́A���̓_��l�����Ă��������B
  
1. �񓚎҂̃^�C�� �]�[���ł̑���_�𓧖��ɕێ����܂��B���n���Ԃł͂Ȃ��AUTC ������g�p���܂��B
    
2. �����傫���Ŋe�X���b�h�̃O���[�v�ɃC���f���g��ݒ肵�܂��B
    
3. �������b�Z�[�W�̓��t�ւ̕ԐM����בւ��܂��B
    
4. �����g�s�b�N�̋��L�ɖ�肪��������ʂ̎����ɕʂ̃X���b�h��J�n���܂��B 
    
5. メッセージがトピックごとにグループ化されるようにする分類別の並べ替えを実装するには、最初に **PR_CONVERSATION_TOPIC** で並べ替えてから、**PR_CONVERSATION_INDEX** で並べ替えます。 並べ替えの結果を表示するには、22 バイト長の会話インデックスを持つメッセージの **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) プロパティを 0 に設定します。 その後で、5 バイト長ずつ増加するたびに、**PR_DEPTH** プロパティの値を 1 増やします。 
    
プロパティの PR_ORIGINAL グループは、会話の追跡にも使用できます。 これらのプロパティを設定して、元のメッセージへの返信メッセージまたは転送メッセージをリンクします。 PR_ORIGINAL のすべてのプロパティは省略可能です。 たとえば、**PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)) を明示的に設定していない場合、メッセージ ストア プロバイダーは既定の値 (**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) プロパティの値) を使用できます。 同様に、**PR_ORIGINAL_AUTHOR_NAME** または **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)) を設定していない場合、これらのプロパティには、**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) プロパティと **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) プロパティの値がそれぞれの既定値として設定されます。 
  

