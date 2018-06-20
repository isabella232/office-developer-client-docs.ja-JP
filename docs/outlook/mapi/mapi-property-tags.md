---
title: MAPI プロパティ タグ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8dc37f1b594eeaa199b48f5946d10e60427d4988
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801434"
---
# <a name="mapi-property-tags"></a><span data-ttu-id="c987b-103">MAPI プロパティ タグ</span><span class="sxs-lookup"><span data-stu-id="c987b-103">MAPI property tags</span></span>
  
<span data-ttu-id="c987b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c987b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c987b-105">プロパティ タグは、16 から 31 のビットの一意のプロパティ識別子とプロパティの型のビット 0 ~ 15 は次の図に示すように含まれている 32 ビットの数値です。</span><span class="sxs-lookup"><span data-stu-id="c987b-105">A property tag is a 32-bit number that contains a unique property identifier in bits 16 through 31 and a property type in bits 0 through 15 as shown in the following illustration.</span></span> 
  
<span data-ttu-id="c987b-106">**プロパティ タグの要素**</span><span class="sxs-lookup"><span data-stu-id="c987b-106">**Property tag elements**</span></span>
  
<span data-ttu-id="c987b-107">![プロパティ タグの要素](media/amapi_10.gif "プロパティ タグの要素")</span><span class="sxs-lookup"><span data-stu-id="c987b-107">![Property tag elements](media/amapi_10.gif "Property tag elements")</span></span>
  
<span data-ttu-id="c987b-108">プロパティ タグを使用して MAPI プロパティを識別し、すべてのプロパティは、いずれか、MAPI、クライアント、またはサービス プロバイダーによって、プロパティが定義されているかどうかに関係なく必要があります。</span><span class="sxs-lookup"><span data-stu-id="c987b-108">Property tags are used to identify MAPI properties and every property must have one, regardless of whether the property is defined by MAPI, a client, or a service provider.</span></span> <span data-ttu-id="c987b-109">MAPI は、Mapitags.h ヘッダー ファイル内のプロパティのプロパティ タグ定数のセットを定義します。これらのプロパティは、[MAPI 定義のプロパティ] と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="c987b-109">MAPI defines a set of property tag constants for its properties in the Mapitags.h header file; these properties are referred to as the "MAPI-defined properties".</span></span> 
  
<span data-ttu-id="c987b-110">プロパティ タグ定数は、一貫性と使いやすさの名前付け規則に従います。</span><span class="sxs-lookup"><span data-stu-id="c987b-110">The property tag constants follow a naming convention for consistency and ease of use.</span></span> <span data-ttu-id="c987b-111">各プロパティ タグの名前に 2 つの部分がある: PR_ プレフィックスおよびプロパティの内容を説明する 1 つまたは複数の文字の文字列です。</span><span class="sxs-lookup"><span data-stu-id="c987b-111">There are two parts to the name of each property tag: a PR_ prefix and one or more character strings that describe the contents of the property.</span></span> <span data-ttu-id="c987b-112">複数文字の文字列は、アンダー スコアで区切られます。</span><span class="sxs-lookup"><span data-stu-id="c987b-112">Multiple character strings are separated by underscores.</span></span> <span data-ttu-id="c987b-113">メッセージの受信者のアドレスの種類のプロパティ タグは、たとえば、 **PR\_ADDRTYPE** ([PidTagOrgAddrtype](http://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) と、すべての送信メッセージのコピーを受信するように指定されたフォルダーのエントリ id は、 **PR_IPM_SENTMAIL_エントリ ID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="c987b-113">For example, the property tag for the address type of a message recipient is **PR\_ADDRTYPE** ([PidTagOrgAddrtype](http://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) and the entry identifier for the folder designated to receive a copy of every outbound message is **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
  
<span data-ttu-id="c987b-114">[PROP_TYPE](prop_type.md)、 [PROP_ID](prop_id.md)、および[PROP_TAG](prop_tag.md)にそれらの間で、プロパティ タグを付ける作業を支援するいくつかのマクロを利用できます。</span><span class="sxs-lookup"><span data-stu-id="c987b-114">A few macros are available to help work with property tags, among them [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md), and [PROP_TAG](prop_tag.md).</span></span> <span data-ttu-id="c987b-115">**プロペラ\_型**プロパティ タグからプロパティの型を抽出します。**プロペラ\_ID** id を抽出します。</span><span class="sxs-lookup"><span data-stu-id="c987b-115">**PROP\_TYPE** extracts the property type from the property tag; **PROP\_ID** extracts the identifier.</span></span> <span data-ttu-id="c987b-116">**PROP_TAG**は、プロパティの型と識別子のプロパティ タグを作成します。</span><span class="sxs-lookup"><span data-stu-id="c987b-116">**PROP_TAG** builds a property tag from a property type and identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c987b-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="c987b-117">See also</span></span>

- [<span data-ttu-id="c987b-118">MAPI Property Overview</span><span class="sxs-lookup"><span data-stu-id="c987b-118">MAPI Property Overview</span></span>](mapi-property-overview.md)

