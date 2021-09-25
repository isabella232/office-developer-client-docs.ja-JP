---
title: IMAPISupportDoSentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 296c2df4b3dbee93a54585a932ee06591aecb3aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596072"
---
# <a name="imapisupportdosentmail"></a>IMAPISupport::DoSentMail

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
���M���ꂽ���b�Z�[�W��������܂��B
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpMessage_
  
> [����]�|�C���^�[��J���Ă��郁�b�Z�[�W�𑗐M�ς݃A�C�e����ۗ��Ɏw�肳��Ă���t�H���_�[�Ƀ��b�Z�[�W�𐶐�����K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

**IMAPISupport::D oSentMail** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。 メッセージ ストア プロバイダーは、メッセージの処理が完了すると MAPI スプーラーによって呼び出される [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)メソッドの実装から **DoSentMail** を呼び出します。 **FinishedMsg は** メッセージのロックを解除し、メッセージの参照カウントが 1 で **、DoSentMail を呼び出します**。
  
 **DoSentMail**�ł́A���̃^�X�N����s���܂��B 
  
- 送信後にメッセージを **PR_DELETE_AFTER_SUBMITする必要** があるかどうかを確認するメッセージ ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティをチェックします。
    
- ���M�ς݃A�C�e�� �t�H���_�[�̏ꏊ����肵�܂��B
    
- ���b�Z�[�W�̂������M�ς݃A�C�e��] �ɐݒ肷��A�t�b�N�̏�����J�n���܂��B
    
- Moves the message to the Sent Items folder, Deleted Items folder, or to another folder.
    
- ���b�Z�[�W�������܂��B
    
## <a name="see-also"></a>関連項目



[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[PidTagDeleteAfterSubmit ���K���̃v���p�e�B](pidtagdeleteaftersubmit-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

