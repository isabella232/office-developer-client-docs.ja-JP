---
title: MAPI プロパティのタグ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 96211d3b6e1e4dfbd4c93a98c8dd04de10eac884
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328238"
---
# <a name="mapi-property-tags"></a><span data-ttu-id="695ea-103">MAPI プロパティのタグ</span><span class="sxs-lookup"><span data-stu-id="695ea-103">MAPI property tags</span></span>
  
<span data-ttu-id="695ea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="695ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="695ea-105">プロパティ タグは、ビット 16 ~ 31 の一意のプロパティ識別子と、次の図に示すように、ビット 0 ~ 15 のプロパティ型を含む 32 ビットの数値です。</span><span class="sxs-lookup"><span data-stu-id="695ea-105">A property tag is a 32-bit number that contains a unique property identifier in bits 16 through 31 and a property type in bits 0 through 15 as shown in the following illustration.</span></span> 
  
<span data-ttu-id="695ea-106">**プロパティ タグ要素**</span><span class="sxs-lookup"><span data-stu-id="695ea-106">**Property tag elements**</span></span>
  
<span data-ttu-id="695ea-107">![プロパティ タグ要素](media/amapi_10.gif "プロパティ タグ要素")</span><span class="sxs-lookup"><span data-stu-id="695ea-107">![Property tag elements](media/amapi_10.gif "Property tag elements")</span></span>
  
<span data-ttu-id="695ea-108">プロパティ タグは MAPI プロパティを識別するために使用され、プロパティが MAPI、クライアント、またはサービス プロバイダーによって定義されているかどうかに関係なく、すべてのプロパティに 1 つが必要です。</span><span class="sxs-lookup"><span data-stu-id="695ea-108">Property tags are used to identify MAPI properties and every property must have one, regardless of whether the property is defined by MAPI, a client, or a service provider.</span></span> <span data-ttu-id="695ea-109">MAPI は、Mapitags.h ヘッダー ファイル内のプロパティのプロパティ タグ定数のセットを定義します。これらのプロパティは"MAPI 定義プロパティ" と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="695ea-109">MAPI defines a set of property tag constants for its properties in the Mapitags.h header file; these properties are referred to as the "MAPI-defined properties".</span></span> 
  
<span data-ttu-id="695ea-110">プロパティ タグの定数は、一貫性と使いやすさを確保するために名前付け規則に従います。</span><span class="sxs-lookup"><span data-stu-id="695ea-110">The property tag constants follow a naming convention for consistency and ease of use.</span></span> <span data-ttu-id="695ea-111">各プロパティ タグの名前には、1 つのプレフィックスとプロパティPR_説明する 1 つ以上の文字列の 2 つの部分があります。</span><span class="sxs-lookup"><span data-stu-id="695ea-111">There are two parts to the name of each property tag: a PR_ prefix and one or more character strings that describe the contents of the property.</span></span> <span data-ttu-id="695ea-112">複数の文字列はアンダースコアで区切られた文字列です。</span><span class="sxs-lookup"><span data-stu-id="695ea-112">Multiple character strings are separated by underscores.</span></span> <span data-ttu-id="695ea-113">たとえば、メッセージ受信者のアドレスの種類のプロパティ タグは **PR \_ ADDRTYPE** ([PidTagOrgAddrtype)](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)であり、すべての送信メッセージのコピーを受信するために指定されたフォルダーのエントリ識別子は **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)です。</span><span class="sxs-lookup"><span data-stu-id="695ea-113">For example, the property tag for the address type of a message recipient is **PR\_ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) and the entry identifier for the folder designated to receive a copy of every outbound message is **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
  
<span data-ttu-id="695ea-114">プロパティ タグの操作に役立ついくつかのマクロを使用して、[](prop_type.md)プロパティ タグ、PROP_TYPE、PROP_ID、PROP_TAG。 [](prop_tag.md) [](prop_id.md)</span><span class="sxs-lookup"><span data-stu-id="695ea-114">A few macros are available to help work with property tags, among them [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md), and [PROP_TAG](prop_tag.md).</span></span> <span data-ttu-id="695ea-115">**PROP \_TYPE** は、プロパティ タグからプロパティの種類を抽出します。 **PROP \_ID は** 識別子を抽出します。</span><span class="sxs-lookup"><span data-stu-id="695ea-115">**PROP\_TYPE** extracts the property type from the property tag; **PROP\_ID** extracts the identifier.</span></span> <span data-ttu-id="695ea-116">**PROP_TAG** 型と識別子からプロパティ タグを作成します。</span><span class="sxs-lookup"><span data-stu-id="695ea-116">**PROP_TAG** builds a property tag from a property type and identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="695ea-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="695ea-117">See also</span></span>

- [<span data-ttu-id="695ea-118">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="695ea-118">MAPI Property Overview</span></span>](mapi-property-overview.md)

