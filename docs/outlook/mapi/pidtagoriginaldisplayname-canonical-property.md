---
title: PidTagOriginalDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayName
api_type:
- COM
ms.assetid: 176245d9-724d-44f1-b7a3-eddf652533b2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2b7aef416beb9eee70aeff8cf20cb38ae8e7993f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355609"
---
# <a name="pidtagoriginaldisplayname-canonical-property"></a><span data-ttu-id="94a5d-103">PidTagOriginalDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94a5d-103">PidTagOriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="94a5d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94a5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94a5d-105">アドレス帳から個人用アドレス帳または他の書き込み可能なアドレス帳にコピーされたエントリの元の表示名を含む。</span><span class="sxs-lookup"><span data-stu-id="94a5d-105">Contains the original display name for an entry copied from an address book to a personal address book or other writable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94a5d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="94a5d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94a5d-107">PR_ORIGINAL_DISPLAY_NAME、PR_ORIGINAL_DISPLAY_NAME_A、PR_ORIGINAL_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="94a5d-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="94a5d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="94a5d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="94a5d-109">0x3A13</span><span class="sxs-lookup"><span data-stu-id="94a5d-109">0x3A13</span></span>  <br/> |
|<span data-ttu-id="94a5d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="94a5d-110">Data type:</span></span>  <br/> |<span data-ttu-id="94a5d-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="94a5d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="94a5d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="94a5d-112">Area:</span></span>  <br/> |<span data-ttu-id="94a5d-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="94a5d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94a5d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="94a5d-114">Remarks</span></span>

<span data-ttu-id="94a5d-115">これらのプロパティには、コピーされたエントリの元のソースに関する情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="94a5d-115">These properties contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="94a5d-116">非読み取りレポートの場合、これらのプロパティには、レポートが生成される元のメッセージ受信者の表示名のコピーが含まれる。</span><span class="sxs-lookup"><span data-stu-id="94a5d-116">For a nonread report, these properties contain a copy of the display name of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="94a5d-117">元の受信者が配布リストの一部である場合、配布リストの表示名はレポートに対して保持されます。</span><span class="sxs-lookup"><span data-stu-id="94a5d-117">When the original recipient is part of a distribution list, the display name of the distribution list is preserved for the report.</span></span>
  
<span data-ttu-id="94a5d-118">クライアント アプリケーションは、これらのプロパティを使用して、比較する表示名の変更されていないコピーを与えることによって、エントリの変更や "スプーフィング" を防止できます。</span><span class="sxs-lookup"><span data-stu-id="94a5d-118">A client application can use these properties to prevent alteration or "spoofing" of entries, by giving an unaltered copy of the display name to compare.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="94a5d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="94a5d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="94a5d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="94a5d-120">Protocol specifications</span></span>

<span data-ttu-id="94a5d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94a5d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94a5d-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="94a5d-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="94a5d-123">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94a5d-123">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94a5d-124">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="94a5d-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="94a5d-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="94a5d-125">Header files</span></span>

<span data-ttu-id="94a5d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94a5d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="94a5d-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="94a5d-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="94a5d-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="94a5d-128">Mapitags.h</span></span>
  
> <span data-ttu-id="94a5d-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="94a5d-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94a5d-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="94a5d-130">See also</span></span>



[<span data-ttu-id="94a5d-131">PidTagTransmittableDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94a5d-131">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="94a5d-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="94a5d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94a5d-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94a5d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94a5d-134">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="94a5d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94a5d-135">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="94a5d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

