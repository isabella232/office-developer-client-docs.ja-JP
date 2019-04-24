---
title: imapisupportdo送信メール
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
ms.openlocfilehash: 8289b8dd2e0ab3c760e77a37b821d2fe74e4abe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315970"
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
    
 _lpmessage_
  
> [����]�|�C���^�[��J���Ă��郁�b�Z�[�W�𑗐M�ς݃A�C�e����ۗ��Ɏw�肳��Ă���t�H���_�[�Ƀ��b�Z�[�W�𐶐�����K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>解説

**imapisupport::D o送信メール**メソッドは、メッセージストアプロバイダーサポートオブジェクトに実装されています。 メッセージストアプロバイダーは、メッセージの処理が完了したときに MAPI スプーラーによって呼び出される[IMsgStore:: FinishedMsg](imsgstore-finishedmsg.md)メソッドの実装から、**メール**を呼び出します。 **FinishedMsg**は、メッセージのロックを解除し、メッセージの参照カウントが1であることを確認し、 **dosentmail**を呼び出します。
  
 **DoSentMail**�ł́A���̃^�X�N����s���܂��B 
  
- **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティのメッセージをチェックして、送信後にメッセージを削除する必要があるかどうかを判断します。
    
- ���M�ς݃A�C�e�� �t�H���_�[�̏ꏊ����肵�܂��B
    
- ���b�Z�[�W�̂������M�ς݃A�C�e��] �ɐݒ肷��A�t�b�N�̏�����J�n���܂��B
    
- Moves the message to the Sent Items folder, Deleted Items folder, or to another folder.
    
- ���b�Z�[�W�������܂��B
    
## <a name="see-also"></a>関連項目



[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[PidTagDeleteAfterSubmit ���K���̃v���p�e�B](pidtagdeleteaftersubmit-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

