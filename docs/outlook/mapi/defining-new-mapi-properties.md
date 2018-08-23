---
title: 新しい MAPI プロパティを定義します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a2325ea-ddfa-480f-b65f-f5b20471fb40
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f922ee95cda84311d840aa9de339883c57efba56
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590324"
---
# <a name="defining-new-mapi-properties"></a><span data-ttu-id="5ad78-103">新しい MAPI プロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="5ad78-103">Defining New MAPI Properties</span></span>

  
  
<span data-ttu-id="5ad78-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ad78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ad78-105">にもかかわらず、クライアントとサービスのプロバイダーで使用するため、MAPI によって提供されるプロパティの豊富なは、MAPI は、必要な場合に作成する新しいプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5ad78-105">In spite of the wealth of properties supplied by MAPI for use by clients and service providers, MAPI enables new properties to be created if necessary.</span></span> <span data-ttu-id="5ad78-106">いくつかの新しいパブリック プロパティを定義するための有効なシナリオには、新しいメッセージ クラスと新しいプロパティを作成する独自のメッセージング システムの機能を公開するサービス プロバイダーをサポートするためにプロパティを作成するクライアントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5ad78-106">Some of the valid scenarios for defining new public properties include a client creating properties to support a new message class and a service provider creating new properties to expose unique messaging system features.</span></span>
  
<span data-ttu-id="5ad78-107">通常、既存の MAPI オブジェクトまたはメッセージ クラスの新しいプロパティを定義するのにはサービス ・ プロバイダーに対して無効です。</span><span class="sxs-lookup"><span data-stu-id="5ad78-107">It is typically not valid for a service provider to define new properties for an existing MAPI object or message class.</span></span> <span data-ttu-id="5ad78-108">識別子の標準と形式の要素を設定して、シームレスに混在させるし、一致するユーザーを有効にすると、メッセージング システムの多数のサービスのプロバイダーが、MAPI を使用する場合の主な利点の 1 つ。</span><span class="sxs-lookup"><span data-stu-id="5ad78-108">One of the primary benefits of using MAPI is that standard identifiers and formats for a large number of messaging system elements are set up, enabling users to seamlessly mix and match service providers.</span></span> <span data-ttu-id="5ad78-109">非標準プロパティを使用するサービス プロバイダーは他のサービス プロバイダーにも機能しません。</span><span class="sxs-lookup"><span data-stu-id="5ad78-109">Service providers that use nonstandard properties do not work as well with other service providers.</span></span> 
  
<span data-ttu-id="5ad78-110">クライアントは、新しいメッセージ クラスのコンテンツのプロパティを作成できます。</span><span class="sxs-lookup"><span data-stu-id="5ad78-110">Clients can create content properties for new message classes by:</span></span>
  
- <span data-ttu-id="5ad78-111">メッセージ クラスに固有のコンテンツ プロパティの指定された範囲内のプロパティの識別子を使用しています。</span><span class="sxs-lookup"><span data-stu-id="5ad78-111">Using property identifiers within a designated range for message class-specific content properties.</span></span>
    
    - <span data-ttu-id="5ad78-112">または、</span><span class="sxs-lookup"><span data-stu-id="5ad78-112">Or -</span></span>
    
- <span data-ttu-id="5ad78-113">名前付きプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="5ad78-113">Using named properties.</span></span> 
    
<span data-ttu-id="5ad78-114">すべてのサービス プロバイダーが名前付きプロパティをサポートしているために、最初のオプションの使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5ad78-114">The first option is preferable because not all service providers support named properties.</span></span> <span data-ttu-id="5ad78-115">MAPI には、新規のメッセージ クラスに固有のコンテンツ プロパティを使用するクライアントの 2 つの別の範囲が定義されています。</span><span class="sxs-lookup"><span data-stu-id="5ad78-115">MAPI defines two separate ranges for clients to use for new message class-specific content properties:</span></span>
  
- <span data-ttu-id="5ad78-116">転送可能なプロパティの 0x6800 に 0x7BFF</span><span class="sxs-lookup"><span data-stu-id="5ad78-116">0x6800 to 0x7BFF for transmittable properties</span></span>
    
- <span data-ttu-id="5ad78-117">0x7C00 に 0x7FFF nontransmittable のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5ad78-117">0x7C00 to 0x7FFF for nontransmittable properties</span></span>
    
<span data-ttu-id="5ad78-118">プロパティ識別子は、さまざまなベンダー、またはユーザーによって定義されたプロパティとの間の衝突を防ぐための定義済みの範囲である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ad78-118">Property identifiers must fall in predefined ranges to help prevent collisions between properties defined by different vendors or users.</span></span> <span data-ttu-id="5ad78-119">ただし、これらの範囲内のプロパティのユーザーは、プロパティの動作についての前提条件を作成できません。</span><span class="sxs-lookup"><span data-stu-id="5ad78-119">However, users of properties in these ranges cannot make assumptions as to the behavior of the properties.</span></span> <span data-ttu-id="5ad78-120">新しいメッセージ クラスを作成するすべてのクライアントがこれらの範囲へのアクセス権を持つ_xxxx_の識別子を持つプロパティは、1 つのメッセージ クラスの 1 つの動作ともう 1 つのメッセージ クラスの別の動作を意味します。</span><span class="sxs-lookup"><span data-stu-id="5ad78-120">Every client that creates a new message class has access to these ranges; a property with identifier  _xxxx_ can mean one behavior for one message class and another behavior for another message class.</span></span> 
  
<span data-ttu-id="5ad78-121">名前付きプロパティは、特定のプロパティは、メッセージ クラスを一意に保証するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ad78-121">Named properties are used to guarantee a specific property is unique to a message class.</span></span> <span data-ttu-id="5ad78-122">0x8000 の範囲の名前付きプロパティの識別子を開始します。</span><span class="sxs-lookup"><span data-stu-id="5ad78-122">Named property identifiers start in the 0x8000 range.</span></span> <span data-ttu-id="5ad78-123">クライアントでは、1 つまたは複数の名前を定義し、それぞれの名前と識別子を関連付けるには、メッセージ ストアの[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="5ad78-123">Clients define one or more names and then call the message store's [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to associate an identifier with each name.</span></span> <span data-ttu-id="5ad78-124">名前付きプロパティは、オブジェクトの所有者は、名前付きプロパティをサポートしている場合にのみ、任意のオブジェクトの新しいプロパティを定義するのには、クライアントまたはサービス プロバイダーによって使用できます。</span><span class="sxs-lookup"><span data-stu-id="5ad78-124">Named properties can be used by clients or service providers to define new properties for any object only if the owner of the object supports named properties.</span></span> <span data-ttu-id="5ad78-125">これらのプロパティのユーザー名と識別子にマップするには、 **GetIDsFromNames**と関連する**IMAPIProp**メソッドでは、 [GetNamesFromIDs](imapiprop-getnamesfromids.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5ad78-125">Users of these properties call **GetIDsFromNames** and a related **IMAPIProp** method, [GetNamesFromIDs](imapiprop-getnamesfromids.md), to map between a name and its identifier.</span></span>
  
<span data-ttu-id="5ad78-126">新規または既存のすべてのプロパティは、一連の定義済みのプロパティの種類を使用してください。</span><span class="sxs-lookup"><span data-stu-id="5ad78-126">All properties, new or existing, must use the set of predefined property types.</span></span> <span data-ttu-id="5ad78-127">新しいプロパティの種類を追加することはできませんし、既存の型を変更または削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="5ad78-127">New property types cannot be added and existing types cannot be modified or deleted.</span></span> <span data-ttu-id="5ad78-128">任意の適切な型では、単純で小さななどのプロパティを単一の文字または 16 ビット整数のプロパティを格納できます。</span><span class="sxs-lookup"><span data-stu-id="5ad78-128">Simple, small properties, such as single-character or 16-bit integer properties, can be stored in any appropriate type.</span></span> <span data-ttu-id="5ad78-129">たとえば、 **ulong 型**として整数を格納することができ、 **PT_STRING8**として文字列を格納することができます。</span><span class="sxs-lookup"><span data-stu-id="5ad78-129">For example, integers can be stored as **ULONG** and strings can be stored as **PT_STRING8**.</span></span> 
  
<span data-ttu-id="5ad78-130">**PT_BINARY**型を使用して、長さのバイト配列を示します。</span><span class="sxs-lookup"><span data-stu-id="5ad78-130">Use the **PT_BINARY** type to indicate a counted byte array.</span></span> <span data-ttu-id="5ad78-131">この種類のプロパティは、オブジェクトに格納できるデータの型を拡張するのに便利です。</span><span class="sxs-lookup"><span data-stu-id="5ad78-131">This property type is useful for extending the types of data that can be stored in an object.</span></span> <span data-ttu-id="5ad78-132">シーケンスで送信されるバイト数とデータの意味に関する前提条件は行われません。</span><span class="sxs-lookup"><span data-stu-id="5ad78-132">Bytes are transmitted in sequence and no assumptions are made about the meaning of the data.</span></span> <span data-ttu-id="5ad78-133">クライアント アプリケーションでは、これらのプロパティからデータを読み取る、ときに、データをどのように保存されてから変更することはありません。</span><span class="sxs-lookup"><span data-stu-id="5ad78-133">When a client application reads data out of such a property, the data is unchanged from how it was stored.</span></span> <span data-ttu-id="5ad78-134">クライアントでは、Cpu 間でデータを移動するときの交換のために必要なバイトを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ad78-134">The client must perform any necessary byte swapping when moving data across CPUs.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ad78-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ad78-135">See also</span></span>



[<span data-ttu-id="5ad78-136">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="5ad78-136">MAPI Property Overview</span></span>](mapi-property-overview.md)

