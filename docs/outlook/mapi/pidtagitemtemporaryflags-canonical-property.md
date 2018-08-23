---
title: PidTagItemTemporaryflags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagItemTemporaryflags
api_type:
- HeaderDef
ms.assetid: 8066de8e-2b77-4bac-8df3-e64b03ee42b9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e8bed42ee44e48540df52e806c7113e02b60cd07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593635"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a><span data-ttu-id="04933-103">PidTagItemTemporaryflags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="04933-103">PidTagItemTemporaryflags Canonical Property</span></span>

  
  
<span data-ttu-id="04933-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04933-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04933-105">メッセージを読み取るには、されたが、既読としてマークされていないことを示すフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="04933-105">Contains a flag that indicates that a message has been read, but not marked as read.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="04933-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="04933-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="04933-107">PR_ITEM_TMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="04933-107">PR_ITEM_TMPFLAGS</span></span>  <br/> |
|<span data-ttu-id="04933-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="04933-108">Identifier:</span></span>  <br/> |<span data-ttu-id="04933-109">0x1097</span><span class="sxs-lookup"><span data-stu-id="04933-109">0x1097</span></span>  <br/> |
|<span data-ttu-id="04933-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="04933-110">Data type:</span></span>  <br/> |<span data-ttu-id="04933-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="04933-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="04933-112">領域:</span><span class="sxs-lookup"><span data-stu-id="04933-112">Area:</span></span>  <br/> |<span data-ttu-id="04933-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="04933-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04933-114">注釈</span><span class="sxs-lookup"><span data-stu-id="04933-114">Remarks</span></span>

<span data-ttu-id="04933-115">このプロパティは、どのメッセージが実際に開封して、フォルダーからそれらを削除することがなく読まれてを追跡する Outlook の未読メ ッ セージ] 検索フォルダーに使用します。</span><span class="sxs-lookup"><span data-stu-id="04933-115">This property is used in Outlook's Unread Messages search folder to keep track of which messages have been read without actually marking them as read, which would remove them from the folder.</span></span> <span data-ttu-id="04933-116">このプロパティは削除、変更を表示し、項目としてマークされている場合にお読みください。</span><span class="sxs-lookup"><span data-stu-id="04933-116">When the view changes this property is removed and the item is marked as read.</span></span> <span data-ttu-id="04933-117">このプロパティは、Exchange Server に同期されません。</span><span class="sxs-lookup"><span data-stu-id="04933-117">This property will not synchronize to the Exchange Server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="04933-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="04933-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="04933-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="04933-119">Protocol specifications</span></span>

<span data-ttu-id="04933-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04933-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04933-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="04933-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="04933-122">[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04933-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04933-123">フォルダーの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="04933-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="04933-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="04933-124">Header files</span></span>

<span data-ttu-id="04933-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="04933-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="04933-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="04933-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="04933-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="04933-127">Mapitags.h</span></span>
  
> <span data-ttu-id="04933-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="04933-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04933-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="04933-129">See also</span></span>



[<span data-ttu-id="04933-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="04933-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="04933-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="04933-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="04933-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="04933-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="04933-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="04933-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

