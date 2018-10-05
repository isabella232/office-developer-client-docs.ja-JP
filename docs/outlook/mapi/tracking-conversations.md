---
title: ��b��Ǘ����܂��B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7f1dd7a23bbd643b496b7634b6ad0230c806585f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398606"
---
# <a name="tracking-conversations"></a>��b��Ǘ����܂��B

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
��b����́A���b�Z�[�W�ɑ΂���ԐM����W���Ă��܂��B�N���C�A���g�́A��b�̊Ǘ��ɖ𗧂� 2 �̃v���p�e�B��ݒ肷��K�v������܂��B
  
- **PR_CONVERSATION_TOPIC**([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))
    
    **PR_CONVERSATION_TOPIC**は、正規化されたプレフィックス文字列のない件名、メッセージの件名です。 メッセージの**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) のプロパティの値にこのプロパティを設定します。 
    
- **PR_CONVERSATION_INDEX**([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))
    
    **PR_CONVERSATION_INDEX**�ł́A����̃X���b�h��ŁA���b�Z�[�W�̈ʒu������܂��B�V�������b�Z�[�W�A�]�����ꂽ���b�Z�[�W�A�܂��͕ԐM���邩�ǂ����́A���M���b�Z�[�W���Ƃ� **PR_CONVERSATION_INDEX**��ݒ肷��ڋq�� reponsibility ���܂��B�N���C�A���g�ł́A�蓮�ł��̃v���p�e�B��ݒ肵����A [ScCreateConversationIndex](sccreateconversationindex.md)�AMAPI �ɂ���Ē񋟂���郆�[�e�B���e�B�֐���Ăяo�����Ƃ��ł��܂��B 
    
 **ScCreateConversationIndex**�ɂ́A���ׂĂ̑��M���b�Z�[�W�̃X���b�h �C���f�b�N�X�̒l����������܂��B **ScCreateConversationIndex**�w�b�_�[�̃u���b�N�̒����A0 ������ 22 �o�C�g�Ƃ��āA�C���f�b�N�X���������܂��͂��̑��̎q���e 5 �o�C�g�̒�����u���b�N���܂��B 
  
�w�b�_�[�̃u���b�N 22 �o�C�g�A�g�݂� 3 �̕����ō\������܂��B
  
- 1 �͗\��o�C�g�ł��B���̒l�� 1 �ł��B
    
- �V�X�e���̌��݂̎����� 5 �o�C�g�́A [FILETIME](filetime.md)�\���`���ɕϊ����܂��B 
    
- 16 バイトの[GUID](guid.md)、またはグローバルに一意の識別子を保持します。
    
�e�q�u���b�N 5 �o�C�g�A���̂悤�ɕ����ō\������܂��B
  
- 1 �r�b�g���A���݂̎����ƁA�w�b�_�[�̃u���b�N�Ɋi�[����Ă��鎞�Ԃ̍��ق�\���R�[�h���܂܂�Ă��܂��B���� 2 �ڂ� 2 �N�ԂƂ̍��� 1 �b�����ł���ꍇ�� 1 ���傫�� 56 �N�𒴂���.02 �����ł���ꍇ�́A���̃r�b�g�� 0 �ɂȂ�܂��B
    
- 30 �̂����ꂩ�̃r�b�g�� **FILETIME**�P�ʂŃw�b�_�[�̃u���b�N�̌��݂̎����Ǝ��Ԃ̈Ⴂ���܂܂�Ă��܂��B�ŏ��̃r�b�g�̒l�ɉ����āA2 �̕��@�̂����ꂩ��g�p���Ďq�u���b�N�̂��̕�������������܂��B���̃r�b�g�� 0 �̏ꍇ�́A��� 15 �r�b�g�Ɖ��� 18 �r�b�g **ScCreateConversationIndex**��j�����܂��B���̃r�b�g�� 1 �̏ꍇ�́A���̊֐��́A��� 10 �r�b�g�Ɖ��� 23 �r�b�g��j�����܂��B 
    
- 4 �r�b�g��[GetTickCount](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx)Win32 �֐���Ăяo���ɂ���Đ��������A�����_���Ȕԍ����܂܂�Ă��܂��B
    
- �V�[�P���X��܂� 4 �r�b�g�̐��̓����_���Ȕԍ��̕�������擾�������܂��B
    
���b�Z�[�W�̃X���b�h �C���f�b�N�X��蓮�Őݒ肷��ꍇ�́A���̓_��l�����Ă��������B
  
1. �񓚎҂̃^�C�� �]�[���ł̑���_�𓧖��ɕێ����܂��B���n���Ԃł͂Ȃ��AUTC ������g�p���܂��B
    
2. �����傫���Ŋe�X���b�h�̃O���[�v�ɃC���f���g��ݒ肵�܂��B
    
3. �������b�Z�[�W�̓��t�ւ̕ԐM����בւ��܂��B
    
4. �����g�s�b�N�̋��L�ɖ�肪��������ʂ̎����ɕʂ̃X���b�h��J�n���܂��B 
    
5. メッセージは、トピック別にグループ化されるように分類された並べ替えを実装するには、最初**PR_CONVERSATION_TOPIC**と**PR_CONVERSATION_INDEX**を並べ替えます。 並べ替えの結果を表示するには、22 バイトの長さである会話のインデックスを持つメッセージの場合は 0 に、 **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) プロパティを設定します。 長さの 5 バイト単位ごとの 1 つで**PR_DEPTH**プロパティの値をインクリメントします。 
    
プロパティの PR_ORIGINAL グループは、会話の追跡にも使用できます。 元のメッセージに返信または転送メッセージをリンクするのにはこれらのプロパティを設定します。 すべての PR_ORIGINAL プロパティは、オプションです。 既定値、または**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) の値にメッセージ ストア プロバイダーが使用できる場合は明示的に設定しない、たとえば、 **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md))プロパティです。 同様に、 **PR_ORIGINAL_AUTHOR_NAME**または**PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)) が設定されていない場合は、これらのプロパティをデフォルトの**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) と**PR_ の値CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) プロパティでは、それぞれ。 
  

