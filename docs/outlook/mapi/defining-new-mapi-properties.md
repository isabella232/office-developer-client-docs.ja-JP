---
title: 新しい MAPI プロパティの定義
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a2325ea-ddfa-480f-b65f-f5b20471fb40
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 666ee413319765e39e25d586208f764afc93ae6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425016"
---
# <a name="defining-new-mapi-properties"></a><span data-ttu-id="63cfb-103">新しい MAPI プロパティの定義</span><span class="sxs-lookup"><span data-stu-id="63cfb-103">Defining New MAPI Properties</span></span>

  
  
<span data-ttu-id="63cfb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63cfb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63cfb-105">クライアントとサービス プロバイダーが使用するために MAPI によって提供される豊富なプロパティにもかかわらず、MAPI を使用すると、必要に応じて新しいプロパティを作成できます。</span><span class="sxs-lookup"><span data-stu-id="63cfb-105">In spite of the wealth of properties supplied by MAPI for use by clients and service providers, MAPI enables new properties to be created if necessary.</span></span> <span data-ttu-id="63cfb-106">新しいパブリック プロパティを定義するための有効なシナリオには、新しいメッセージ クラスをサポートするプロパティを作成するクライアントと、一意のメッセージング システム機能を公開するための新しいプロパティを作成するサービス プロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="63cfb-106">Some of the valid scenarios for defining new public properties include a client creating properties to support a new message class and a service provider creating new properties to expose unique messaging system features.</span></span>
  
<span data-ttu-id="63cfb-107">通常、サービス プロバイダーが既存の MAPI オブジェクトまたはメッセージ クラスの新しいプロパティを定義するには無効です。</span><span class="sxs-lookup"><span data-stu-id="63cfb-107">It is typically not valid for a service provider to define new properties for an existing MAPI object or message class.</span></span> <span data-ttu-id="63cfb-108">MAPI を使用する主な利点の 1 つは、多数のメッセージング システム要素の標準識別子と形式が設定され、ユーザーがサービス プロバイダーをシームレスに組み合わせ、一致できる点です。</span><span class="sxs-lookup"><span data-stu-id="63cfb-108">One of the primary benefits of using MAPI is that standard identifiers and formats for a large number of messaging system elements are set up, enabling users to seamlessly mix and match service providers.</span></span> <span data-ttu-id="63cfb-109">標準以外のプロパティを使用するサービス プロバイダーは、他のサービス プロバイダーと同様に機能しません。</span><span class="sxs-lookup"><span data-stu-id="63cfb-109">Service providers that use nonstandard properties do not work as well with other service providers.</span></span> 
  
<span data-ttu-id="63cfb-110">クライアントは、次の方法で新しいメッセージ クラスのコンテンツ プロパティを作成できます。</span><span class="sxs-lookup"><span data-stu-id="63cfb-110">Clients can create content properties for new message classes by:</span></span>
  
- <span data-ttu-id="63cfb-111">メッセージ クラス固有のコンテンツ プロパティに指定範囲内のプロパティ識別子を使用する。</span><span class="sxs-lookup"><span data-stu-id="63cfb-111">Using property identifiers within a designated range for message class-specific content properties.</span></span>
    
    - <span data-ttu-id="63cfb-112">Or -</span><span class="sxs-lookup"><span data-stu-id="63cfb-112">Or -</span></span>
    
- <span data-ttu-id="63cfb-113">名前付きプロパティの使用。</span><span class="sxs-lookup"><span data-stu-id="63cfb-113">Using named properties.</span></span> 
    
<span data-ttu-id="63cfb-114">最初のオプションが望ましいのは、すべてのサービス プロバイダーが名前付きプロパティをサポートしている場合ではないのでです。</span><span class="sxs-lookup"><span data-stu-id="63cfb-114">The first option is preferable because not all service providers support named properties.</span></span> <span data-ttu-id="63cfb-115">MAPI では、クライアントが新しいメッセージ クラス固有のコンテンツ プロパティに使用する 2 つの個別の範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="63cfb-115">MAPI defines two separate ranges for clients to use for new message class-specific content properties:</span></span>
  
- <span data-ttu-id="63cfb-116">0x6800プロパティ0x7BFFを設定する方法</span><span class="sxs-lookup"><span data-stu-id="63cfb-116">0x6800 to 0x7BFF for transmittable properties</span></span>
    
- <span data-ttu-id="63cfb-117">0x7C00、0x7FFFのプロパティを使用する方法</span><span class="sxs-lookup"><span data-stu-id="63cfb-117">0x7C00 to 0x7FFF for nontransmittable properties</span></span>
    
<span data-ttu-id="63cfb-118">プロパティ識別子は、異なるベンダーまたはユーザーによって定義されたプロパティ間の競合を防ぐのに役立つ定義済みの範囲に含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="63cfb-118">Property identifiers must fall in predefined ranges to help prevent collisions between properties defined by different vendors or users.</span></span> <span data-ttu-id="63cfb-119">ただし、これらの範囲のプロパティのユーザーは、プロパティの動作を前提とすることはできません。</span><span class="sxs-lookup"><span data-stu-id="63cfb-119">However, users of properties in these ranges cannot make assumptions as to the behavior of the properties.</span></span> <span data-ttu-id="63cfb-120">新しいメッセージ クラスを作成するすべてのクライアントは、これらの範囲にアクセスできます。識別子  _xxxx_ を持つプロパティは、1 つのメッセージ クラスに対する 1 つの動作と、別のメッセージ クラスの別の動作を意味します。</span><span class="sxs-lookup"><span data-stu-id="63cfb-120">Every client that creates a new message class has access to these ranges; a property with identifier  _xxxx_ can mean one behavior for one message class and another behavior for another message class.</span></span> 
  
<span data-ttu-id="63cfb-121">名前付きプロパティは、特定のプロパティがメッセージ クラスに固有のプロパティを保証するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="63cfb-121">Named properties are used to guarantee a specific property is unique to a message class.</span></span> <span data-ttu-id="63cfb-122">名前付きプロパティ識別子は、指定した範囲0x8000開始します。</span><span class="sxs-lookup"><span data-stu-id="63cfb-122">Named property identifiers start in the 0x8000 range.</span></span> <span data-ttu-id="63cfb-123">クライアントは 1 つ以上の名前を定義し、メッセージ ストアの [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) メソッドを呼び出して、識別子を各名前に関連付ける。</span><span class="sxs-lookup"><span data-stu-id="63cfb-123">Clients define one or more names and then call the message store's [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to associate an identifier with each name.</span></span> <span data-ttu-id="63cfb-124">名前付きプロパティは、オブジェクトの所有者が名前付きプロパティをサポートしている場合にのみ、クライアントまたはサービス プロバイダーが任意のオブジェクトの新しいプロパティを定義するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="63cfb-124">Named properties can be used by clients or service providers to define new properties for any object only if the owner of the object supports named properties.</span></span> <span data-ttu-id="63cfb-125">これらのプロパティのユーザーは **、GetIDsFromNames** と関連 **する IMAPIProp** メソッド [GetNamesFromIDs](imapiprop-getnamesfromids.md)を呼び出して、名前とその識別子の間をマップします。</span><span class="sxs-lookup"><span data-stu-id="63cfb-125">Users of these properties call **GetIDsFromNames** and a related **IMAPIProp** method, [GetNamesFromIDs](imapiprop-getnamesfromids.md), to map between a name and its identifier.</span></span>
  
<span data-ttu-id="63cfb-126">すべてのプロパティ (新規または既存) では、定義済みのプロパティの種類のセットを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63cfb-126">All properties, new or existing, must use the set of predefined property types.</span></span> <span data-ttu-id="63cfb-127">新しいプロパティの種類を追加することはできません。既存の型を変更または削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="63cfb-127">New property types cannot be added and existing types cannot be modified or deleted.</span></span> <span data-ttu-id="63cfb-128">1 文字または 16 ビットの整数プロパティなどの単純で小さいプロパティは、任意の適切な型に格納できます。</span><span class="sxs-lookup"><span data-stu-id="63cfb-128">Simple, small properties, such as single-character or 16-bit integer properties, can be stored in any appropriate type.</span></span> <span data-ttu-id="63cfb-129">たとえば、整数は **ULONG** として格納し、文字列は次 **のように格納** PT_STRING8。</span><span class="sxs-lookup"><span data-stu-id="63cfb-129">For example, integers can be stored as **ULONG** and strings can be stored as **PT_STRING8**.</span></span> 
  
<span data-ttu-id="63cfb-130">カウントされた **バイトPT_BINARY** を示すために、この型を使用します。</span><span class="sxs-lookup"><span data-stu-id="63cfb-130">Use the **PT_BINARY** type to indicate a counted byte array.</span></span> <span data-ttu-id="63cfb-131">このプロパティの種類は、オブジェクトに格納できるデータの種類を拡張する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="63cfb-131">This property type is useful for extending the types of data that can be stored in an object.</span></span> <span data-ttu-id="63cfb-132">バイトは順序に基づいて送信され、データの意味に関する前提は作成されません。</span><span class="sxs-lookup"><span data-stu-id="63cfb-132">Bytes are transmitted in sequence and no assumptions are made about the meaning of the data.</span></span> <span data-ttu-id="63cfb-133">クライアント アプリケーションがそのようなプロパティからデータを読み取る場合、データは保存方法から変更されません。</span><span class="sxs-lookup"><span data-stu-id="63cfb-133">When a client application reads data out of such a property, the data is unchanged from how it was stored.</span></span> <span data-ttu-id="63cfb-134">クライアントは、CPU 間でデータを移動するときに必要なバイト スワップを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63cfb-134">The client must perform any necessary byte swapping when moving data across CPUs.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="63cfb-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="63cfb-135">See also</span></span>



[<span data-ttu-id="63cfb-136">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="63cfb-136">MAPI Property Overview</span></span>](mapi-property-overview.md)

