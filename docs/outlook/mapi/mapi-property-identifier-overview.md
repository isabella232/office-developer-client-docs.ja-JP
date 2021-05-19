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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414698"
---
# <a name="mapi-property-identifier-overview"></a><span data-ttu-id="d94fa-103">MAPI プロパティ識別子の概要</span><span class="sxs-lookup"><span data-stu-id="d94fa-103">MAPI Property Identifier Overview</span></span>

  
  
<span data-ttu-id="d94fa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d94fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d94fa-105">プロパティ識別子は、プロパティの使用およびプロパティの責任者を示すために使用される番号です。</span><span class="sxs-lookup"><span data-stu-id="d94fa-105">A property identifier is a number that is used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="d94fa-106">プロパティ識別子は、MAPI で範囲に分割されます。識別子が範囲内にある場合は、その使用と所有権を示します。</span><span class="sxs-lookup"><span data-stu-id="d94fa-106">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="d94fa-107">プロパティ識別子の範囲は、0x0001から0xFFFF。</span><span class="sxs-lookup"><span data-stu-id="d94fa-107">The range of property identifiers runs from 0x0001 through 0xFFFF.</span></span> <span data-ttu-id="d94fa-108">プロパティの0x0000および0xFFFFは、すべてのケースで予約されます。つまり、これらの識別子は未使用のままである必要があります。</span><span class="sxs-lookup"><span data-stu-id="d94fa-108">Property identifiers 0x0000 and 0xFFFF are reserved in all cases, meaning that these identifiers must remain unused.</span></span> <span data-ttu-id="d94fa-109">MAPI によって定義されるプロパティの範囲は、次の0x0001から0x3FFF。</span><span class="sxs-lookup"><span data-stu-id="d94fa-109">The range for properties defined by MAPI runs from 0x0001 to 0x3FFF.</span></span> <span data-ttu-id="d94fa-110">これらのプロパティは、MAPI 定義プロパティと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d94fa-110">These properties are referred to as MAPI-defined properties.</span></span> <span data-ttu-id="d94fa-111">メッセージと0x4000 0x7FFFに属する範囲であり、クライアントまたはサービス プロバイダーは、この範囲内のプロパティを定義できます。</span><span class="sxs-lookup"><span data-stu-id="d94fa-111">The range 0x4000 to 0x7FFF belongs to message and recipient properties, and either clients or service providers can define properties in this range.</span></span> <span data-ttu-id="d94fa-112">タグ付きプロパティと0x0001 0x7FFFプロパティと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d94fa-112">Properties in the range of 0x0001 to 0x7FFF are referred to as tagged properties.</span></span> <span data-ttu-id="d94fa-113">この0x8000は、名前付きプロパティと呼ばれるプロパティ、または 32 ビットのグローバル一意識別子 (GUID) と Unicode 文字文字列または数値のいずれかを含むプロパティの範囲です。</span><span class="sxs-lookup"><span data-stu-id="d94fa-113">Beyond 0x8000 is the range for what is known as named properties, or properties that include a 32-bit globally unique identifier (GUID) and either a Unicode character string or numeric value.</span></span> <span data-ttu-id="d94fa-114">クライアントは、名前付きプロパティを使用してプロパティ セットをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="d94fa-114">Clients can use named properties to customize their property set.</span></span>
  
<span data-ttu-id="d94fa-115">サービス プロバイダーは、セキュリティで保護されたプロファイル プロパティを、セキュリティで保護されたプロファイル プロパティ0x67F0から0x67FF。</span><span class="sxs-lookup"><span data-stu-id="d94fa-115">Service providers can define secure profile properties in the range 0x67F0 through 0x67FF.</span></span> <span data-ttu-id="d94fa-116">セキュリティで保護されたプロファイル プロパティは、パスワードなどの追加の保護が必要な情報に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d94fa-116">Secure profile properties are used for information that requires additional protection, such as passwords.</span></span> <span data-ttu-id="d94fa-117">これらのプロパティは非表示にし、暗号化できます。</span><span class="sxs-lookup"><span data-stu-id="d94fa-117">These properties can be hidden and encrypted.</span></span> <span data-ttu-id="d94fa-118">[IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドによって返されるプロパティの既定の一覧にセキュリティで保護されたプロパティが含まれているかどうかは、プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="d94fa-118">Whether or not secure properties are included in the default list of properties returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method depends on the provider's implementation.</span></span> <span data-ttu-id="d94fa-119">通常、これらのプロパティは含まれません。</span><span class="sxs-lookup"><span data-stu-id="d94fa-119">Usually these properties are not included.</span></span> <span data-ttu-id="d94fa-120">[IProfSect : IMAPIProp](iprofsectimapiprop.md)インターフェイスは、セキュリティで保護されたプロパティを含むプロファイル セクションのプロパティにアクセスするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d94fa-120">The [IProfSect : IMAPIProp](iprofsectimapiprop.md) interface is used for accessing the properties of a profile section, including secure properties.</span></span> 
  
<span data-ttu-id="d94fa-121">一部のプロパティ範囲は、転送可能なプロパティまたは転送できないプロパティに制限されます。</span><span class="sxs-lookup"><span data-stu-id="d94fa-121">Some of the property ranges are restricted to transmittable properties or nontransmittable properties.</span></span> <span data-ttu-id="d94fa-122">送信可能なプロパティは、メッセージと一緒に転送されます。転送できないプロパティは、メッセージと一緒に転送されません。</span><span class="sxs-lookup"><span data-stu-id="d94fa-122">Transmittable properties are transferred with a message; nontransmittable properties are not transferred with a message.</span></span> <span data-ttu-id="d94fa-123">非送信可能なプロパティには、通常、現在のセッションで動作するクライアントとサービス プロバイダーにのみ価値のある情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d94fa-123">Nontransmittable properties usually contain information that is of value only to clients and service providers operating with the current session.</span></span> <span data-ttu-id="d94fa-124">これらのプロパティは、必ずしも別のメッセージング システムと別のサービス プロバイダーのセットにとって役に立つとは限りません。</span><span class="sxs-lookup"><span data-stu-id="d94fa-124">These properties would not necessarily be useful to another messaging system and another set of service providers.</span></span> <span data-ttu-id="d94fa-125">転送可能なプロパティの概念は、主にトランスポート プロバイダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d94fa-125">The concept of transmittable properties applies primarily to transport providers.</span></span> <span data-ttu-id="d94fa-126">プロパティが送信可能かどうかを判断するには、Mapitags.h ヘッダー ファイルで定義されている **FIsTransmittable** マクロにプロパティ タグを渡します。</span><span class="sxs-lookup"><span data-stu-id="d94fa-126">To determine whether a property is transmittable or not, pass its property tag to the **FIsTransmittable** macro, defined in the Mapitags.h header file.</span></span> 
  
<span data-ttu-id="d94fa-127">識別子範囲の詳細については、「プロパティ識別子の [範囲」を参照してください](property-identifier-ranges.md)。</span><span class="sxs-lookup"><span data-stu-id="d94fa-127">For a complete description of the identifier ranges, see [Property Identifier Ranges](property-identifier-ranges.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d94fa-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="d94fa-128">See also</span></span>



[<span data-ttu-id="d94fa-129">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="d94fa-129">MAPI Property Overview</span></span>](mapi-property-overview.md)

