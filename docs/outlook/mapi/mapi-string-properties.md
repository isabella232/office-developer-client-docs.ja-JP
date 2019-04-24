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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309521"
---
# <a name="mapi-string-properties"></a><span data-ttu-id="71087-103">MAPI 文字列のプロパティ</span><span class="sxs-lookup"><span data-stu-id="71087-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="71087-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71087-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71087-105">MAPI には、文字列プロパティを説明する3つの異なるプロパティの種類が用意されています。</span><span class="sxs-lookup"><span data-stu-id="71087-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="71087-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="71087-106">PT_TSTRING</span></span>
  
<span data-ttu-id="71087-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="71087-107">PT_STRING8</span></span>
  
<span data-ttu-id="71087-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="71087-108">PT_UNICODE</span></span>
  
<span data-ttu-id="71087-109">文字列プロパティは、最も一般的に PT_TSTRING として定義されています。</span><span class="sxs-lookup"><span data-stu-id="71087-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="71087-110">PT_TSTRING プロパティの型は、UNICODE マクロが定義されているかどうかに応じて、他の文字列型のプロパティのうちの1つに条件付きでコンパイルされます。</span><span class="sxs-lookup"><span data-stu-id="71087-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="71087-111">PT_STRING8 は、ANSI 形式の8ビットの null 終端文字列を記述します。PT_UNICODE は、2バイトの null で終わる文字列を記述します。</span><span class="sxs-lookup"><span data-stu-id="71087-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="71087-112">クライアントまたはサービスプロバイダー、あるいはクライアントとプロバイダーの両方が Unicode 文字列をサポートするかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="71087-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="71087-113">必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="71087-113">It is not required.</span></span> <span data-ttu-id="71087-114">PT_STRING8 文字列のみをサポートするクライアントは、Unicode とその逆をサポートするプロバイダーで操作できます。</span><span class="sxs-lookup"><span data-stu-id="71087-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="71087-115">この相互運用性を有効にするために、クライアントとサービスプロバイダーはフラグ (MAPI_UNICODE フラグ) を渡して、文字列の交換を伴うメソッドで UNICODE がサポートされていることを示します。</span><span class="sxs-lookup"><span data-stu-id="71087-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="71087-116">たとえば、クライアントが Unicode をサポートしており、フォルダーの表示名を取得する必要があるとします。</span><span class="sxs-lookup"><span data-stu-id="71087-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="71087-117">すべてのクライアントの PT_TSTRING プロパティは、PT_UNICODE 型にコンパイルされます。</span><span class="sxs-lookup"><span data-stu-id="71087-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="71087-118">クライアントがフォルダーの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを取得するときに、MAPI_UNICODE フラグを渡して、表示名文字列が UNICODE 形式で返されることを要求します。.</span><span class="sxs-lookup"><span data-stu-id="71087-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="71087-119">クライアントおよびサービスプロバイダーは、メソッド呼び出しで文字セットを指定することは要求のみであることに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71087-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="71087-120">1つまたは両方の文字セットをサポートすることは、オブジェクトの実装側になります。</span><span class="sxs-lookup"><span data-stu-id="71087-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="71087-121">ただし、サービスプロバイダーは、1つのセットのみをサポートするプロバイダーよりも広範囲に分散を実現できるため、両方の文字セットをサポートすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="71087-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="71087-122">文字列プロパティは、バイナリプロパティと同じように大きくなる可能性があります。プロパティの型 PT_BINARY を使用するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="71087-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="71087-123">大きなプロパティの操作を簡単にするために、MAPI では、これらのプロパティを設定してサイズ制限を適用することができます。</span><span class="sxs-lookup"><span data-stu-id="71087-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="71087-124">これらの制限は、以下によって異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="71087-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="71087-125">プロパティの読み取りまたは書き込みを行うかどうか。</span><span class="sxs-lookup"><span data-stu-id="71087-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="71087-126">サービスプロバイダーが**imapiprop**メソッドを実装する方法。</span><span class="sxs-lookup"><span data-stu-id="71087-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="71087-127">メモリ制約などの実行時の考慮事項。</span><span class="sxs-lookup"><span data-stu-id="71087-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="71087-128">文字セットの変換の問題。</span><span class="sxs-lookup"><span data-stu-id="71087-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="71087-129">サイズ制限は、大きなプロパティの値をすべて表示することができなくなる場合があるため、テーブルの列セットで使用されている場合は、文字列およびバイナリプロパティに配置することもできます。</span><span class="sxs-lookup"><span data-stu-id="71087-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="71087-130">多くのサービスプロバイダーは、表で使用されている大きな文字列またはバイナリのプロパティを255バイトに切り捨てます。</span><span class="sxs-lookup"><span data-stu-id="71087-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="71087-131">クライアントがオブジェクトの**GetProps**または**setprops**メソッドを呼び出して、大きな文字列またはバイナリプロパティを処理するときに、プロパティのサイズが原因で呼び出しが失敗した場合、このメソッドはエラー値 MAPI_E_NOT_ENOUGH_MEMORY を返します。</span><span class="sxs-lookup"><span data-stu-id="71087-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="71087-132">特定のプロパティに対してエラーが発生している**GetProps**の場合、クライアントは[imapiprop:: openproperty](imapiprop-openproperty.md)を呼び出し、IID_IStream をインターフェイス識別子として指定して、アクセス用の**IStream**を要求することによって回復できます。</span><span class="sxs-lookup"><span data-stu-id="71087-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="71087-133">**openproperty**を使用すると、クライアントは、大きなプロパティの処理により適した**IStream**などのインターフェイスを使用して、ラージプロパティを取得できます。</span><span class="sxs-lookup"><span data-stu-id="71087-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="71087-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="71087-134">See also</span></span>



[<span data-ttu-id="71087-135">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="71087-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

