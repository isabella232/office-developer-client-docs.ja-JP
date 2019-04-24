---
title: プロパティ名とプロパティセット
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
# <a name="property-names-and-property-sets"></a><span data-ttu-id="abc36-103">プロパティ名とプロパティセット</span><span class="sxs-lookup"><span data-stu-id="abc36-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="abc36-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abc36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abc36-105">すべての名前付きプロパティの名前は、2つの部分で構成されます。</span><span class="sxs-lookup"><span data-stu-id="abc36-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="abc36-106">プロパティセットを指定するグローバル一意識別子 (GUID)。</span><span class="sxs-lookup"><span data-stu-id="abc36-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="abc36-107">Unicode 文字列または32ビットの数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="abc36-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="abc36-108">名前付きプロパティの名前については、 [mapinameid](mapinameid.md)構造を使用して説明します。</span><span class="sxs-lookup"><span data-stu-id="abc36-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="abc36-109">この構造体には、プロパティセットメンバー、数値または文字列形式のいずれかの名前を指定するメンバ、および使用する形式を識別するメンバが含まれています。</span><span class="sxs-lookup"><span data-stu-id="abc36-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="abc36-110">プロパティセットはプロパティの名前の一部であるため、オプションではありません。</span><span class="sxs-lookup"><span data-stu-id="abc36-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="abc36-111">MAPI では、クライアントとサービスプロバイダーが使用するためにいくつかのプロパティセットが定義されていますが、既存のプロパティセットが適切でない場合は、新しいプロパティセットを定義できます。</span><span class="sxs-lookup"><span data-stu-id="abc36-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="abc36-112">クライアントおよびサービスプロバイダーは、 [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx)関数を呼び出すことによって、独自のプロパティセットを定義できます。</span><span class="sxs-lookup"><span data-stu-id="abc36-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) function.</span></span> <span data-ttu-id="abc36-113">通常、これらのプロパティセットはカスタムクライアントアプリケーション用に作成されます。</span><span class="sxs-lookup"><span data-stu-id="abc36-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="abc36-114">MAPI のプロパティセットは、次の定数で表されます。</span><span class="sxs-lookup"><span data-stu-id="abc36-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="abc36-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="abc36-115">PS_MAPI</span></span>
  
<span data-ttu-id="abc36-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="abc36-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="abc36-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="abc36-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="abc36-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="abc36-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="abc36-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="abc36-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="abc36-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="abc36-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="abc36-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="abc36-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="abc36-122">PS_MAPI プロパティセットは予約されています。このメソッドは、名前付きプロパティの範囲の下に識別子を持つプロパティの名前を生成するために、サービスプロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="abc36-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="abc36-123">PS_PUBLIC_STRINGS プロパティセットは、IPM メッセージの名前付きプロパティのクライアントによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="abc36-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="abc36-124">PS_PUBLIC_STRINGS プロパティセットの名前付きプロパティはクライアントのユーザーインターフェイスに表示されるため、IPC メッセージクラスに属するものなどの非表示のメッセージは、このプロパティセットで名前付きプロパティを作成しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="abc36-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="abc36-125">代わりに、メッセージクラス固有の範囲である 0x6800 ~ で、プロパティを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="abc36-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="abc36-126">その他のプロパティセットは、通常、ルーティングリストのメンバーである受信者を説明する名前付きプロパティを保持します。</span><span class="sxs-lookup"><span data-stu-id="abc36-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="abc36-127">受信者リストのプロパティに関連付けられているプロパティと同じ種類の情報が含まれている場合、これらのプロパティセットのプロパティは、対象のメッセージングシステムへのマッピングを要求するためにゲートウェイによって認識されます。</span><span class="sxs-lookup"><span data-stu-id="abc36-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="abc36-128">プロパティを説明するための情報には5つの種類があるため、MAPI は5つの異なるプロパティセットを定義しています。</span><span class="sxs-lookup"><span data-stu-id="abc36-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="abc36-129">ルーティングリストのメンバーのアドレスとアドレスの種類が含まれている必要があるメッセージを送信するクライアントは、PS_ROUTING_EMAIL_ADDRESSES プロパティと PS_ROUTING_ADDRTYPE プロパティセットの各メンバーに対して名前付きプロパティを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="abc36-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="abc36-130">これにより、外部メッセージングシステムに送信するときに、アドレスとアドレスの種類が引き続き有効になります。</span><span class="sxs-lookup"><span data-stu-id="abc36-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="abc36-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="abc36-131">See also</span></span>



[<span data-ttu-id="abc36-132">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="abc36-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

