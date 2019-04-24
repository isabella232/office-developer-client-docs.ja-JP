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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336681"
---
# <a name="defining-new-mapi-properties"></a><span data-ttu-id="32a32-103">新しい MAPI プロパティの定義</span><span class="sxs-lookup"><span data-stu-id="32a32-103">Defining New MAPI Properties</span></span>

  
  
<span data-ttu-id="32a32-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32a32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32a32-105">mapi によってクライアントおよびサービスプロバイダーで使用されるプロパティが豊富になっているにもかかわらず、mapi では、必要に応じて新しいプロパティを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="32a32-105">In spite of the wealth of properties supplied by MAPI for use by clients and service providers, MAPI enables new properties to be created if necessary.</span></span> <span data-ttu-id="32a32-106">新しいパブリックプロパティを定義するための有効なシナリオには、新しいメッセージクラスをサポートするためのプロパティを作成するクライアントと、一意のメッセージングシステム機能を公開するための新しいプロパティを作成するサービスプロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="32a32-106">Some of the valid scenarios for defining new public properties include a client creating properties to support a new message class and a service provider creating new properties to expose unique messaging system features.</span></span>
  
<span data-ttu-id="32a32-107">通常、サービスプロバイダーは、既存の MAPI オブジェクトまたはメッセージクラスの新しいプロパティを定義するのには無効です。</span><span class="sxs-lookup"><span data-stu-id="32a32-107">It is typically not valid for a service provider to define new properties for an existing MAPI object or message class.</span></span> <span data-ttu-id="32a32-108">MAPI を使用する主な利点の1つは、多数のメッセージングシステム要素の標準の識別子と形式が設定されているため、ユーザーがサービスプロバイダーをシームレスに組み合わせて使用できるようになることです。</span><span class="sxs-lookup"><span data-stu-id="32a32-108">One of the primary benefits of using MAPI is that standard identifiers and formats for a large number of messaging system elements are set up, enabling users to seamlessly mix and match service providers.</span></span> <span data-ttu-id="32a32-109">非標準プロパティを使用しているサービスプロバイダーは、他のサービスプロバイダーと同様に機能しません。</span><span class="sxs-lookup"><span data-stu-id="32a32-109">Service providers that use nonstandard properties do not work as well with other service providers.</span></span> 
  
<span data-ttu-id="32a32-110">クライアントは、次の方法で新しいメッセージクラスのコンテンツプロパティを作成できます。</span><span class="sxs-lookup"><span data-stu-id="32a32-110">Clients can create content properties for new message classes by:</span></span>
  
- <span data-ttu-id="32a32-111">メッセージクラス固有のコンテンツプロパティに指定された範囲内でプロパティ識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="32a32-111">Using property identifiers within a designated range for message class-specific content properties.</span></span>
    
    - <span data-ttu-id="32a32-112">や</span><span class="sxs-lookup"><span data-stu-id="32a32-112">Or -</span></span>
    
- <span data-ttu-id="32a32-113">名前付きプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="32a32-113">Using named properties.</span></span> 
    
<span data-ttu-id="32a32-114">すべてのサービスプロバイダーが名前付きプロパティをサポートするわけではないため、最初のオプションが推奨されます。</span><span class="sxs-lookup"><span data-stu-id="32a32-114">The first option is preferable because not all service providers support named properties.</span></span> <span data-ttu-id="32a32-115">MAPI は、クライアントが新しいメッセージクラス固有のコンテンツプロパティに使用する2つの異なる範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="32a32-115">MAPI defines two separate ranges for clients to use for new message class-specific content properties:</span></span>
  
- <span data-ttu-id="32a32-116">0x6800 から 0x7bff (の場合) のプロパティ</span><span class="sxs-lookup"><span data-stu-id="32a32-116">0x6800 to 0x7BFF for transmittable properties</span></span>
    
- <span data-ttu-id="32a32-117">ノン非対称テーブルプロパティの0x7C00</span><span class="sxs-lookup"><span data-stu-id="32a32-117">0x7C00 to 0x7FFF for nontransmittable properties</span></span>
    
<span data-ttu-id="32a32-118">さまざまなベンダーまたはユーザーによって定義されたプロパティ間の競合を防止するため、プロパティ識別子は事前定義された範囲に分類する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32a32-118">Property identifiers must fall in predefined ranges to help prevent collisions between properties defined by different vendors or users.</span></span> <span data-ttu-id="32a32-119">ただし、これらの範囲内のプロパティのユーザーは、プロパティの動作についての仮定を設定できません。</span><span class="sxs-lookup"><span data-stu-id="32a32-119">However, users of properties in these ranges cannot make assumptions as to the behavior of the properties.</span></span> <span data-ttu-id="32a32-120">新しい message クラスを作成するすべてのクライアントは、これらの範囲にアクセスできます。識別子が_xxxx_のプロパティは、1つのメッセージクラスと別のメッセージクラスに対する別の動作の1つの動作を意味します。</span><span class="sxs-lookup"><span data-stu-id="32a32-120">Every client that creates a new message class has access to these ranges; a property with identifier  _xxxx_ can mean one behavior for one message class and another behavior for another message class.</span></span> 
  
<span data-ttu-id="32a32-121">名前付きプロパティは、特定のプロパティがメッセージクラスに対して一意であることを保証するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="32a32-121">Named properties are used to guarantee a specific property is unique to a message class.</span></span> <span data-ttu-id="32a32-122">名前付きプロパティの識別子は、0x8000 の範囲で始まります。</span><span class="sxs-lookup"><span data-stu-id="32a32-122">Named property identifiers start in the 0x8000 range.</span></span> <span data-ttu-id="32a32-123">クライアントは1つ以上の名前を定義し、メッセージストアの[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドを呼び出して、識別子を各名前に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="32a32-123">Clients define one or more names and then call the message store's [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to associate an identifier with each name.</span></span> <span data-ttu-id="32a32-124">名前付きプロパティは、オブジェクトの所有者が名前付きプロパティをサポートしている場合にのみ、任意のオブジェクトの新しいプロパティを定義するために、クライアントまたはサービスプロバイダーが使用できます。</span><span class="sxs-lookup"><span data-stu-id="32a32-124">Named properties can be used by clients or service providers to define new properties for any object only if the owner of the object supports named properties.</span></span> <span data-ttu-id="32a32-125">これらのプロパティのユーザーは、 **getidsfromnames**と、関連する**imapiprop**メソッド[GetNamesFromIDs](imapiprop-getnamesfromids.md)を呼び出して、名前とその識別子の間のマッピングを行います。</span><span class="sxs-lookup"><span data-stu-id="32a32-125">Users of these properties call **GetIDsFromNames** and a related **IMAPIProp** method, [GetNamesFromIDs](imapiprop-getnamesfromids.md), to map between a name and its identifier.</span></span>
  
<span data-ttu-id="32a32-126">新規または既存のすべてのプロパティは、あらかじめ定義されたプロパティの種類のセットを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32a32-126">All properties, new or existing, must use the set of predefined property types.</span></span> <span data-ttu-id="32a32-127">新しいプロパティの種類を追加することはできません。また、既存の種類を変更または削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="32a32-127">New property types cannot be added and existing types cannot be modified or deleted.</span></span> <span data-ttu-id="32a32-128">単純な小さなプロパティ (単一文字または16ビット整数プロパティなど) は、適切な型に格納できます。</span><span class="sxs-lookup"><span data-stu-id="32a32-128">Simple, small properties, such as single-character or 16-bit integer properties, can be stored in any appropriate type.</span></span> <span data-ttu-id="32a32-129">たとえば、整数を**ULONG**として格納し、文字列を**PT_STRING8**として格納することができます。</span><span class="sxs-lookup"><span data-stu-id="32a32-129">For example, integers can be stored as **ULONG** and strings can be stored as **PT_STRING8**.</span></span> 
  
<span data-ttu-id="32a32-130">**PT_BINARY** type を使用して、カウントされたバイト配列を示します。</span><span class="sxs-lookup"><span data-stu-id="32a32-130">Use the **PT_BINARY** type to indicate a counted byte array.</span></span> <span data-ttu-id="32a32-131">このプロパティの種類は、オブジェクトに格納できるデータの種類を拡張する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="32a32-131">This property type is useful for extending the types of data that can be stored in an object.</span></span> <span data-ttu-id="32a32-132">バイトは順に転送され、データの意味については仮定されません。</span><span class="sxs-lookup"><span data-stu-id="32a32-132">Bytes are transmitted in sequence and no assumptions are made about the meaning of the data.</span></span> <span data-ttu-id="32a32-133">クライアントアプリケーションがこのようなプロパティからデータを読み取る場合、データは格納された方法から変更されません。</span><span class="sxs-lookup"><span data-stu-id="32a32-133">When a client application reads data out of such a property, the data is unchanged from how it was stored.</span></span> <span data-ttu-id="32a32-134">クライアントは、cpu 間でデータを移動するときに、必要なバイト交換を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32a32-134">The client must perform any necessary byte swapping when moving data across CPUs.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="32a32-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="32a32-135">See also</span></span>



[<span data-ttu-id="32a32-136">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="32a32-136">MAPI Property Overview</span></span>](mapi-property-overview.md)

