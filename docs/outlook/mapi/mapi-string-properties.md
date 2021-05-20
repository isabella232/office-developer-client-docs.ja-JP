---
title: MAPI 文字列のプロパティ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9720b649eadecc73d84d98926674a1786796ba70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431394"
---
# <a name="mapi-string-properties"></a><span data-ttu-id="eea0a-103">MAPI 文字列のプロパティ</span><span class="sxs-lookup"><span data-stu-id="eea0a-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="eea0a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eea0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eea0a-105">MAPI には、文字列プロパティを記述する 3 つの異なるプロパティの種類があります。</span><span class="sxs-lookup"><span data-stu-id="eea0a-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="eea0a-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="eea0a-106">PT_TSTRING</span></span>
  
<span data-ttu-id="eea0a-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="eea0a-107">PT_STRING8</span></span>
  
<span data-ttu-id="eea0a-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eea0a-108">PT_UNICODE</span></span>
  
<span data-ttu-id="eea0a-109">文字列プロパティは、最も一般的に、文字列プロパティとしてPT_TSTRING。</span><span class="sxs-lookup"><span data-stu-id="eea0a-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="eea0a-110">プロパティPT_TSTRINGは、UNICODE マクロが定義されたかどうかに応じて、他の文字列プロパティの種類の 1 つを条件付きでコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="eea0a-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="eea0a-111">PT_STRING8 ANSI 形式の 8 ビットの null 終端文字文字列について説明します。PT_UNICODE、2 バイトの null 終端文字文字列について説明します。</span><span class="sxs-lookup"><span data-stu-id="eea0a-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="eea0a-112">クライアントまたはサービス プロバイダー、またはクライアントとプロバイダーの両方で Unicode 文字文字列をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="eea0a-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="eea0a-113">必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="eea0a-113">It is not required.</span></span> <span data-ttu-id="eea0a-114">文字列のみをサポートするクライアントPT_STRING8 Unicode をサポートするプロバイダーを操作でき、その逆も同様です。</span><span class="sxs-lookup"><span data-stu-id="eea0a-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="eea0a-115">この相互運用性を有効にするには、クライアントとサービス プロバイダーは MAPI_UNICODE フラグを渡して、文字列の交換を伴うメソッドで Unicode がサポートされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="eea0a-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="eea0a-116">たとえば、クライアントが Unicode をサポートし、フォルダーの表示名を取得する必要がある場合です。</span><span class="sxs-lookup"><span data-stu-id="eea0a-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="eea0a-117">クライアントのすべてのプロパティは、PT_TSTRINGを入力PT_UNICODE。</span><span class="sxs-lookup"><span data-stu-id="eea0a-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="eea0a-118">クライアントは、フォルダーの [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出して PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを取得すると **、MAPI_UNICODE** フラグを渡して、Unicode 形式で表示名文字列を返す要求を行います。</span><span class="sxs-lookup"><span data-stu-id="eea0a-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="eea0a-119">クライアントとサービス プロバイダーは、メソッド呼び出しで文字セットを指定する場合は要求のみである点に注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eea0a-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="eea0a-120">1 つまたは両方の文字セットをサポートする方法は、オブジェクトの実装者です。</span><span class="sxs-lookup"><span data-stu-id="eea0a-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="eea0a-121">ただし、サービス プロバイダーは、1 つのセットのみをサポートするプロバイダーよりも広範な配布を実現できるので、両方の文字セットをサポートしてください。</span><span class="sxs-lookup"><span data-stu-id="eea0a-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="eea0a-122">文字列プロパティは、バイナリ プロパティ (プロパティの種類を使用するプロパティ) と同じサイズPT_BINARY。</span><span class="sxs-lookup"><span data-stu-id="eea0a-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="eea0a-123">大きなプロパティの操作を容易にするために、MAPI では、サービス プロバイダーがこれらのプロパティを設定してサイズ制限を適用できます。</span><span class="sxs-lookup"><span data-stu-id="eea0a-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="eea0a-124">これらの制限は、次に応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="eea0a-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="eea0a-125">プロパティが読み取りまたは書き込み中かどうか。</span><span class="sxs-lookup"><span data-stu-id="eea0a-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="eea0a-126">サービス プロバイダーが **IMAPIProp メソッドを実装する** 方法。</span><span class="sxs-lookup"><span data-stu-id="eea0a-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="eea0a-127">メモリの制約など、ランタイムに関する考慮事項。</span><span class="sxs-lookup"><span data-stu-id="eea0a-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="eea0a-128">文字セットの変換に関する問題。</span><span class="sxs-lookup"><span data-stu-id="eea0a-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="eea0a-129">サイズ制限は、大きなプロパティのすべての値を表示できない場合があるため、テーブルの列セットで使用する場合にも、文字列プロパティとバイナリ プロパティに配置できます。</span><span class="sxs-lookup"><span data-stu-id="eea0a-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="eea0a-130">多くのサービス プロバイダーは、テーブルで使用される大きな文字列プロパティまたはバイナリ プロパティを 255 バイトに切り詰めます。</span><span class="sxs-lookup"><span data-stu-id="eea0a-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="eea0a-131">クライアントがオブジェクトの **GetProps** または **SetProps** メソッドを呼び出して、大きな文字列またはバイナリ プロパティを処理し、プロパティ サイズが原因で呼び出しが失敗すると、メソッドはエラー値 MAPI_E_NOT_ENOUGH_MEMORY を返します。</span><span class="sxs-lookup"><span data-stu-id="eea0a-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="eea0a-132">特定のプロパティに対して失敗している **GetProps** の場合、クライアントは [IMAPIProp::OpenProperty](imapiprop-openproperty.md) を呼び出し、IID_IStream をインターフェイス識別子として指定して **IStream** にアクセスを要求することで回復できます。</span><span class="sxs-lookup"><span data-stu-id="eea0a-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="eea0a-133">**OpenProperty を使用すると**、クライアントは、大きなプロパティの操作に適した **IStream** などのインターフェイスを使用して大きなプロパティを取得できます。</span><span class="sxs-lookup"><span data-stu-id="eea0a-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eea0a-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="eea0a-134">See also</span></span>



[<span data-ttu-id="eea0a-135">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="eea0a-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

