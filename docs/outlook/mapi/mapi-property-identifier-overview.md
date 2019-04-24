---
title: MAPI プロパティ識別子の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 29626f49365a0f37f1e13d965c62bfd5ad0fb774
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328188"
---
# <a name="mapi-property-identifier-overview"></a><span data-ttu-id="7ea07-103">MAPI プロパティ識別子の概要</span><span class="sxs-lookup"><span data-stu-id="7ea07-103">MAPI Property Identifier Overview</span></span>

  
  
<span data-ttu-id="7ea07-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ea07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ea07-105">プロパティ識別子は、プロパティがどのように使用されているかを示すために使用される番号です。</span><span class="sxs-lookup"><span data-stu-id="7ea07-105">A property identifier is a number that is used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="7ea07-106">プロパティ識別子は MAPI で範囲に分割されます。範囲内の識別子は、その使用と所有権を示します。</span><span class="sxs-lookup"><span data-stu-id="7ea07-106">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="7ea07-107">プロパティ識別子の範囲は、0x0001 から0xffff で実行されます。</span><span class="sxs-lookup"><span data-stu-id="7ea07-107">The range of property identifiers runs from 0x0001 through 0xFFFF.</span></span> <span data-ttu-id="7ea07-108">プロパティ識別子0x0000 および0xffff は常に予約されています。つまり、これらの識別子は使用しないままにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ea07-108">Property identifiers 0x0000 and 0xFFFF are reserved in all cases, meaning that these identifiers must remain unused.</span></span> <span data-ttu-id="7ea07-109">MAPI で定義されているプロパティの範囲は、0x0001 から0x3fff に対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="7ea07-109">The range for properties defined by MAPI runs from 0x0001 to 0x3FFF.</span></span> <span data-ttu-id="7ea07-110">これらのプロパティは、MAPI で定義されたプロパティと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="7ea07-110">These properties are referred to as MAPI-defined properties.</span></span> <span data-ttu-id="7ea07-111">"0x4000 から" という範囲は、message プロパティおよび recipient プロパティに属しており、クライアントまたはサービスプロバイダーはこの範囲内のプロパティを定義できます。</span><span class="sxs-lookup"><span data-stu-id="7ea07-111">The range 0x4000 to 0x7FFF belongs to message and recipient properties, and either clients or service providers can define properties in this range.</span></span> <span data-ttu-id="7ea07-112">0x0001 の範囲内のプロパティは、タグ付きプロパティと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="7ea07-112">Properties in the range of 0x0001 to 0x7FFF are referred to as tagged properties.</span></span> <span data-ttu-id="7ea07-113">0x8000 を超えると、名前付きプロパティと呼ばれるもの、または32ビットのグローバル一意識別子 (GUID) を含むプロパティ、Unicode 文字列または数値のいずれかの値が指定されます。</span><span class="sxs-lookup"><span data-stu-id="7ea07-113">Beyond 0x8000 is the range for what is known as named properties, or properties that include a 32-bit globally unique identifier (GUID) and either a Unicode character string or numeric value.</span></span> <span data-ttu-id="7ea07-114">クライアントは、名前付きプロパティを使用して、プロパティセットをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="7ea07-114">Clients can use named properties to customize their property set.</span></span>
  
<span data-ttu-id="7ea07-115">サービスプロバイダーは、範囲 0x67f0 ~ 0x67f0 で、セキュリティで保護されたプロファイルプロパティを定義できます。</span><span class="sxs-lookup"><span data-stu-id="7ea07-115">Service providers can define secure profile properties in the range 0x67F0 through 0x67FF.</span></span> <span data-ttu-id="7ea07-116">セキュリティで保護されたプロファイルプロパティは、パスワードなどの追加の保護を必要とする情報に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7ea07-116">Secure profile properties are used for information that requires additional protection, such as passwords.</span></span> <span data-ttu-id="7ea07-117">これらのプロパティは、非表示と暗号化が可能です。</span><span class="sxs-lookup"><span data-stu-id="7ea07-117">These properties can be hidden and encrypted.</span></span> <span data-ttu-id="7ea07-118">[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドによって返されるプロパティの既定のリストにセキュリティで保護されたプロパティが含まれるかどうかは、プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="7ea07-118">Whether or not secure properties are included in the default list of properties returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method depends on the provider's implementation.</span></span> <span data-ttu-id="7ea07-119">通常、これらのプロパティは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="7ea07-119">Usually these properties are not included.</span></span> <span data-ttu-id="7ea07-120">[IProfSect: imapiprop](iprofsectimapiprop.md)インターフェイスは、セキュリティで保護されたプロパティを含む、プロファイルセクションのプロパティへのアクセスに使用されます。</span><span class="sxs-lookup"><span data-stu-id="7ea07-120">The [IProfSect : IMAPIProp](iprofsectimapiprop.md) interface is used for accessing the properties of a profile section, including secure properties.</span></span> 
  
<span data-ttu-id="7ea07-121">プロパティ範囲の中には、複数のテーブルプロパティまたはノン非対称テーブルプロパティに制限があります。</span><span class="sxs-lookup"><span data-stu-id="7ea07-121">Some of the property ranges are restricted to transmittable properties or nontransmittable properties.</span></span> <span data-ttu-id="7ea07-122">送信テーブルのプロパティは、メッセージと共に転送されます。ノン非対称テーブルのプロパティは、メッセージと共に転送されません。</span><span class="sxs-lookup"><span data-stu-id="7ea07-122">Transmittable properties are transferred with a message; nontransmittable properties are not transferred with a message.</span></span> <span data-ttu-id="7ea07-123">通常、ノン非対称テーブルプロパティには、現在のセッションで動作しているクライアントおよびサービスプロバイダーにのみ価値のある情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7ea07-123">Nontransmittable properties usually contain information that is of value only to clients and service providers operating with the current session.</span></span> <span data-ttu-id="7ea07-124">これらのプロパティは、他のメッセージングシステムや別のサービスプロバイダーにとっては、必ずしも役に立つわけではありません。</span><span class="sxs-lookup"><span data-stu-id="7ea07-124">These properties would not necessarily be useful to another messaging system and another set of service providers.</span></span> <span data-ttu-id="7ea07-125">送信テーブルプロパティの概念は、主にトランスポートプロバイダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="7ea07-125">The concept of transmittable properties applies primarily to transport providers.</span></span> <span data-ttu-id="7ea07-126">プロパティが FIsTransmittable のテーブルであるかどうかを判断するには、Mapitags ヘッダーファイルで定義されている\*\*\*\* マクロにプロパティタグを渡します。</span><span class="sxs-lookup"><span data-stu-id="7ea07-126">To determine whether a property is transmittable or not, pass its property tag to the **FIsTransmittable** macro, defined in the Mapitags.h header file.</span></span> 
  
<span data-ttu-id="7ea07-127">識別子の範囲の詳細については、「[プロパティ識別子の範囲](property-identifier-ranges.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7ea07-127">For a complete description of the identifier ranges, see [Property Identifier Ranges](property-identifier-ranges.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ea07-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="7ea07-128">See also</span></span>



[<span data-ttu-id="7ea07-129">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="7ea07-129">MAPI Property Overview</span></span>](mapi-property-overview.md)

