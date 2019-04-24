---
title: PidTagDefaultStore 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultStore
api_type:
- HeaderDef
ms.assetid: 6314d91c-4948-4fd1-bacc-932d4bb2c22f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0cbcc8185f6f46a1bfceb2dd6d0aaf9c5d7cab2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270106"
---
# <a name="pidtagdefaultstore-canonical-property"></a><span data-ttu-id="201a4-103">PidTagDefaultStore 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="201a4-103">PidTagDefaultStore Canonical Property</span></span>

  
  
<span data-ttu-id="201a4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="201a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="201a4-105">メッセージストアがメッセージストアテーブル内の既定のメッセージストアである場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="201a4-105">Contains TRUE if a message store is the default message store in the message store table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="201a4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="201a4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="201a4-107">PR_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="201a4-107">PR_DEFAULT_STORE</span></span>  <br/> |
|<span data-ttu-id="201a4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="201a4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="201a4-109">0x3400</span><span class="sxs-lookup"><span data-stu-id="201a4-109">0x3400</span></span>  <br/> |
|<span data-ttu-id="201a4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="201a4-110">Data type:</span></span>  <br/> |<span data-ttu-id="201a4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="201a4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="201a4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="201a4-112">Area:</span></span>  <br/> |<span data-ttu-id="201a4-113">MAPI メッセージストア</span><span class="sxs-lookup"><span data-stu-id="201a4-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="201a4-114">解説</span><span class="sxs-lookup"><span data-stu-id="201a4-114">Remarks</span></span>

<span data-ttu-id="201a4-115">このプロパティは、メッセージストアテーブルの列として表示されます。</span><span class="sxs-lookup"><span data-stu-id="201a4-115">This property appears as a column in the message store table.</span></span> <span data-ttu-id="201a4-116">値は**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) に基づいています。</span><span class="sxs-lookup"><span data-stu-id="201a4-116">The value is based on **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="201a4-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="201a4-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="201a4-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="201a4-118">Protocol specifications</span></span>

<span data-ttu-id="201a4-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="201a4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="201a4-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="201a4-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="201a4-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="201a4-121">Header files</span></span>

<span data-ttu-id="201a4-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="201a4-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="201a4-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="201a4-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="201a4-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="201a4-124">Mapitags.h</span></span>
  
> <span data-ttu-id="201a4-125">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="201a4-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="201a4-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="201a4-126">See also</span></span>



[<span data-ttu-id="201a4-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="201a4-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="201a4-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="201a4-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="201a4-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="201a4-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="201a4-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="201a4-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

