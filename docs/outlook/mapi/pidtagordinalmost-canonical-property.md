---
title: PidTagOrdinalMost 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOrdinalMost
api_type:
- COM
ms.assetid: c18de08b-8c28-4cdf-bd2e-b9c650cd6da6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c2cf784ff9a86c9e2a2ce1a25b3c4b8ff7d8b75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803040"
---
# <a name="pidtagordinalmost-canonical-property"></a><span data-ttu-id="06db4-103">PidTagOrdinalMost 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="06db4-103">PidTagOrdinalMost Canonical Property</span></span>

  
  
<span data-ttu-id="06db4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06db4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06db4-105">負の値は、フォルダー内のすべてのタスクの**dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) プロパティの値以下の正の整数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="06db4-105">Contains a positive number whose negative is less than or equal to the value of the **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) property of all tasks in the folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06db4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="06db4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06db4-107">PR_ORDINAL_MOST</span><span class="sxs-lookup"><span data-stu-id="06db4-107">PR_ORDINAL_MOST</span></span>  <br/> |
|<span data-ttu-id="06db4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="06db4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06db4-109">0x36E2</span><span class="sxs-lookup"><span data-stu-id="06db4-109">0x36E2</span></span>  <br/> |
|<span data-ttu-id="06db4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="06db4-110">Data type:</span></span>  <br/> |<span data-ttu-id="06db4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="06db4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="06db4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="06db4-112">Area:</span></span>  <br/> |<span data-ttu-id="06db4-113">タスク</span><span class="sxs-lookup"><span data-stu-id="06db4-113">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06db4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="06db4-114">Remarks</span></span>

<span data-ttu-id="06db4-115">条件に違反する方法で、フォルダー内の任意のタスク オブジェクトの**dispidTaskOrdinal**プロパティが変更されるたびに、この状態を維持するためにこのプロパティを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06db4-115">This property must be updated to maintain this condition whenever the **dispidTaskOrdinal** property of any task object in the folder changes in a way that would violate the condition.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="06db4-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="06db4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="06db4-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="06db4-117">Protocol specifications</span></span>

<span data-ttu-id="06db4-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06db4-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06db4-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="06db4-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="06db4-120">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06db4-120">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06db4-121">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="06db4-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
  
### <a name="header-files"></a><span data-ttu-id="06db4-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="06db4-122">Header files</span></span>

<span data-ttu-id="06db4-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06db4-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="06db4-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="06db4-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="06db4-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="06db4-125">Mapitags.h</span></span>
  
> <span data-ttu-id="06db4-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="06db4-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06db4-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="06db4-127">See also</span></span>



[<span data-ttu-id="06db4-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="06db4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06db4-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="06db4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06db4-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="06db4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06db4-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="06db4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

