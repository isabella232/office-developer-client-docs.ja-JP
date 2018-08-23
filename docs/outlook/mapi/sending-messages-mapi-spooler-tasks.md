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
ms.openlocfilehash: eef65990637d9c164ffe75f682e01ed134510e32
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570276"
---
# <a name="sending-messages-mapi-spooler-tasks"></a>���b�Z�[�W�̑��M: MAPI �X�v�[���[ �^�X�N

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI �X�v�[���[�Ɋւ��郁�b�Z�[�W�̓]���v���Z�X�Ɋ܂܂�郁�b�Z�[�W �X�g�A���Ȃ��Ɩ��ڂɊ֘A�g�����X�|�[�g �v���o�C�_�[�𖧌����X�g�A����уg�����X�|�[�g�ɂ́A��M�҂�����ł��Ȃ��Ƃ��A����у��b�Z�[�W�̏������K�v�ł��B
  
 **��A�K�v�ȏ����́AMAPI �X�v�[���[�́A���̎菇����s���܂��B**
  
1. メッセージがロックされていない場合は、 [IMsgStore::SetLockState](imsgstore-setlockstate.md)メソッドを使用して、メッセージをロックします。 
    
2. その**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティが FALSE に設定されているすべての受信者にメッセージを送信するトランスポート プロバイダーがあります。 
    
3. **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) プロパティが設定されている場合のプリプロセス中に使用するためのメッセージに追加された追加情報をクリーンアップするための適切な関数 ([RemovePreprocessInfo](removepreprocessinfo.md)) を呼び出します。 トランスポート プロバイダーは、プリプロセッサ関数を登録すると、この関数を指定します。 
    
4. [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)���\�b�h��Ăяo���܂��B **FinishedMsg**���b�Z�[�W�́A�v���o�C�_�[��i�[���܂��B
    
  - ���b�Z�[�W�̃��b�N�������܂��B
    
  - フックのアウト バウンド メッセージ フック プロバイダーが存在する場合の処理を実行する[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)メソッドを呼び出します。 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) のプロパティのエントリ id によって識別されたフォルダーにメッセージをコピーし、メッセージの処理をフック プロバイダーが送信場合は、メッセージによって置き換えられません。 最後に、 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティが TRUE に設定されている場合に、メッセージを削除します。 
    

