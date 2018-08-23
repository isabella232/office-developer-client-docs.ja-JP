---
title: MAPI プロパティ識別子の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 725256a64cb7d55be494ba623247255dfe5936c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801421"
---
# <a name="mapi-property-identifier-overview"></a><span data-ttu-id="23c74-103">MAPI プロパティ識別子の概要</span><span class="sxs-lookup"><span data-stu-id="23c74-103">MAPI Property Identifier Overview</span></span>

  
  
<span data-ttu-id="23c74-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23c74-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23c74-105">プロパティの識別子は、プロパティの使用を示すために使用される番号およびその責任者です。</span><span class="sxs-lookup"><span data-stu-id="23c74-105">A property identifier is a number that is used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="23c74-106">プロパティ識別子は、MAPI によって範囲に分かれています。識別子が範囲に該当する場所は、その使用法と所有権を示します。</span><span class="sxs-lookup"><span data-stu-id="23c74-106">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="23c74-107">プロパティ識別子の範囲は、0x0001 から 0 xffff まで実行されます。</span><span class="sxs-lookup"><span data-stu-id="23c74-107">The range of property identifiers runs from 0x0001 through 0xFFFF.</span></span> <span data-ttu-id="23c74-108">0x0000 と 0 xffff のプロパティ識別子は、すべての場合、これらの識別子を未使用に残す必要があることを意味に予約されています。</span><span class="sxs-lookup"><span data-stu-id="23c74-108">Property identifiers 0x0000 and 0xFFFF are reserved in all cases, meaning that these identifiers must remain unused.</span></span> <span data-ttu-id="23c74-109">MAPI によって定義されているプロパティの範囲は、0x0001 からから 0x3FFF を実行します。</span><span class="sxs-lookup"><span data-stu-id="23c74-109">The range for properties defined by MAPI runs from 0x0001 to 0x3FFF.</span></span> <span data-ttu-id="23c74-110">これらのプロパティは、MAPI 定義のプロパティと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="23c74-110">These properties are referred to as MAPI-defined properties.</span></span> <span data-ttu-id="23c74-111">メッセージと受信者のプロパティが属する範囲 0x7FFF を 0x4000 と、クライアントまたはサービス プロバイダーは、この範囲のプロパティを定義できます。</span><span class="sxs-lookup"><span data-stu-id="23c74-111">The range 0x4000 to 0x7FFF belongs to message and recipient properties, and either clients or service providers can define properties in this range.</span></span> <span data-ttu-id="23c74-112">0x0001 に 0x7FFF の範囲内のプロパティは、タグ付きのプロパティと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="23c74-112">Properties in the range of 0x0001 to 0x7FFF are referred to as tagged properties.</span></span> <span data-ttu-id="23c74-113">0x8000 を超える、名前付きプロパティ、または 32 ビットのグローバル一意識別子 (GUID) が、Unicode 文字の文字列または数値の値を含むプロパティと呼ばれるものの範囲です。</span><span class="sxs-lookup"><span data-stu-id="23c74-113">Beyond 0x8000 is the range for what is known as named properties, or properties that include a 32-bit globally unique identifier (GUID) and either a Unicode character string or numeric value.</span></span> <span data-ttu-id="23c74-114">クライアントは、そのプロパティの設定をカスタマイズするのには、名前付きプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="23c74-114">Clients can use named properties to customize their property set.</span></span>
  
<span data-ttu-id="23c74-115">サービス プロバイダーは、0x67FF から 0x67F0 の範囲で、セキュリティで保護されたプロファイル プロパティを定義できます。</span><span class="sxs-lookup"><span data-stu-id="23c74-115">Service providers can define secure profile properties in the range 0x67F0 through 0x67FF.</span></span> <span data-ttu-id="23c74-116">プロファイルのプロパティは、パスワードなどの追加の保護を必要とする情報の使用をセキュリティで保護します。</span><span class="sxs-lookup"><span data-stu-id="23c74-116">Secure profile properties are used for information that requires additional protection, such as passwords.</span></span> <span data-ttu-id="23c74-117">これらのプロパティを非表示にし、暗号化します。</span><span class="sxs-lookup"><span data-stu-id="23c74-117">These properties can be hidden and encrypted.</span></span> <span data-ttu-id="23c74-118">[IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドによって返されるプロパティの既定の一覧でセキュリティで保護されたプロパティが含まれているかどうかは、プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="23c74-118">Whether or not secure properties are included in the default list of properties returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method depends on the provider's implementation.</span></span> <span data-ttu-id="23c74-119">通常これらのプロパティは含まれません。</span><span class="sxs-lookup"><span data-stu-id="23c74-119">Usually these properties are not included.</span></span> <span data-ttu-id="23c74-120">[IProfSect: IMAPIProp](iprofsectimapiprop.md)インターフェイスは、セキュリティで保護されたプロパティを含む、プロファイル セクションのプロパティにアクセスするために使用します。</span><span class="sxs-lookup"><span data-stu-id="23c74-120">The [IProfSect : IMAPIProp](iprofsectimapiprop.md) interface is used for accessing the properties of a profile section, including secure properties.</span></span> 
  
<span data-ttu-id="23c74-121">プロパティの範囲のいくつかの機能は、転送可能なプロパティまたはプロパティを nontransmittable に制限されます。</span><span class="sxs-lookup"><span data-stu-id="23c74-121">Some of the property ranges are restricted to transmittable properties or nontransmittable properties.</span></span> <span data-ttu-id="23c74-122">転送可能なプロパティは、メッセージに転送されます。nontransmittable プロパティは、メッセージは転送されません。</span><span class="sxs-lookup"><span data-stu-id="23c74-122">Transmittable properties are transferred with a message; nontransmittable properties are not transferred with a message.</span></span> <span data-ttu-id="23c74-123">Nontransmittable プロパティには、通常、クライアントとサービス プロバイダーが現在のセッションで動作するだけの価値のある情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="23c74-123">Nontransmittable properties usually contain information that is of value only to clients and service providers operating with the current session.</span></span> <span data-ttu-id="23c74-124">これらのプロパティは必ずしも別のメッセージング システムとサービス ・ プロバイダーの別のセットに便利です。</span><span class="sxs-lookup"><span data-stu-id="23c74-124">These properties would not necessarily be useful to another messaging system and another set of service providers.</span></span> <span data-ttu-id="23c74-125">転送可能なプロパティの概念は、トランスポート プロバイダーに主に適用されます。</span><span class="sxs-lookup"><span data-stu-id="23c74-125">The concept of transmittable properties applies primarily to transport providers.</span></span> <span data-ttu-id="23c74-126">かプロパティが送信できるかどうかを確認するのには、 **FIsTransmittable**マクロは、Mapitags.h ヘッダー ファイルで定義する、プロパティ タグを渡します。</span><span class="sxs-lookup"><span data-stu-id="23c74-126">To determine whether a property is transmittable or not, pass its property tag to the **FIsTransmittable** macro, defined in the Mapitags.h header file.</span></span> 
  
<span data-ttu-id="23c74-127">識別子の範囲の詳細については、[プロパティ識別子の範囲](property-identifier-ranges.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23c74-127">For a complete description of the identifier ranges, see [Property Identifier Ranges](property-identifier-ranges.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23c74-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="23c74-128">See also</span></span>



[<span data-ttu-id="23c74-129">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="23c74-129">MAPI Property Overview</span></span>](mapi-property-overview.md)

