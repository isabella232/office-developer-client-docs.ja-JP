---
title: MAPI 文字列のプロパティ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3cf118866bbc305678201a42a9a91998334f5cb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801467"
---
# <a name="mapi-string-properties"></a><span data-ttu-id="64d50-103">MAPI 文字列のプロパティ</span><span class="sxs-lookup"><span data-stu-id="64d50-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="64d50-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="64d50-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="64d50-105">MAPI には、文字列のプロパティを記述する 3 つのプロパティの種類が用意されています。</span><span class="sxs-lookup"><span data-stu-id="64d50-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="64d50-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="64d50-106">PT_TSTRING</span></span>
  
<span data-ttu-id="64d50-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="64d50-107">PT_STRING8</span></span>
  
<span data-ttu-id="64d50-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="64d50-108">PT_UNICODE</span></span>
  
<span data-ttu-id="64d50-109">文字列プロパティは、通常、PT_TSTRING として定義されます。</span><span class="sxs-lookup"><span data-stu-id="64d50-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="64d50-110">PT_TSTRING プロパティの型は他の文字列プロパティの型、UNICODE マクロが定義されているかどうかによって異なりますのいずれかに条件付きでコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="64d50-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="64d50-111">PT_STRING8 8 ビット文字の null で終わる文字列を ANSI 形式での説明します。PT_UNICODE では、2 バイト文字の null で終わる文字列について説明します。</span><span class="sxs-lookup"><span data-stu-id="64d50-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="64d50-112">Unicode 文字の文字列をサポートするか、クライアント、または、サービス プロバイダー、またはクライアントとプロバイダーの両方を選択できます。</span><span class="sxs-lookup"><span data-stu-id="64d50-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="64d50-113">必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="64d50-113">It is not required.</span></span> <span data-ttu-id="64d50-114">PT_STRING8 文字列のみをサポートしているクライアントは、Unicode およびその逆の場合をサポートするプロバイダーを操作できます。</span><span class="sxs-lookup"><span data-stu-id="64d50-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="64d50-115">クライアントとサービス ・ プロバイダーは、この相互運用性を有効にするには、フラグ、文字の文字列の交換を伴う方法で Unicode がサポートされていることを示す MAPI_UNICODE フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="64d50-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="64d50-116">たとえば、クライアントは、Unicode をサポートしているし、フォルダーの表示名を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64d50-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="64d50-117">すべてのクライアントの PT_TSTRING プロパティをコンパイルするには PT_UNICODE を入力します。</span><span class="sxs-lookup"><span data-stu-id="64d50-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="64d50-118">表示名の文字列が Unicode 形式で返されることを要求するのには MAPI_UNICODE フラグを渡す、クライアントがその**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティを取得するためにフォルダーの[IMAPIProp::GetProps](imapiprop-getprops.md)のメソッドを呼び出すと、.</span><span class="sxs-lookup"><span data-stu-id="64d50-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="64d50-119">クライアントとサービス ・ プロバイダーは、要求だけは、メソッドの呼び出しで文字セットを指定することに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64d50-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="64d50-120">オブジェクトの実装者は、1 つまたは両方の文字セットをサポートします。</span><span class="sxs-lookup"><span data-stu-id="64d50-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="64d50-121">ただし、サービス プロバイダーは、1 セットだけをサポートするプロバイダーよりも広範囲の配布を達成するためにできるため、両方の文字セットをサポートすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="64d50-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="64d50-122">文字列プロパティは、バイナリのプロパティと同様に非常に大きくなるまで拡張できます: プロパティを使用するプロパティは、PT_BINARY を入力します。</span><span class="sxs-lookup"><span data-stu-id="64d50-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="64d50-123">大きなプロパティの操作を容易にするためは、MAPI は、サイズの制限を適用するのには、これらのプロパティを設定するサービス プロバイダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="64d50-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="64d50-124">これらの制限は、によって異なります。</span><span class="sxs-lookup"><span data-stu-id="64d50-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="64d50-125">プロパティがされているかどうかを読み取ったり書き込んだりします。</span><span class="sxs-lookup"><span data-stu-id="64d50-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="64d50-126">サービス プロバイダーが、 **IMAPIProp**メソッドを実装する方法です。</span><span class="sxs-lookup"><span data-stu-id="64d50-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="64d50-127">メモリの制約などの実行時の考慮事項</span><span class="sxs-lookup"><span data-stu-id="64d50-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="64d50-128">文字セットの変換の問題です。</span><span class="sxs-lookup"><span data-stu-id="64d50-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="64d50-129">文字列のサイズの制限を配置することもしもすべての大規模なプロパティの値が表示されるようにすることはないためテーブルの列で使用すると、バイナリのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="64d50-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="64d50-130">多くのサービス プロバイダーには、大きな文字列または 255 バイトをテーブルで使用されているバイナリのプロパティが切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="64d50-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="64d50-131">クライアントは、大きな文字列またはバイナリのプロパティを操作するのには、オブジェクトの**GetProps**または**SetProps**メソッドを呼び出すし、プロパティのサイズであるため、呼び出しは失敗、エラー値 MAPI_E_NOT_ENOUGH_MEMORY を返します。</span><span class="sxs-lookup"><span data-stu-id="64d50-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="64d50-132">**GetProps**の特定のプロパティの不足している場合で[IMAPIProp::OpenProperty](imapiprop-openproperty.md)を呼び出すと、インターフェイス識別子として IID_IStream を指定することによってアクセスの**IStream**を要求するクライアントを回復できます。</span><span class="sxs-lookup"><span data-stu-id="64d50-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="64d50-133">クライアントは、 **OpenProperty**を使用するなど、大きなプロパティを操作するために適している**IStream**インターフェイスを使用して大規模なプロパティを取得できます。</span><span class="sxs-lookup"><span data-stu-id="64d50-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64d50-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="64d50-134">See also</span></span>



[<span data-ttu-id="64d50-135">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="64d50-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

