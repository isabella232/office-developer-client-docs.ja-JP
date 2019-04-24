---
title: MAPI ���O�t���v���p�e�B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d83b98b4f06c648676852673a694a63b78f568b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345865"
---
# <a name="mapi-named-properties"></a><span data-ttu-id="a0316-103">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="a0316-103">MAPI Named Properties</span></span>
 
<span data-ttu-id="a0316-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0316-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0316-105">MAPI には、プロパティに名前を割り当てたり、これらの名前を一意の識別子にマップしたり、このマッピングを永続的にするための機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="a0316-105">MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent.</span></span> <span data-ttu-id="a0316-106">id マッピングの永続名を指定すると、プロパティ名はセッション間で有効なままになります。</span><span class="sxs-lookup"><span data-stu-id="a0316-106">Persistent name to identifier mapping ensures that property names remain valid across sessions.</span></span>
  
<span data-ttu-id="a0316-107">名前付きプロパティを定義するには、クライアントまたはサービスプロバイダーが名前を作成し、それを[mapinameid](mapinameid.md)構造に格納します。</span><span class="sxs-lookup"><span data-stu-id="a0316-107">To define a named property, a client or service provider makes up a name and stores it in a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="a0316-108">名前は32ビットのグローバル一意識別子 (GUID) と、Unicode 文字列または数値のいずれかで構成されるため、名前付きプロパティの作成者は、重複を恐れることなく、わかりやすい名前を作成できます。</span><span class="sxs-lookup"><span data-stu-id="a0316-108">Because names are made up of a 32-bit globally unique identifier, or GUID, and either a Unicode character string or numeric value, creators of named properties can create meaningful names without fear of duplication.</span></span> <span data-ttu-id="a0316-109">名前は一意であり、識別子の値に関係なく使用できます。</span><span class="sxs-lookup"><span data-stu-id="a0316-109">Names are unique and they can be used without regard to the value of their identifiers.</span></span> 
  
<span data-ttu-id="a0316-110">名前付きプロパティをサポートするために、サービスプロバイダーは、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)と[imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)の2つのメソッドを実装して、名前と識別子の間を変換し、その[imapiprop:: GetProps](imapiprop-getprops.md) [を許可します。imapiprop:: setprops](imapiprop-setprops.md)メソッドを使用して、名前付きプロパティの範囲内の識別子を持つプロパティを取得および変更します。</span><span class="sxs-lookup"><span data-stu-id="a0316-110">To support named properties, a service provider implements two methods — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — to translate between names and identifiers and to allow its [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) methods to retrieve and modify properties with identifiers in the named property range.</span></span> <span data-ttu-id="a0316-111">名前付きプロパティの識別子の範囲は、0x8000 ~ 0xFFFE です。</span><span class="sxs-lookup"><span data-stu-id="a0316-111">The range for named property identifiers is between 0x8000 and 0xFFFE.</span></span> 
  
<span data-ttu-id="a0316-112">**imapiprop**インターフェイスを実装するオブジェクトは、名前付きプロパティをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="a0316-112">Any object that implements the **IMAPIProp** interface can support named properties.</span></span> <span data-ttu-id="a0316-113">このサポートを提供するために、他のプロバイダーからのエントリをコンテナーにコピーし、任意のメッセージの種類を作成するために使用できるメッセージストアプロバイダーを使用できるようにするアドレス帳プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="a0316-113">Address book providers that allow entries from other providers to be copied into their containers and message store providers that can be used to create arbitrary message types are required to supply this support.</span></span> <span data-ttu-id="a0316-114">他のすべてのサービスプロバイダーのオプションです。</span><span class="sxs-lookup"><span data-stu-id="a0316-114">It is an option for all other service providers.</span></span> <span data-ttu-id="a0316-115">名前付きプロパティをサポートしないプロバイダーは、 **getidsfromnames**および**GetNamesFromIDs**メソッドから MAPI_E_NO_SUPPORT を返し、0x8000 以上**の識別子を持つプロパティを設定することを拒否します。spropの配列**。</span><span class="sxs-lookup"><span data-stu-id="a0316-115">Providers that do not support named properties return MAPI_E_NO_SUPPORT from the **GetIDsFromNames** and **GetNamesFromIDs** methods and refuse to set any properties with identifiers of 0x8000 or greater, returning MAPI_E_UNEXPECTED in the **SPropProblemarray**.</span></span>
  
<span data-ttu-id="a0316-116">プロパティの名前を作成することは、クライアントが既存またはカスタムのメッセージクラスの新しいプロパティを定義する1つの方法です。</span><span class="sxs-lookup"><span data-stu-id="a0316-116">Creating names for properties is one way for clients to define new properties for existing or custom message classes.</span></span> <span data-ttu-id="a0316-117">サービスプロバイダーは、名前付きプロパティを使用して、メッセージングシステムの固有の機能を公開できます。</span><span class="sxs-lookup"><span data-stu-id="a0316-117">Service providers can use named properties to expose unique features of their messaging systems.</span></span> <span data-ttu-id="a0316-118">さらに、名前付きプロパティを使用する別の方法として、0x8000 未満の識別子を持つプロパティを参照する別の方法を提供しています。</span><span class="sxs-lookup"><span data-stu-id="a0316-118">Yet another use for named properties is to provide an alternate way of referring to properties with identifiers below 0x8000.</span></span> 
  
<span data-ttu-id="a0316-119">たとえば、クライアントは次のようなコードを使用して、オブジェクトのすべての名前付きプロパティの名前を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="a0316-119">For example, a client could use code similar to the following code to retrieve the names for all of an object's named properties:</span></span>
  
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

<span data-ttu-id="a0316-120">PS_PUBLIC_STRINGS プロパティセットからすべての名前を要求する場合、クライアントは次のように、property set パラメーターの NULL を PS_PUBLIC_STRINGS に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="a0316-120">To request all names from the PS_PUBLIC_STRINGS property set, a client would replace the NULL in the property set parameter to PS_PUBLIC_STRINGS as follows:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="a0316-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0316-121">See also</span></span>

- [<span data-ttu-id="a0316-122">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="a0316-122">MAPI Property Overview</span></span>](mapi-property-overview.md)

