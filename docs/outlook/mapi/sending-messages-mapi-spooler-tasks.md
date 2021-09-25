---
title: ���b�Z�[�W�̑��M MAPI �X�v�[���[ �^�X�N
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 81c65f21-03ba-43eb-a6d4-d311e660ac5c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1380d7528f0902ec34ec0af9b7a31a4602d1b071
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578649"
---
# <a name="sending-messages-mapi-spooler-tasks"></a>メッセージの送信: MAPI スプーラー タスク

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI �X�v�[���[�Ɋւ��郁�b�Z�[�W�̓]���v���Z�X�Ɋ܂܂�郁�b�Z�[�W �X�g�A���Ȃ��Ɩ��ڂɊ֘A�g�����X�|�[�g �v���o�C�_�[�𖧌����X�g�A����уg�����X�|�[�g�ɂ́A��M�҂�����ł��Ȃ��Ƃ��A����у��b�Z�[�W�̏������K�v�ł��B
  
 **��A�K�v�ȏ����́AMAPI �X�v�[���[�́A���̎菇����s���܂��B**
  
1. If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method. 
    
2. トランスポート プロバイダーは、メッセージを FALSE に設定PR_RESPONSIBILITY  [(PidTagResponsibility)](pidtagresponsibility-canonical-property.md)プロパティを持つすべての受信者に送信します。 
    
3. **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) プロパティが設定されている場合、前処理中に使用するためにメッセージに追加された追加情報をクリーンアップするために、適切な関数 [(RemovePreprocessInfo)](removepreprocessinfo.md)を呼び出します。 This function is specified when the transport provider registers its preprocessor function. 
    
4. [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)���\�b�h��Ăяo���܂��B **FinishedMsg**���b�Z�[�W�́A�v���o�C�_�[��i�[���܂��B
    
  - ���b�Z�[�W�̃��b�N�������܂��B
    
  - Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists. 次に、メッセージング フック プロバイダーの送信メッセージ処理に取って代えされない場合は **、PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティのエントリ識別子によって識別されるフォルダーにメッセージをコピーします。 最後に、このメッセージは、PR_DELETE_AFTER_SUBMIT **(** [PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティが TRUE に設定されている場合にメッセージを削除します。 
    

