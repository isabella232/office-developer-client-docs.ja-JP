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
# <a name="sending-messages-mapi-spooler-tasks"></a><span data-ttu-id="0c51c-103">メッセージの送信: MAPI スプーラーのタスク</span><span class="sxs-lookup"><span data-stu-id="0c51c-103">Sending Messages: MAPI Spooler Tasks</span></span>

  
  
<span data-ttu-id="0c51c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c51c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c51c-105">MAPI �X�v�[���[�Ɋւ��郁�b�Z�[�W�̓]���v���Z�X�Ɋ܂܂�郁�b�Z�[�W �X�g�A���Ȃ��Ɩ��ڂɊ֘A�g�����X�|�[�g �v���o�C�_�[�𖧌����X�g�A����уg�����X�|�[�g�ɂ́A��M�҂�����ł��Ȃ��Ƃ��A����у��b�Z�[�W�̏������K�v�ł��B</span><span class="sxs-lookup"><span data-stu-id="0c51c-105">The MAPI spooler is involved in the message transmission process when the message store is not tightly coupled with a transport provider, when the tightly coupled store and transport cannot handle a recipient, and when the message requires preprocessing.</span></span>
  
 <span data-ttu-id="0c51c-106">**��A�K�v�ȏ����́AMAPI �X�v�[���[�́A���̎菇����s���܂��B**</span><span class="sxs-lookup"><span data-stu-id="0c51c-106">**After any necessary preprocessing, the MAPI spooler performs the following steps:**</span></span>
  
1. <span data-ttu-id="0c51c-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span><span class="sxs-lookup"><span data-stu-id="0c51c-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span></span> 
    
2. <span data-ttu-id="0c51c-108">トランスポートプロバイダは、 **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティが FALSE に設定されているすべての受信者にメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="0c51c-108">Has the transport provider send the message to all recipients that have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to FALSE.</span></span> 
    
3. <span data-ttu-id="0c51c-109">**PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) プロパティが設定されている場合に、処理中にメッセージに追加された追加情報をクリーンアップするための適切な関数 ([removepreprocessinfo](removepreprocessinfo.md)) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0c51c-109">Calls the appropriate function ([RemovePreprocessInfo](removepreprocessinfo.md)) for cleaning up any additional information that was added to the message for use during preprocessing if the **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) property has been set.</span></span> <span data-ttu-id="0c51c-110">This function is specified when the transport provider registers its preprocessor function.</span><span class="sxs-lookup"><span data-stu-id="0c51c-110">This function is specified when the transport provider registers its preprocessor function.</span></span> 
    
4. <span data-ttu-id="0c51c-p102">[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)���\�b�h��Ăяo���܂��B **FinishedMsg**���b�Z�[�W�́A�v���o�C�_�[��i�[���܂��B</span><span class="sxs-lookup"><span data-stu-id="0c51c-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span></span>
    
  - <span data-ttu-id="0c51c-113">���b�Z�[�W�̃��b�N�������܂��B</span><span class="sxs-lookup"><span data-stu-id="0c51c-113">Unlocks the message.</span></span>
    
  - <span data-ttu-id="0c51c-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span><span class="sxs-lookup"><span data-stu-id="0c51c-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span></span> <span data-ttu-id="0c51c-115">次に、 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティでエントリ識別子によって識別されるフォルダーにメッセージをコピーします。これは、メッセージングフックプロバイダーの送信メッセージ処理によって置き換えられていない場合です。</span><span class="sxs-lookup"><span data-stu-id="0c51c-115">It then copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property, if not superseded by a messaging hook provider's sent message processing.</span></span> <span data-ttu-id="0c51c-116">最後に、 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティが TRUE に設定されている場合は、メッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="0c51c-116">Finally, it deletes the message if the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property has been set to TRUE.</span></span> 
    

