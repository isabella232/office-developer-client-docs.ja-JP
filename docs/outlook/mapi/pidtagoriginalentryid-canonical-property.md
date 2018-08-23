---
title: PidTagOriginalEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalEntryId
api_type:
- COM
ms.assetid: 8197d2c7-8665-41b8-bd3a-e9c1c2e642e9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: eab72c5b49ba501d8ab5516bf5a5eae9ea82abe0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588707"
---
# <a name="pidtagoriginalentryid-canonical-property"></a><span data-ttu-id="e2775-103">PidTagOriginalEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e2775-103">PidTagOriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="e2775-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2775-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2775-105">個人用アドレス帳にアドレス帳やその他の書き込み可能なアドレス帳からコピーしたエントリの元のエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e2775-105">Contains the original entry identifier for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2775-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e2775-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2775-107">PR_ORIGINAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e2775-107">PR_ORIGINAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="e2775-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e2775-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2775-109">0x3A12</span><span class="sxs-lookup"><span data-stu-id="e2775-109">0x3A12</span></span>  <br/> |
|<span data-ttu-id="e2775-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e2775-110">Data type:</span></span>  <br/> |<span data-ttu-id="e2775-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e2775-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e2775-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e2775-112">Area:</span></span>  <br/> |<span data-ttu-id="e2775-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="e2775-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2775-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e2775-114">Remarks</span></span>

<span data-ttu-id="e2775-115">このプロパティは、コピーしたエントリの元のソースに関する情報を含むプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="e2775-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="e2775-116">Nonread レポートでは、このプロパティには、レポートを生成する元のメッセージの受信者のエントリ id のコピーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e2775-116">For a nonread report, this property contains a copy of the entry identifier of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="e2775-117">元の受信者、配布リストの一部である場合は、レポートの配布リストのエントリの識別子が保持されます。</span><span class="sxs-lookup"><span data-stu-id="e2775-117">When the original recipient is part of a distribution list, the entry identifier of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e2775-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e2775-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2775-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e2775-119">Protocol specifications</span></span>

<span data-ttu-id="e2775-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2775-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2775-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e2775-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2775-122">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2775-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2775-123">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2775-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="e2775-124">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2775-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2775-125">サーバーとクライアントの間のメッセージングのオブジェクト データの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="e2775-125">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2775-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e2775-126">Header files</span></span>

<span data-ttu-id="e2775-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2775-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2775-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e2775-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="e2775-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e2775-129">Mapitags.h</span></span>
  
> <span data-ttu-id="e2775-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e2775-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2775-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2775-131">See also</span></span>



[<span data-ttu-id="e2775-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e2775-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2775-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e2775-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2775-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e2775-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2775-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e2775-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

