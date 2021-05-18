---
title: プロパティ名とプロパティ セット
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fa9d6afcaf1b360f37e8c8873c9d1a823fcd4888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328547"
---
# <a name="property-names-and-property-sets"></a><span data-ttu-id="5bda6-103">プロパティ名とプロパティ セット</span><span class="sxs-lookup"><span data-stu-id="5bda6-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="5bda6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bda6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bda6-105">名前付きプロパティの名前には、次の 2 つの部分があります。</span><span class="sxs-lookup"><span data-stu-id="5bda6-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="5bda6-106">プロパティ セットを指定するグローバル一意識別子 (GUID)。</span><span class="sxs-lookup"><span data-stu-id="5bda6-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="5bda6-107">Unicode 文字文字列または 32 ビットの数値。</span><span class="sxs-lookup"><span data-stu-id="5bda6-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="5bda6-108">名前付きプロパティの名前については [、MAPINAMEID 構造を使用して説明](mapinameid.md) します。</span><span class="sxs-lookup"><span data-stu-id="5bda6-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="5bda6-109">この構造体には、プロパティ セット メンバー、数値形式または文字列形式で名前を指定するためのメンバー、および使用される形式を識別するためのメンバーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5bda6-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="5bda6-110">プロパティ セットはプロパティの名前の一部なので、省略可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="5bda6-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="5bda6-111">MAPI では、クライアントとサービス プロバイダーが使用する複数のプロパティ セットを定義していますが、既存のプロパティ セットが不適切な場合は、新しいプロパティ セットを定義できます。</span><span class="sxs-lookup"><span data-stu-id="5bda6-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="5bda6-112">クライアントとサービス プロバイダーは [、CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) 関数を呼び出すことによって、独自のプロパティ セットを定義できます。</span><span class="sxs-lookup"><span data-stu-id="5bda6-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) function.</span></span> <span data-ttu-id="5bda6-113">通常、これらのプロパティ セットはカスタム クライアント アプリケーション用に作成されます。</span><span class="sxs-lookup"><span data-stu-id="5bda6-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="5bda6-114">MAPI のプロパティ セットは、次の定数で表されます。</span><span class="sxs-lookup"><span data-stu-id="5bda6-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="5bda6-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="5bda6-115">PS_MAPI</span></span>
  
<span data-ttu-id="5bda6-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="5bda6-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="5bda6-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="5bda6-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="5bda6-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="5bda6-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="5bda6-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="5bda6-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="5bda6-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="5bda6-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="5bda6-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5bda6-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="5bda6-122">プロパティ PS_MAPIは予約済みです。サービス プロバイダーは、名前付きプロパティ範囲の下に識別子を持つプロパティの名前を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5bda6-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="5bda6-123">ipM PS_PUBLIC_STRINGSの名前付きプロパティに対してクライアントが使用するプロパティセットです。</span><span class="sxs-lookup"><span data-stu-id="5bda6-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="5bda6-124">PS_PUBLIC_STRINGS プロパティ セットの名前付きプロパティはクライアントのユーザー インターフェイスに表示されるので、IPC メッセージ クラスに属するメッセージなどの表示できないメッセージは、このプロパティ セットを使用して名前付きプロパティを作成しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bda6-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="5bda6-125">代わりに、メッセージ クラス固有の範囲でプロパティを作成し、0x6800を0x7FFF。</span><span class="sxs-lookup"><span data-stu-id="5bda6-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="5bda6-126">他のプロパティ セットには、通常、ルーティング リストのメンバーである受信者を示す名前付きプロパティが保持されます。</span><span class="sxs-lookup"><span data-stu-id="5bda6-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="5bda6-127">受信者リスト のプロパティに関連付けられているプロパティと同じ種類の情報を含むこれらのプロパティ セットのプロパティは、ターゲット メッセージング システムのマッピングを必要とするゲートウェイによって理解されます。</span><span class="sxs-lookup"><span data-stu-id="5bda6-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="5bda6-128">プロパティを記述するための情報は 5 種類あるため、MAPI では 5 つの異なるプロパティ セットが定義されています。</span><span class="sxs-lookup"><span data-stu-id="5bda6-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="5bda6-129">ルーティング リスト メンバーのアドレスとアドレスの種類を含める必要があるメッセージを送信するクライアントは、PS_ROUTING_EMAIL_ADDRESSES および PS_ROUTING_ADDRTYPE プロパティ セット内の各メンバーに名前付きプロパティを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="5bda6-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="5bda6-130">これにより、外部メッセージング システムに送信するときに、アドレスとアドレスの種類が有効なままになります。</span><span class="sxs-lookup"><span data-stu-id="5bda6-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5bda6-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="5bda6-131">See also</span></span>



[<span data-ttu-id="5bda6-132">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="5bda6-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

