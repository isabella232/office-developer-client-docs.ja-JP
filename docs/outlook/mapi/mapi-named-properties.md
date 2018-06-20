---
title: MAPI プロパティを名前付き
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e755c18ef3cc32f9a00169f19cf336eace447a32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801402"
---
# <a name="mapi-named-properties"></a><span data-ttu-id="ae3fe-103">MAPI プロパティを名前付き</span><span class="sxs-lookup"><span data-stu-id="ae3fe-103">MAPI Named Properties</span></span>
 
<span data-ttu-id="ae3fe-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ae3fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ae3fe-105">MAPI には、プロパティに名前を割り当てるため、これらの名前を一意の識別子にマップするため、および永続的なこのマッピングを行うための機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-105">MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent.</span></span> <span data-ttu-id="ae3fe-106">識別子のマッピングへの永続的な名前は、セッション間でプロパティ名が有効なまま、です。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-106">Persistent name to identifier mapping ensures that property names remain valid across sessions.</span></span>
  
<span data-ttu-id="ae3fe-107">名前付きプロパティを定義するには、クライアントまたはサービス プロバイダーの名前になり[MAPINAMEID](mapinameid.md)構造体に格納します。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-107">To define a named property, a client or service provider makes up a name and stores it in a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="ae3fe-108">ための名前は、32 ビットのグローバルに一意の識別子または GUID、およびどちらか、Unicode 文字の文字列または数値の値、名前付きプロパティの作成者は、重複除外を恐れることがなく意味のある名前を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-108">Because names are made up of a 32-bit globally unique identifier, or GUID, and either a Unicode character string or numeric value, creators of named properties can create meaningful names without fear of duplication.</span></span> <span data-ttu-id="ae3fe-109">名が一意では、それらの識別子の値に関係なく使用できます。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-109">Names are unique and they can be used without regard to the value of their identifiers.</span></span> 
  
<span data-ttu-id="ae3fe-110">名前付きプロパティをサポートするためにサービス ・ プロバイダーは 2 つのメソッドを実装する: [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)と[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) -の名前と識別子の間で変換して、 [IMAPIProp::GetProps](imapiprop-getprops.md) [を許可するにはIMAPIProp::SetProps](imapiprop-setprops.md)を取得し、名前付きプロパティの範囲内で識別子とプロパティを変更するためのメソッドです。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-110">To support named properties, a service provider implements two methods — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — to translate between names and identifiers and to allow its [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) methods to retrieve and modify properties with identifiers in the named property range.</span></span> <span data-ttu-id="ae3fe-111">名前付きプロパティの識別子の範囲は 0x8000 から 0 xfffe までの間です。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-111">The range for named property identifiers is between 0x8000 and 0xFFFE.</span></span> 
  
<span data-ttu-id="ae3fe-112">**IMAPIProp**インターフェイスを実装する任意のオブジェクトは、名前付きプロパティをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-112">Any object that implements the **IMAPIProp** interface can support named properties.</span></span> <span data-ttu-id="ae3fe-113">コンテナーとメッセージにコピーするには、他のプロバイダーからのエントリは、任意のメッセージの種類を作成するのに使用できるプロバイダーを格納できるように、アドレス帳プロバイダーは、このサポートを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-113">Address book providers that allow entries from other providers to be copied into their containers and message store providers that can be used to create arbitrary message types are required to supply this support.</span></span> <span data-ttu-id="ae3fe-114">他のすべてのサービス ・ プロバイダー向けのオプションです。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-114">It is an option for all other service providers.</span></span> <span data-ttu-id="ae3fe-115">名前付きプロパティをサポートしないプロバイダーの MAPI_E_NO_SUPPORT メソッドから返す、 **GetIDsFromNames**と**GetNamesFromIDs**と、**で 0x8000 または大きい値、返される MAPI_E_UNEXPECTED の識別子を持つすべてのプロパティを設定するのには拒否します。SPropProblemarray**。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-115">Providers that do not support named properties return MAPI_E_NO_SUPPORT from the **GetIDsFromNames** and **GetNamesFromIDs** methods and refuse to set any properties with identifiers of 0x8000 or greater, returning MAPI_E_UNEXPECTED in the **SPropProblemarray**.</span></span>
  
<span data-ttu-id="ae3fe-116">既存またはカスタムのメッセージ クラスの新しいプロパティを定義するのにはクライアントの 1 つの方法は、プロパティの名前を作成します。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-116">Creating names for properties is one way for clients to define new properties for existing or custom message classes.</span></span> <span data-ttu-id="ae3fe-117">サービス プロバイダーは、それぞれのメッセージング システム固有の機能を公開するのに名前付きプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-117">Service providers can use named properties to expose unique features of their messaging systems.</span></span> <span data-ttu-id="ae3fe-118">まだ別の名前付きプロパティの使用は、0x8000 未満の識別子を持つプロパティを参照する別の方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-118">Yet another use for named properties is to provide an alternate way of referring to properties with identifiers below 0x8000.</span></span> 
  
<span data-ttu-id="ae3fe-119">などのクライアントでは、すべてのオブジェクトの名前付きプロパティの名前を取得するのに次のコードのようなコードを使用する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-119">For example, a client could use code similar to the following code to retrieve the names for all of an object's named properties:</span></span>
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = NULL;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

<span data-ttu-id="ae3fe-120">PS_PUBLIC_STRINGS プロパティのセットからのすべての名前を要求するには、クライアントがプロパティ セットの PS_PUBLIC_STRINGS パラメーターに NULL をとおりに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="ae3fe-120">To request all names from the PS_PUBLIC_STRINGS property set, a client would replace the NULL in the property set parameter to PS_PUBLIC_STRINGS as follows:</span></span> 
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = &PS_PUBLIC_STRINGS;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

## <a name="see-also"></a><span data-ttu-id="ae3fe-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae3fe-121">See also</span></span>

- [<span data-ttu-id="ae3fe-122">MAPI Property Overview</span><span class="sxs-lookup"><span data-stu-id="ae3fe-122">MAPI Property Overview</span></span>](mapi-property-overview.md)

