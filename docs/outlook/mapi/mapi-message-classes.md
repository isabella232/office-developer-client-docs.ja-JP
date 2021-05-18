---
title: MAPI メッセージ クラス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 64ef2bbb-585c-4908-8ad4-a1c954057e9b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b2ab5d56c53216152a83ca207ff5ba1d53c9049d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412087"
---
# <a name="mapi-message-classes"></a><span data-ttu-id="c3b81-103">MAPI メッセージ クラス</span><span class="sxs-lookup"><span data-stu-id="c3b81-103">MAPI Message Classes</span></span>

  
  
<span data-ttu-id="c3b81-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3b81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3b81-105">すべてのメッセージには、メッセージの種類 **、目的、または** コンテンツを識別する、PR_MESSAGE_CLASS [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)というメッセージ クラス プロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="c3b81-105">Every message has a message class property, **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), which identifies the type, purpose, or content of the message.</span></span> <span data-ttu-id="c3b81-106">**PR_MESSAGE_CLASS** は、すべての新しいメッセージで必須のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="c3b81-106">**PR_MESSAGE_CLASS** is a required property on all new messages.</span></span> <span data-ttu-id="c3b81-107">メッセージのクラスは、ユーザーにメッセージを表示するために使用されるフォームと、受信メッセージを配置するフォルダーを決定します。</span><span class="sxs-lookup"><span data-stu-id="c3b81-107">A message's class determines the form that is used to present the message to the user and the folder for placing incoming messages.</span></span> 
  
<span data-ttu-id="c3b81-108">メッセージ クラスは、ASCII 文字 32 ~ 127 を含む大文字と小文字を区別する文字列で、ピリオドで区切りますが、ピリオドで終わることはできません。</span><span class="sxs-lookup"><span data-stu-id="c3b81-108">Message classes are case-sensitive character strings that contain ASCII characters 32 through 127 and are delimited by periods, but they cannot end with a period.</span></span> <span data-ttu-id="c3b81-109">各文字列はサブクラス化のレベルを表し、許可されるレベルの数に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="c3b81-109">Each string represents a level of subclassing, and there is no limit to the number of levels allowed.</span></span> 
  
<span data-ttu-id="c3b81-110">たとえば、クライアント アプリケーションが送受信するほとんどのメッセージは **、IPM** メッセージ クラスに分類されます。これは、すべての対人メッセージ (つまり、コンピューターによってプログラムによって読み取るのではなく、人間のユーザーが読み取るメッセージ) を表す広範なカテゴリです。</span><span class="sxs-lookup"><span data-stu-id="c3b81-110">For example, most messages that client applications send and receive fall into the **IPM** message class, a broad category that describes all interpersonal messages (that is, messages that are meant to be read by a human user, rather than programmatically by a computer).</span></span> <span data-ttu-id="c3b81-111">メッセージ ストア プロバイダーは、IPM サブクラスを作成して IPM メッセージを **より正確に記述** します。</span><span class="sxs-lookup"><span data-stu-id="c3b81-111">Message store providers more precisely describe an IPM message by creating an **IPM** subclass.</span></span> <span data-ttu-id="c3b81-112">**IPM サブクラスは\*\*\*\*、IPM** メッセージ クラスのプロパティを継承します。</span><span class="sxs-lookup"><span data-stu-id="c3b81-112">The **IPM** subclass inherits the properties of the **IPM** message class.</span></span> <span data-ttu-id="c3b81-113">IPM クラスの **サブクラスの名前は、IPM** などの IPM 識別子に他の文字列を連結することで **指定されます。メモ** メッセージと **IPM を説明するために注意してください。連絡先メッセージ** を説明する連絡先。</span><span class="sxs-lookup"><span data-stu-id="c3b81-113">Subclasses of the **IPM** class are named by concatenating other character strings onto the IPM identifier, such as **IPM.Note** to describe a note message and **IPM.Contact** to describe a contact message.</span></span> 
  
<span data-ttu-id="c3b81-114">IPM メッセージの表示と管理を処理するために、クライアントは MAPI が提供する標準フォームを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c3b81-114">To handle the display and management of IPM messages, clients can use a standard form that MAPI provides.</span></span> <span data-ttu-id="c3b81-115">新しいメッセージ クラスの表示と管理を処理するには、クライアント アプリケーション開発者として次の 2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="c3b81-115">To handle the display and management of new message classes, you as a client application developer have two options:</span></span>
  
1. <span data-ttu-id="c3b81-116">標準クライアントが使用できる MAPI 定義フォーム インターフェイスのセットを使用して、新しいフォームを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c3b81-116">You can create a new form by using the set of MAPI-defined form interfaces that a standard client can use.</span></span>
    
2. <span data-ttu-id="c3b81-117">完全なスタンドアロン アプリケーションを実装することで、独自のクライアントを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c3b81-117">You can write your own client by implementing a complete, standalone application.</span></span> 
    
<span data-ttu-id="c3b81-118">クライアントは、すべての **送信メッセージの PR_MESSAGE_CLASS** プロパティを **IPM** または **IPC** のいずれかのサブクラスに設定する必要があります。メッセージ ストア プロバイダーは、このプロパティを設定する最終的な責任を負います。</span><span class="sxs-lookup"><span data-stu-id="c3b81-118">Although clients should set the **PR_MESSAGE_CLASS** property for every outgoing message to a subclass of either **IPM** or **IPC**, the message store provider has the ultimate responsibility for setting it.</span></span> <span data-ttu-id="c3b81-119">したがって、クライアントがメッセージ クラスを設定せずにメッセージを送信する場合、メッセージ ストア プロバイダーはメッセージを適切な種類のクライアントに対して適切な既定値に設定します。</span><span class="sxs-lookup"><span data-stu-id="c3b81-119">Therefore, if a client sends a message without setting its message class, the message store provider sets it to the appropriate default value for the appropriate type of client.</span></span> <span data-ttu-id="c3b81-120">対人間メッセージング クライアントの既定のメッセージ クラスは **IPM です**。プロセス間通信クライアントの既定のメッセージ クラスは **IPC です**。</span><span class="sxs-lookup"><span data-stu-id="c3b81-120">The default message class for interpersonal messaging clients is **IPM**; the default message class for interprocess communication clients is **IPC**.</span></span> 
  
<span data-ttu-id="c3b81-121">メッセージ クラスの長さは 255 文字です。</span><span class="sxs-lookup"><span data-stu-id="c3b81-121">Message classes have a length restriction of 255 characters.</span></span> <span data-ttu-id="c3b81-122">ただし、レポートで使用されるメッセージ クラスをサポートするために、メッセージ クラスは 127 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="c3b81-122">However, message classes should not exceed 127 characters to support the message classes used in reports.</span></span> <span data-ttu-id="c3b81-123">レポート メッセージ クラスは、元のメッセージのクラスに基づいており、プレフィックスと接尾辞の 2 つが追加されています。</span><span class="sxs-lookup"><span data-stu-id="c3b81-123">Report message classes are based on the class of the original message, with two additions: a prefix and a suffix.</span></span> <span data-ttu-id="c3b81-124">プレフィックス REPORT は、メッセージがレポートであり、サフィックスは、DR (配信レポート)、NDR (配信不能レポート)、IPNRN (読み取りレポート)、または IPNNRN (非読み取りレポート) の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="c3b81-124">The prefix REPORT indicates that the message is a report, and the suffix indicates the type of report: DR (delivery report), NDR (nondelivery report), IPNRN (read report), or IPNNRN (nonread report).</span></span> <span data-ttu-id="c3b81-125">これらの長さの制限は文字で指定されます。2 バイト文字セットを使用するプラットフォームでは、実際のバイト数が多くなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c3b81-125">Note that these length restrictions are given in characters; on platforms that use a double-byte character set, the actual byte count might be higher.</span></span> 
  
<span data-ttu-id="c3b81-126">クライアントがメッセージ クラスの許容制限を超える文字列を割り当てしようとすると、メッセージ ストア プロバイダーは [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドの実装から MAPI_E_INVALID_PARAMETER を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3b81-126">Message store providers should return MAPI_E_INVALID_PARAMETER from their [IMAPIProp::SetProps](imapiprop-setprops.md) method implementations when a client attempts to assign a string that exceeds the allowable limit for their message class.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c3b81-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="c3b81-127">See also</span></span>



[<span data-ttu-id="c3b81-128">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="c3b81-128">MAPI Messages</span></span>](mapi-messages.md)

