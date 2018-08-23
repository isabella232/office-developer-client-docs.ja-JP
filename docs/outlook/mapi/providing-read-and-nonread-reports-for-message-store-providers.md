---
title: メッセージ ストア プロバイダー用の開封済みレポートと未開封レポートの提供
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b082d063cc77be46fcd3d4e07ec6753f78f8f335
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803738"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="c6e78-103">メッセージ ストア プロバイダー用の開封済みレポートと未開封レポートの提供</span><span class="sxs-lookup"><span data-stu-id="c6e78-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="c6e78-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c6e78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c6e78-105">メッセージ ストア プロバイダーはメッセージを受信する場合に、読み取りとメッセージ ストア プロバイダーによって受信されたメッセージの nonread のレポートをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6e78-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="c6e78-106">メッセージ ・ ストアは、ユーザーが、メッセージを開いたとき、ソース ファイルを送信者に通知メッセージを送信**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) のプロパティが受信したメッセージに含まれている場合は、そのプロパティの値は TRUE をメッセージが読み取られたことを示します。</span><span class="sxs-lookup"><span data-stu-id="c6e78-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="c6e78-107">同様に、ユーザーは、開く前に、メッセージを削除した場合、メッセージ ・ ストアする必要がありますメッセージが読まれていることを示す送信者への応答を発行します。</span><span class="sxs-lookup"><span data-stu-id="c6e78-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="c6e78-108">作成するだけではこれらのレポートを発行、 [IMessage: IMAPIProp](imessageimapiprop.md)オブジェクト、メッセージ、関連するプロパティを入力し、メッセージは、ユーザーによって作成されたものがあるかのように、MAPI スプーラーに送信します。</span><span class="sxs-lookup"><span data-stu-id="c6e78-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="c6e78-109">この[IMAPISupport::ReadReceipt](imapisupport-readreceipt.md)メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c6e78-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c6e78-110">特別な注意する必要があるメッセージ ストアは、未読のメッセージを保留中の読み取りまたは nonread のレポートのコピーを作成するとき。</span><span class="sxs-lookup"><span data-stu-id="c6e78-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="c6e78-111">ユーザーはレポートが要求されたメッセージのコピーを読み取るときに、このようなレポートを生成できませんする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6e78-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="c6e78-112">とき、このようなメッセージのコピーを作成するには、メッセージ ストア プロバイダーは、 [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)と[IMessage::SetReadFlag](imessage-setreadflag.md)への呼び出しで、CLEAR_RN_PENDING と CLEAR_NRN_PENDING フラグを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6e78-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c6e78-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="c6e78-113">See also</span></span>



<span data-ttu-id="c6e78-114">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="c6e78-114">[Message Store Features](message-store-features.md)</span></span>

