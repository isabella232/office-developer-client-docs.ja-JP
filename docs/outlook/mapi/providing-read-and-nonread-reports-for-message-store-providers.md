---
title: メッセージストアプロバイダーに対して読み取りおよび非開封レポートを提供する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328512"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="57809-103">メッセージストアプロバイダーに対して読み取りおよび非開封レポートを提供する</span><span class="sxs-lookup"><span data-stu-id="57809-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="57809-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57809-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57809-105">メッセージストアプロバイダーがメッセージを受信できる場合は、メッセージストアプロバイダーによって受信されたメッセージの読み取りレポートおよび非開封レポートをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="57809-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="57809-106">受信したメッセージに**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが含まれており、そのプロパティの値が TRUE である場合、メッセージストアは、ユーザーがメッセージを開いたときに送信者に通知メッセージを送信する必要があります。メッセージが開封されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="57809-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="57809-107">同様に、ユーザーがメッセージを開く前に削除した場合は、メッセージが開封されていないことを示す返信を、メッセージストアが送信者に発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57809-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="57809-108">これらのレポートを発行するには、 [IMessage: imapiprop](imessageimapiprop.md)オブジェクトを作成し、メッセージに関連するプロパティを入力して、そのメッセージがユーザーによって生成された場合と同様に MAPI スプーラーに送信します。</span><span class="sxs-lookup"><span data-stu-id="57809-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="57809-109">[imapisupport:: readreceipt](imapisupport-readreceipt.md)メソッドは、このために使用できます。</span><span class="sxs-lookup"><span data-stu-id="57809-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="57809-110">保留中の読み取りレポートまたは非開封レポートを含む未開封メッセージのコピーをメッセージストアが作成する場合は、特別な注意を払う必要があります。</span><span class="sxs-lookup"><span data-stu-id="57809-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="57809-111">このようなレポートは、ユーザーがレポートが要求されたメッセージのコピーを読み取るときには生成しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="57809-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="57809-112">このようなメッセージのコピーを作成する場合、メッセージストアプロバイダーには、 [imapifolder:: setreadflags](imapifolder-setreadflags.md)および[IMessage:: setreadflags](imessage-setreadflag.md)への呼び出しに CLEAR_RN_PENDING および CLEAR_NRN_PENDING フラグを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="57809-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="57809-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="57809-113">See also</span></span>



<span data-ttu-id="57809-114">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="57809-114">[Message Store Features](message-store-features.md)</span></span>

