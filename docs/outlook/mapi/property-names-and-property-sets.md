---
title: プロパティ名とプロパティ セット
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c586d70054542e8d20c90a8caceafabbbb408de8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803731"
---
# <a name="property-names-and-property-sets"></a><span data-ttu-id="9c691-103">プロパティ名とプロパティ セット</span><span class="sxs-lookup"><span data-stu-id="9c691-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="9c691-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c691-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9c691-105">すべての名前付きプロパティの名前には、2 つの部分があります。</span><span class="sxs-lookup"><span data-stu-id="9c691-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="9c691-106">グローバルに一意の識別子または GUID では、プロパティ セットを指定します。</span><span class="sxs-lookup"><span data-stu-id="9c691-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="9c691-107">Unicode 文字の文字列、または 32 ビットの数値です。</span><span class="sxs-lookup"><span data-stu-id="9c691-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="9c691-108">[MAPINAMEID](mapinameid.md)構造体を使用して、名前付きプロパティの名前を説明します。</span><span class="sxs-lookup"><span data-stu-id="9c691-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="9c691-109">この構造体には、プロパティ セットのメンバー、メンバーの名前を指定する数値または文字列のいずれかの形式でどちらの形式が使用される特定のメンバーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9c691-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="9c691-110">プロパティ セット、プロパティ名の一部であるために、省略可能なことはできません。</span><span class="sxs-lookup"><span data-stu-id="9c691-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="9c691-111">MAPI には、クライアントとサービス ・ プロバイダーで使用するためのいくつかのプロパティ セットが定義されているが、既存のプロパティ セットが適切でない場合は、新しいプロパティ セットを定義できます。</span><span class="sxs-lookup"><span data-stu-id="9c691-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="9c691-112">クライアントとサービス ・ プロバイダーは、 [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx)関数を呼び出すことによって、独自のプロパティ セットを定義できます。</span><span class="sxs-lookup"><span data-stu-id="9c691-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx) function.</span></span> <span data-ttu-id="9c691-113">通常これらのプロパティ セットは、カスタム クライアント アプリケーションの作成されます。</span><span class="sxs-lookup"><span data-stu-id="9c691-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="9c691-114">MAPI のプロパティ セットは、次の定数によって表されます。</span><span class="sxs-lookup"><span data-stu-id="9c691-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="9c691-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="9c691-115">PS_MAPI</span></span>
  
<span data-ttu-id="9c691-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="9c691-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="9c691-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="9c691-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="9c691-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="9c691-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="9c691-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="9c691-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="9c691-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="9c691-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="9c691-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9c691-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="9c691-122">PS_MAPI プロパティ セットは予約されています。名前付きプロパティの範囲の下の識別子を持つプロパティの名前を生成するサービス プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="9c691-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="9c691-123">PS_PUBLIC_STRINGS プロパティ セットは、IPM メッセージの名前付きプロパティをクライアントによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="9c691-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="9c691-124">PS_PUBLIC_STRINGS プロパティ セットの名前付きプロパティがあるためにという名前のプロパティをこのプロパティを設定を非表示のメッセージを作成しないように IPC メッセージ クラスに属している必要があります次のようにクライアントのユーザー インターフェイスで表示します。</span><span class="sxs-lookup"><span data-stu-id="9c691-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="9c691-125">代わりに、メッセージ クラスに固有の範囲、0x7FFF を 0x6800 にプロパティを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c691-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="9c691-126">その他のプロパティ セットは、通常のルーティングの一覧のメンバーである受信者を説明する名前付きのプロパティを保持します。</span><span class="sxs-lookup"><span data-stu-id="9c691-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="9c691-127">同じ種類の受信者のリストのプロパティに関連付けられているプロパティの情報を含む、これらのプロパティ セットにプロパティが理解ゲートウェイ メッセージング システムのターゲットのマッピングを必要とします。</span><span class="sxs-lookup"><span data-stu-id="9c691-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="9c691-128">5 種類のプロパティを記述するための情報があるため、MAPI が 5 つの異なるプロパティ セットを定義します。</span><span class="sxs-lookup"><span data-stu-id="9c691-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="9c691-129">メッセージのルーティングの一覧のメンバーのアドレスおよびアドレス タイプを含める必要があります PS_ROUTING_EMAIL_ADDRESSES 内の各メンバーの名前付きプロパティと PS_ROUTING_ADDRTYPE プロパティの割り当てを送信するクライアントを設定します。</span><span class="sxs-lookup"><span data-stu-id="9c691-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="9c691-130">これにより、アドレスとアドレスの種類は外部のメッセージング システムに送信されるときに実行可能なことです。</span><span class="sxs-lookup"><span data-stu-id="9c691-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9c691-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c691-131">See also</span></span>



[<span data-ttu-id="9c691-132">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="9c691-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

