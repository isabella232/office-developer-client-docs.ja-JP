---
title: IMAPISupportDoSentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2bded946a1fc7d7ab181d3953defa24e247c003c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800756"
---
# <a name="imapisupportdosentmail"></a>IMAPISupport::DoSentMail

  
  
**適用されます**: Outlook 
  
���M���ꂽ���b�Z�[�W��������܂��B
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpMessage_
  
> [����]�|�C���^�[��J���Ă��郁�b�Z�[�W�𑗐M�ς݃A�C�e����ۗ��Ɏw�肳��Ă���t�H���_�[�Ƀ��b�Z�[�W�𐶐�����K�v������܂��B
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

���b�Z�[�W �X�g�A �v���o�C�**�[ �T�|�[�g �I�u�W�F�N�g�� **IMAPISupport::DoSentMail**���\�b�h��������܂��B���b�Z�[�W�̃X�g�A �v���o�C�**�[�́A���b�Z�[�W�̏���������������AMAPI �X�v�[���[�ŌĂяo�����[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)���\�b�h�̎������� [DoSentMail](imsgstore-finishedmsg.md)��Ăяo���܂��B **FinishedMsg**�́A���b�Z�[�W�̃��b�N�����A�ɂ��A���b�Z�[�W�̎Q�ƃJ�E���g�� 1�A **DoSentMail**��Ăяo���܂��B
  
 **DoSentMail**�ł́A���̃^�X�N����s���܂��B 
  
- メッセージを送信した後、メッセージを削除する必要があるかどうかを判断するのには**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) のプロパティをチェックします。
    
- ���M�ς݃A�C�e�� �t�H���_�[�̏ꏊ����肵�܂��B
    
- ���b�Z�[�W�̂������M�ς݃A�C�e��] �ɐݒ肷��A�t�b�N�̏�����J�n���܂��B
    
- 送信済みアイテム フォルダー、削除済みアイテム フォルダー、または別のフォルダーにメッセージを移動します。
    
- ���b�Z�[�W�������܂��B
    
## <a name="see-also"></a>�֘A����



[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[PidTagDeleteAfterSubmit ���K���̃v���p�e�B](pidtagdeleteaftersubmit-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

