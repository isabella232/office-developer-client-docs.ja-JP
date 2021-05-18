---
title: PidTagJunkIncludeContacts 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e61e98d1db1ab3acb958da353d8d22870937632
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328715"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a><span data-ttu-id="f2b9f-103">PidTagJunkIncludeContacts 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f2b9f-103">PidTagJunkIncludeContacts Canonical Property</span></span>

  
  
<span data-ttu-id="f2b9f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2b9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2b9f-105">連絡先フォルダー内の連絡先の電子メール アドレスがスパム フィルターに関して特別に処理されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f2b9f-105">Indicates whether email addresses of the contacts in the Contacts folder are treated specially with respect to the spam filter.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2b9f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f2b9f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f2b9f-107">PR_JUNK_INCLUDE_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="f2b9f-107">PR_JUNK_INCLUDE_CONTACTS</span></span>  <br/> |
|<span data-ttu-id="f2b9f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f2b9f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f2b9f-109">0x6100</span><span class="sxs-lookup"><span data-stu-id="f2b9f-109">0x6100</span></span>  <br/> |
|<span data-ttu-id="f2b9f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f2b9f-110">Data type:</span></span>  <br/> |<span data-ttu-id="f2b9f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f2b9f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f2b9f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f2b9f-112">Area:</span></span>  <br/> |<span data-ttu-id="f2b9f-113">スパム</span><span class="sxs-lookup"><span data-stu-id="f2b9f-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2b9f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f2b9f-114">Remarks</span></span>

<span data-ttu-id="f2b9f-115">"0x00000001" に設定されている場合、これらの電子メール アドレスは、これらのアドレスからのメールが "迷惑メールではない" として扱われるなど、迷惑メール ルール制限の "信頼済み" 連絡先メール アドレス部分を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2b9f-115">If set to "0x00000001", these email addresses must populate the "trusted" contact email address portion of the Junk E-Mail Rule Restriction such that mail from these addresses is treated as "not junk".</span></span> <span data-ttu-id="f2b9f-116">"0x00000000" に設定されている場合、連絡先フォルダーの電子メール アドレスを迷惑メール ルールに追加し、ルールのセクションは NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2b9f-116">If set to "0x00000000", email addresses from the Contacts folder must not be added to the Junk E-Mail Rule, and the section of the rule must be NULL.</span></span>
  
<span data-ttu-id="f2b9f-117">このプロパティに値 "0x00000001" が指定されている場合、追加された連絡先に迷惑メール ルールの信頼できる連絡先セクションにまだ含まれていない電子メール アドレスがある場合は、これらの電子メール アドレスを制限に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2b9f-117">If this property is present with a value of "0x00000001" and if the added contact has email addresses that are not yet included in the trusted contacts section of the Junk E-Mail Rule, those email addresses must be added to the restriction.</span></span> <span data-ttu-id="f2b9f-118">このプロパティが "0x00000000"の場合、アクションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="f2b9f-118">If this property is "0x00000000", no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f2b9f-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f2b9f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f2b9f-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f2b9f-120">Protocol specifications</span></span>

<span data-ttu-id="f2b9f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2b9f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2b9f-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="f2b9f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f2b9f-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2b9f-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2b9f-124">許可/ブロック リストの処理と迷惑メール メッセージの決定を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="f2b9f-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f2b9f-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f2b9f-125">Header files</span></span>

<span data-ttu-id="f2b9f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2b9f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f2b9f-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f2b9f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="f2b9f-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f2b9f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="f2b9f-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f2b9f-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2b9f-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2b9f-130">See also</span></span>



[<span data-ttu-id="f2b9f-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f2b9f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f2b9f-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f2b9f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f2b9f-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f2b9f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f2b9f-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f2b9f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

