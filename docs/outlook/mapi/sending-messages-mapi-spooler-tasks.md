---
title: ���b�Z�[�W�̑��M MAPI �X�v�[���[ �^�X�N
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 81c65f21-03ba-43eb-a6d4-d311e660ac5c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8a6730cca5c75a888afb5ff0a44f1e2a0a6465e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339677"
---
# <a name="sending-messages-mapi-spooler-tasks"></a>メッセージの送信: MAPI スプーラーのタスク

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI �X�v�[���[�Ɋւ��郁�b�Z�[�W�̓]���v���Z�X�Ɋ܂܂�郁�b�Z�[�W �X�g�A���Ȃ��Ɩ��ڂɊ֘A�g�����X�|�[�g �v���o�C�_�[�𖧌����X�g�A����уg�����X�|�[�g�ɂ́A��M�҂�����ł��Ȃ��Ƃ��A����у��b�Z�[�W�̏������K�v�ł��B
  
 **��A�K�v�ȏ����́AMAPI �X�v�[���[�́A���̎菇����s���܂��B**
  
1. If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method. 
    
2. トランスポートプロバイダは、 **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティが FALSE に設定されているすべての受信者にメッセージを送信します。 
    
3. **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) プロパティが設定されている場合に、処理中にメッセージに追加された追加情報をクリーンアップするための適切な関数 ([removepreprocessinfo](removepreprocessinfo.md)) を呼び出します。 This function is specified when the transport provider registers its preprocessor function. 
    
4. [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)���\�b�h��Ăяo���܂��B **FinishedMsg**���b�Z�[�W�́A�v���o�C�_�[��i�[���܂��B
    
  - ���b�Z�[�W�̃��b�N�������܂��B
    
  - Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists. 次に、 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティでエントリ識別子によって識別されるフォルダーにメッセージをコピーします。これは、メッセージングフックプロバイダーの送信メッセージ処理によって置き換えられていない場合です。 最後に、 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティが TRUE に設定されている場合は、メッセージを削除します。 
    

