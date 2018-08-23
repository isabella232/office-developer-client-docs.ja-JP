---
title: PidTagOriginalSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSearchKey
api_type:
- COM
ms.assetid: ac5eb91d-31c9-459b-bb22-f4ccfc92d1db
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 69108529b13c8c5523f0ea92ef627c69a6722469
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594580"
---
# <a name="pidtagoriginalsearchkey-canonical-property"></a><span data-ttu-id="67e4f-103">PidTagOriginalSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="67e4f-103">PidTagOriginalSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="67e4f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67e4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67e4f-105">個人用アドレス帳にアドレス帳やその他の書き込み可能なアドレス帳からコピーしたエントリの元の検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="67e4f-105">Contains the original search key for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="67e4f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="67e4f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67e4f-107">PR_ORIGINAL_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="67e4f-107">PR_ORIGINAL_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="67e4f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="67e4f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67e4f-109">0x3A14</span><span class="sxs-lookup"><span data-stu-id="67e4f-109">0x3A14</span></span>  <br/> |
|<span data-ttu-id="67e4f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="67e4f-110">Data type:</span></span>  <br/> |<span data-ttu-id="67e4f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="67e4f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="67e4f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="67e4f-112">Area:</span></span>  <br/> |<span data-ttu-id="67e4f-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="67e4f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67e4f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="67e4f-114">Remarks</span></span>

<span data-ttu-id="67e4f-115">このプロパティは、コピーしたエントリの元のソースに関する情報を含むプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="67e4f-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="67e4f-116">Nonread レポートでは、このプロパティには、レポートを生成する元のメッセージ受信者の検索キーのコピーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="67e4f-116">For a nonread report, this property contains a copy of the search key of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="67e4f-117">元の受信者、配布リストの一部である場合は、レポートの配布リストの検索キーが保持されます。</span><span class="sxs-lookup"><span data-stu-id="67e4f-117">When the original recipient is part of a distribution list, the search key of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="67e4f-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="67e4f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="67e4f-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="67e4f-119">Protocol specifications</span></span>

<span data-ttu-id="67e4f-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67e4f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67e4f-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="67e4f-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="67e4f-122">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67e4f-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67e4f-123">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="67e4f-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="67e4f-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="67e4f-124">Header files</span></span>

<span data-ttu-id="67e4f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67e4f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="67e4f-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="67e4f-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="67e4f-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="67e4f-127">Mapitags.h</span></span>
  
> <span data-ttu-id="67e4f-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="67e4f-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67e4f-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="67e4f-129">See also</span></span>



[<span data-ttu-id="67e4f-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="67e4f-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67e4f-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="67e4f-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67e4f-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="67e4f-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67e4f-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="67e4f-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

