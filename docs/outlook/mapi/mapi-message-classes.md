---
title: MAPI メッセージクラス
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
# <a name="mapi-message-classes"></a><span data-ttu-id="1d01a-103">MAPI メッセージクラス</span><span class="sxs-lookup"><span data-stu-id="1d01a-103">MAPI Message Classes</span></span>

  
  
<span data-ttu-id="1d01a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d01a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d01a-105">すべてのメッセージには、メッセージクラスプロパティ**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) があり、メッセージの種類、目的、または内容を識別します。</span><span class="sxs-lookup"><span data-stu-id="1d01a-105">Every message has a message class property, **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), which identifies the type, purpose, or content of the message.</span></span> <span data-ttu-id="1d01a-106">**PR_MESSAGE_CLASS**は、すべての新しいメッセージの必須プロパティです。</span><span class="sxs-lookup"><span data-stu-id="1d01a-106">**PR_MESSAGE_CLASS** is a required property on all new messages.</span></span> <span data-ttu-id="1d01a-107">メッセージのクラスは、ユーザーにメッセージを表示するために使用するフォームと、受信メッセージを配置するフォルダーを決定します。</span><span class="sxs-lookup"><span data-stu-id="1d01a-107">A message's class determines the form that is used to present the message to the user and the folder for placing incoming messages.</span></span> 
  
<span data-ttu-id="1d01a-108">メッセージクラスは大文字と小文字が区別され、ASCII 文字 32 ~ 127 を含み、ピリオドで区切られていますが、末尾にピリオドを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="1d01a-108">Message classes are case-sensitive character strings that contain ASCII characters 32 through 127 and are delimited by periods, but they cannot end with a period.</span></span> <span data-ttu-id="1d01a-109">各文字列はサブクラス化のレベルを表し、許可されるレベル数に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="1d01a-109">Each string represents a level of subclassing, and there is no limit to the number of levels allowed.</span></span> 
  
<span data-ttu-id="1d01a-110">たとえば、クライアントアプリケーションが送受信するメッセージのほとんどは、 **IPM**メッセージクラスに分類されます。これは、すべての個人外のメッセージ (つまり、人間が判読することを意図したメッセージを、プログラムによってプログラムするのではなく、人間のユーザーが読み取ることを意図したメッセージ) を説明する幅広いカテゴリです。コンピューター)。</span><span class="sxs-lookup"><span data-stu-id="1d01a-110">For example, most messages that client applications send and receive fall into the **IPM** message class, a broad category that describes all interpersonal messages (that is, messages that are meant to be read by a human user, rather than programmatically by a computer).</span></span> <span data-ttu-id="1d01a-111">メッセージストアプロバイダー **ipm**サブクラスを作成することにより、ipm メッセージをより正確に記述します。</span><span class="sxs-lookup"><span data-stu-id="1d01a-111">Message store providers more precisely describe an IPM message by creating an **IPM** subclass.</span></span> <span data-ttu-id="1d01a-112">**ipm**サブクラスは、 **ipm**メッセージクラスのプロパティを継承します。</span><span class="sxs-lookup"><span data-stu-id="1d01a-112">The **IPM** subclass inherits the properties of the **IPM** message class.</span></span> <span data-ttu-id="1d01a-113">ipm クラスの\*\*\*\* サブクラスには、他の文字文字列を ipm 識別子 (ipm など) に連結することによって名前が付けられ**ます。** メモメッセージと IPM について説明し**ます。** 連絡先メッセージを説明する連絡先。</span><span class="sxs-lookup"><span data-stu-id="1d01a-113">Subclasses of the **IPM** class are named by concatenating other character strings onto the IPM identifier, such as **IPM.Note** to describe a note message and **IPM.Contact** to describe a contact message.</span></span> 
  
<span data-ttu-id="1d01a-114">IPM メッセージの表示と管理を処理するために、クライアントは MAPI が提供する標準のフォームを使用できます。</span><span class="sxs-lookup"><span data-stu-id="1d01a-114">To handle the display and management of IPM messages, clients can use a standard form that MAPI provides.</span></span> <span data-ttu-id="1d01a-115">新しいメッセージクラスの表示と管理を処理するために、クライアントアプリケーション開発者は次の2つのオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="1d01a-115">To handle the display and management of new message classes, you as a client application developer have two options:</span></span>
  
1. <span data-ttu-id="1d01a-116">標準クライアントで使用できる MAPI 定義フォームインターフェイスのセットを使用して、新しいフォームを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1d01a-116">You can create a new form by using the set of MAPI-defined form interfaces that a standard client can use.</span></span>
    
2. <span data-ttu-id="1d01a-117">完全なスタンドアロンアプリケーションを実装することにより、独自のクライアントを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1d01a-117">You can write your own client by implementing a complete, standalone application.</span></span> 
    
<span data-ttu-id="1d01a-118">クライアントは、すべての送信メッセージの**PR_MESSAGE_CLASS**プロパティを、 **IPM**または**IPC**のサブクラスに設定する必要がありますが、メッセージストアプロバイダーには、それを設定するための最終的な責任があります。</span><span class="sxs-lookup"><span data-stu-id="1d01a-118">Although clients should set the **PR_MESSAGE_CLASS** property for every outgoing message to a subclass of either **IPM** or **IPC**, the message store provider has the ultimate responsibility for setting it.</span></span> <span data-ttu-id="1d01a-119">そのため、クライアントがメッセージクラスを設定せずにメッセージを送信した場合、メッセージストアプロバイダーは、適切な種類のクライアントに対して適切な既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="1d01a-119">Therefore, if a client sends a message without setting its message class, the message store provider sets it to the appropriate default value for the appropriate type of client.</span></span> <span data-ttu-id="1d01a-120">個人間メッセージングクライアントの既定のメッセージクラスは**IPM**です。プロセス間通信クライアントの既定のメッセージクラスは**IPC**です。</span><span class="sxs-lookup"><span data-stu-id="1d01a-120">The default message class for interpersonal messaging clients is **IPM**; the default message class for interprocess communication clients is **IPC**.</span></span> 
  
<span data-ttu-id="1d01a-121">メッセージクラスには、255文字の長さ制限があります。</span><span class="sxs-lookup"><span data-stu-id="1d01a-121">Message classes have a length restriction of 255 characters.</span></span> <span data-ttu-id="1d01a-122">ただし、メッセージクラスは、レポートで使用されるメッセージクラスをサポートするために127文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="1d01a-122">However, message classes should not exceed 127 characters to support the message classes used in reports.</span></span> <span data-ttu-id="1d01a-123">レポートメッセージクラスは、元のメッセージのクラスに基づいています。これには、プレフィックスとサフィックスという2つの追加があります。</span><span class="sxs-lookup"><span data-stu-id="1d01a-123">Report message classes are based on the class of the original message, with two additions: a prefix and a suffix.</span></span> <span data-ttu-id="1d01a-124">プレフィックスレポートは、メッセージがレポートであることを示し、サフィックスはレポートの種類 (配信レポート)、NDR (配信レポート)、IPNRN (読み取りレポート)、または ipnnrn (非開封レポート) を示します。</span><span class="sxs-lookup"><span data-stu-id="1d01a-124">The prefix REPORT indicates that the message is a report, and the suffix indicates the type of report: DR (delivery report), NDR (nondelivery report), IPNRN (read report), or IPNNRN (nonread report).</span></span> <span data-ttu-id="1d01a-125">これらの長さ制限は文字で指定されることに注意してください。2バイト文字セットを使用するプラットフォームでは、実際のバイト数が大きくなることがあります。</span><span class="sxs-lookup"><span data-stu-id="1d01a-125">Note that these length restrictions are given in characters; on platforms that use a double-byte character set, the actual byte count might be higher.</span></span> 
  
<span data-ttu-id="1d01a-126">メッセージストアプロバイダーは、クライアントが自分のメッセージクラスに対して許容される制限を超える文字列を割り当てようとしたときに、 [imapiprop:: setprops](imapiprop-setprops.md)メソッド実装から MAPI_E_INVALID_PARAMETER を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d01a-126">Message store providers should return MAPI_E_INVALID_PARAMETER from their [IMAPIProp::SetProps](imapiprop-setprops.md) method implementations when a client attempts to assign a string that exceeds the allowable limit for their message class.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1d01a-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1d01a-127">See also</span></span>



[<span data-ttu-id="1d01a-128">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="1d01a-128">MAPI Messages</span></span>](mapi-messages.md)

