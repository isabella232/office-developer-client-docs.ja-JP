---
title: メッセージ ストア プロバイダーに対する読み取りレポートと読み取り以外のレポートの提供
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432339"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="ae767-103">メッセージ ストア プロバイダーに対する読み取りレポートと読み取り以外のレポートの提供</span><span class="sxs-lookup"><span data-stu-id="ae767-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="ae767-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae767-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae767-105">メッセージ ストア プロバイダーがメッセージを受信できる場合は、メッセージ ストア プロバイダーが受信したメッセージの読み取りレポートと未読レポートをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae767-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="ae767-106">受信メッセージに **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)プロパティが含まれている場合、そのプロパティの値が TRUE の場合、メッセージ ストアは、ユーザーがメッセージを開くと送信者に通知メッセージを送信し、メッセージが読み取られたことを示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae767-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="ae767-107">同様に、ユーザーがメッセージを開く前に削除した場合、メッセージ ストアは、メッセージが読み取りなかったことを示す返信を送信者に発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae767-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="ae767-108">これらのレポートの発行は [、IMessage : IMAPIProp](imessageimapiprop.md) オブジェクトを作成し、メッセージに関連するプロパティを入力し、メッセージがユーザーに送信された場合と同様に MAPI スプーラーに送信する問題です。</span><span class="sxs-lookup"><span data-stu-id="ae767-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="ae767-109">この [場合、IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ae767-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ae767-110">メッセージ ストアが未読メッセージのコピーを、保留中の読み取りレポートまたは未読レポートと一緒に作成する場合は、特別な注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="ae767-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="ae767-111">このようなレポートは、ユーザーが要求されたメッセージのコピーを読み取った場合に生成される必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae767-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="ae767-112">このようなメッセージのコピーを作成する場合、メッセージ ストア プロバイダーは [、IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) および [IMessage::SetReadFlag](imessage-setreadflag.md)への呼び出しに CLEAR_RN_PENDING フラグと CLEAR_NRN_PENDING フラグを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae767-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ae767-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae767-113">See also</span></span>



<span data-ttu-id="ae767-114">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="ae767-114">[Message Store Features](message-store-features.md)</span></span>

