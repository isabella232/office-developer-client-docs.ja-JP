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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435048"
---
# <a name="mapi-named-properties"></a><span data-ttu-id="22fef-103">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="22fef-103">MAPI Named Properties</span></span>
 
<span data-ttu-id="22fef-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22fef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22fef-105">MAPI は、プロパティに名前を割り当てる機能、これらの名前を一意の識別子にマッピングし、このマッピングを永続的に行う機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="22fef-105">MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent.</span></span> <span data-ttu-id="22fef-106">識別子マッピングに対する永続的な名前を使用すると、セッション間でプロパティ名が有効なままになります。</span><span class="sxs-lookup"><span data-stu-id="22fef-106">Persistent name to identifier mapping ensures that property names remain valid across sessions.</span></span>
  
<span data-ttu-id="22fef-107">名前付きプロパティを定義するには、クライアントまたはサービス プロバイダーが名前を構成し [、MAPINAMEID 構造に格納](mapinameid.md) します。</span><span class="sxs-lookup"><span data-stu-id="22fef-107">To define a named property, a client or service provider makes up a name and stores it in a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="22fef-108">名前は 32 ビットのグローバル一意識別子 (GUID) と Unicode 文字文字列または数値ででなされるので、名前付きプロパティの作成者は重複を恐れずに意味のある名前を作成できます。</span><span class="sxs-lookup"><span data-stu-id="22fef-108">Because names are made up of a 32-bit globally unique identifier, or GUID, and either a Unicode character string or numeric value, creators of named properties can create meaningful names without fear of duplication.</span></span> <span data-ttu-id="22fef-109">名前は一意であり、識別子の値に関係なく使用できます。</span><span class="sxs-lookup"><span data-stu-id="22fef-109">Names are unique and they can be used without regard to the value of their identifiers.</span></span> 
  
<span data-ttu-id="22fef-110">名前付きプロパティをサポートするために、サービス プロバイダーは [、IMAPIProp:::GetIDsFromNames](imapiprop-getidsfromnames.md) と [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) の 2 つのメソッドを実装して、名前と識別子の間で変換し [、IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) メソッドが名前付きプロパティ範囲の識別子を持つプロパティを取得および変更できます。</span><span class="sxs-lookup"><span data-stu-id="22fef-110">To support named properties, a service provider implements two methods — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — to translate between names and identifiers and to allow its [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) methods to retrieve and modify properties with identifiers in the named property range.</span></span> <span data-ttu-id="22fef-111">名前付きプロパティ識別子の範囲は、0x8000と0xFFFE。</span><span class="sxs-lookup"><span data-stu-id="22fef-111">The range for named property identifiers is between 0x8000 and 0xFFFE.</span></span> 
  
<span data-ttu-id="22fef-112">**IMAPIProp** インターフェイスを実装するオブジェクトは、名前付きプロパティをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="22fef-112">Any object that implements the **IMAPIProp** interface can support named properties.</span></span> <span data-ttu-id="22fef-113">このサポートを提供するには、他のプロバイダーのエントリをコンテナーにコピーできるアドレス帳プロバイダーと、任意のメッセージの種類を作成するために使用できるメッセージ ストア プロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="22fef-113">Address book providers that allow entries from other providers to be copied into their containers and message store providers that can be used to create arbitrary message types are required to supply this support.</span></span> <span data-ttu-id="22fef-114">これは、他のすべてのサービス プロバイダーのオプションです。</span><span class="sxs-lookup"><span data-stu-id="22fef-114">It is an option for all other service providers.</span></span> <span data-ttu-id="22fef-115">名前付きプロパティをサポートしていないプロバイダーは **、GetIDsFromNames** メソッドと **GetNamesFromIDs** メソッドから MAPI_E_NO_SUPPORT を返し、0x8000 以上の識別子を持つプロパティの設定を拒否し **、SPropProblemarray** で MAPI_E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="22fef-115">Providers that do not support named properties return MAPI_E_NO_SUPPORT from the **GetIDsFromNames** and **GetNamesFromIDs** methods and refuse to set any properties with identifiers of 0x8000 or greater, returning MAPI_E_UNEXPECTED in the **SPropProblemarray**.</span></span>
  
<span data-ttu-id="22fef-116">プロパティの名前を作成する方法の 1 つは、クライアントが既存のメッセージ クラスまたはカスタム メッセージ クラスの新しいプロパティを定義する方法の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="22fef-116">Creating names for properties is one way for clients to define new properties for existing or custom message classes.</span></span> <span data-ttu-id="22fef-117">サービス プロバイダーは、名前付きプロパティを使用して、メッセージング システムの一意の機能を公開できます。</span><span class="sxs-lookup"><span data-stu-id="22fef-117">Service providers can use named properties to expose unique features of their messaging systems.</span></span> <span data-ttu-id="22fef-118">名前付きプロパティのもう 1 つの使い方は、以下の識別子を持つプロパティを参照する別の方法を提供0x8000。</span><span class="sxs-lookup"><span data-stu-id="22fef-118">Yet another use for named properties is to provide an alternate way of referring to properties with identifiers below 0x8000.</span></span> 
  
<span data-ttu-id="22fef-119">たとえば、クライアントは次のようなコードを使用して、オブジェクトのすべての名前付きプロパティの名前を取得できます。</span><span class="sxs-lookup"><span data-stu-id="22fef-119">For example, a client could use code similar to the following code to retrieve the names for all of an object's named properties:</span></span>
  
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

<span data-ttu-id="22fef-120">PS_PUBLIC_STRINGS プロパティ セットからすべての名前を要求するには、クライアントはプロパティ セット パラメーターの NULL を次のようにPS_PUBLIC_STRINGS置き換えます。</span><span class="sxs-lookup"><span data-stu-id="22fef-120">To request all names from the PS_PUBLIC_STRINGS property set, a client would replace the NULL in the property set parameter to PS_PUBLIC_STRINGS as follows:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="22fef-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="22fef-121">See also</span></span>

- [<span data-ttu-id="22fef-122">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="22fef-122">MAPI Property Overview</span></span>](mapi-property-overview.md)

