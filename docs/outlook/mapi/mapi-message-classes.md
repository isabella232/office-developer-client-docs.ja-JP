---
title: MAPI メッセージ クラス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 64ef2bbb-585c-4908-8ad4-a1c954057e9b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 27b81c0939aa3e880f3998d33f4717c51bdbe681
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801401"
---
# <a name="mapi-message-classes"></a><span data-ttu-id="73af7-103">MAPI メッセージ クラス</span><span class="sxs-lookup"><span data-stu-id="73af7-103">MAPI Message Classes</span></span>

  
  
<span data-ttu-id="73af7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73af7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73af7-105">すべてのメッセージには、 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) の種類、目的、またはメッセージの内容を識別する、メッセージ クラス プロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="73af7-105">Every message has a message class property, **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), which identifies the type, purpose, or content of the message.</span></span> <span data-ttu-id="73af7-106">**PR_MESSAGE_CLASS**は、すべての新規メッセージに必要なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="73af7-106">**PR_MESSAGE_CLASS** is a required property on all new messages.</span></span> <span data-ttu-id="73af7-107">メッセージのクラスでは、受信メッセージを配置するフォルダーをユーザーにメッセージを表示するために使用されるフォームを決定します。</span><span class="sxs-lookup"><span data-stu-id="73af7-107">A message's class determines the form that is used to present the message to the user and the folder for placing incoming messages.</span></span> 
  
<span data-ttu-id="73af7-108">メッセージ クラスには、32 127 からの ASCII 文字が含まれていると、ピリオドで区切られた文字列を文字の大文字小文字を区別しますが、ピリオドで終了できません。</span><span class="sxs-lookup"><span data-stu-id="73af7-108">Message classes are case-sensitive character strings that contain ASCII characters 32 through 127 and are delimited by periods, but they cannot end with a period.</span></span> <span data-ttu-id="73af7-109">各文字列はサブクラスのレベルを表し、許可されるレベルの数に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="73af7-109">Each string represents a level of subclassing, and there is no limit to the number of levels allowed.</span></span> 
  
<span data-ttu-id="73af7-110">たとえば、クライアント アプリケーションが送信して、 **IPM**メッセージに分類が表示されるほとんどのメッセージ クラス、個人間のすべてのメッセージを記述するさまざまなカテゴリ (つまり、人間のユーザーではなく、プログラムで読み取る必要のあるメッセージ、コンピューター)。</span><span class="sxs-lookup"><span data-stu-id="73af7-110">For example, most messages that client applications send and receive fall into the **IPM** message class, a broad category that describes all interpersonal messages (that is, messages that are meant to be read by a human user, rather than programmatically by a computer).</span></span> <span data-ttu-id="73af7-111">メッセージ ストア プロバイダーより正確に、 **IPM**のサブクラスを作成することによって、IPM メッセージを説明します。</span><span class="sxs-lookup"><span data-stu-id="73af7-111">Message store providers more precisely describe an IPM message by creating an **IPM** subclass.</span></span> <span data-ttu-id="73af7-112">**IPM**のサブクラスでは、 **IPM**メッセージ クラスのプロパティを継承します。</span><span class="sxs-lookup"><span data-stu-id="73af7-112">The **IPM** subclass inherits the properties of the **IPM** message class.</span></span> <span data-ttu-id="73af7-113">**IPM など、IPM 識別子の上に他の文字の文字列を連結することにより、 **IPM**クラスのサブクラスと呼びます。注** **IPM、注意のメッセージを記述します。お問い合わせください**連絡先のメッセージを記述します。</span><span class="sxs-lookup"><span data-stu-id="73af7-113">Subclasses of the **IPM** class are named by concatenating other character strings onto the IPM identifier, such as **IPM.Note** to describe a note message and **IPM.Contact** to describe a contact message.</span></span> 
  
<span data-ttu-id="73af7-114">IPM メッセージの管理と表示を処理するには、クライアントは、MAPI が提供する標準的なフォームを使用できます。</span><span class="sxs-lookup"><span data-stu-id="73af7-114">To handle the display and management of IPM messages, clients can use a standard form that MAPI provides.</span></span> <span data-ttu-id="73af7-115">を表示しを新しいメッセージ クラスの管理を処理するには、クライアント アプリケーションの開発者は、ある 2 つのオプション。</span><span class="sxs-lookup"><span data-stu-id="73af7-115">To handle the display and management of new message classes, you as a client application developer have two options:</span></span>
  
1. <span data-ttu-id="73af7-116">新しいフォームを作成するには、標準的なクライアントを使用して MAPI 定義フォームのインターフェイスのセットを使用します。</span><span class="sxs-lookup"><span data-stu-id="73af7-116">You can create a new form by using the set of MAPI-defined form interfaces that a standard client can use.</span></span>
    
2. <span data-ttu-id="73af7-117">独自のクライアントを作成するには、完全な実装することによってスタンドアロンのアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="73af7-117">You can write your own client by implementing a complete, standalone application.</span></span> 
    
<span data-ttu-id="73af7-118">クライアントは、 **IPM**または**IPC**のいずれかのサブクラスにすべての発信メッセージの**PR_MESSAGE_CLASS**プロパティを設定する必要があります、メッセージ ストア プロバイダーは最終的な責任を設定することです。</span><span class="sxs-lookup"><span data-stu-id="73af7-118">Although clients should set the **PR_MESSAGE_CLASS** property for every outgoing message to a subclass of either **IPM** or **IPC**, the message store provider has the ultimate responsibility for setting it.</span></span> <span data-ttu-id="73af7-119">したがって、クライアントは、そのメッセージ クラスを設定せず、メッセージを送信する場合、メッセージ ストア プロバイダーに設定クライアントの適切な種類の適切な既定値です。</span><span class="sxs-lookup"><span data-stu-id="73af7-119">Therefore, if a client sends a message without setting its message class, the message store provider sets it to the appropriate default value for the appropriate type of client.</span></span> <span data-ttu-id="73af7-120">個人間のメッセージング クライアントのデフォルトのメッセージ クラス**IPM**です。プロセス間通信のクライアントのデフォルトのメッセージ クラスは、 **IPC**です。</span><span class="sxs-lookup"><span data-stu-id="73af7-120">The default message class for interpersonal messaging clients is **IPM**; the default message class for interprocess communication clients is **IPC**.</span></span> 
  
<span data-ttu-id="73af7-121">メッセージ クラスには、255 文字の長さの制限があります。</span><span class="sxs-lookup"><span data-stu-id="73af7-121">Message classes have a length restriction of 255 characters.</span></span> <span data-ttu-id="73af7-122">ただし、メッセージ クラスを超えない 127 文字までのレポートで使用するメッセージ クラスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="73af7-122">However, message classes should not exceed 127 characters to support the message classes used in reports.</span></span> <span data-ttu-id="73af7-123">2 つの追加と、元のメッセージのクラスに基づくレポートのメッセージ クラス: プレフィックスとサフィックス。</span><span class="sxs-lookup"><span data-stu-id="73af7-123">Report message classes are based on the class of the original message, with two additions: a prefix and a suffix.</span></span> <span data-ttu-id="73af7-124">プレフィックス レポートことを示し、メッセージは、レポート、サフィックスは、レポートの種類を示します: 災害復旧 (配信レポートの場合)、NDR (配信不能レポート)、(レポートを参照)、IPNRN または IPNNRN (nonread のレポート)。</span><span class="sxs-lookup"><span data-stu-id="73af7-124">The prefix REPORT indicates that the message is a report, and the suffix indicates the type of report: DR (delivery report), NDR (nondelivery report), IPNRN (read report), or IPNNRN (nonread report).</span></span> <span data-ttu-id="73af7-125">文字で、これらの長さの制限が指定されているに注意してください。2 バイト文字セットを使用するプラットフォームでは、実際のバイト数が高い場合があります。</span><span class="sxs-lookup"><span data-stu-id="73af7-125">Note that these length restrictions are given in characters; on platforms that use a double-byte character set, the actual byte count might be higher.</span></span> 
  
<span data-ttu-id="73af7-126">メッセージ ストア プロバイダーは、クライアントがそのメッセージ クラスの使用可能な制限を超える文字列を代入しようとすると、 [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドの実装から MAPI_E_INVALID_PARAMETER を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="73af7-126">Message store providers should return MAPI_E_INVALID_PARAMETER from their [IMAPIProp::SetProps](imapiprop-setprops.md) method implementations when a client attempts to assign a string that exceeds the allowable limit for their message class.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="73af7-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="73af7-127">See also</span></span>



[<span data-ttu-id="73af7-128">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="73af7-128">MAPI Messages</span></span>](mapi-messages.md)

