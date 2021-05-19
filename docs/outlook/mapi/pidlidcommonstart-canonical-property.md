---
title: PidLidCommonStart 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonStart
api_type:
- COM
ms.assetid: d999852d-ce98-4c3c-a772-87f5db4aa04e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ec7c213d7eec9ab0ef5766442e3de59a24811d37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345487"
---
# <a name="pidlidcommonstart-canonical-property"></a><span data-ttu-id="40afd-103">PidLidCommonStart 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="40afd-103">PidLidCommonStart Canonical Property</span></span>

  
  
<span data-ttu-id="40afd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40afd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40afd-105">メッセージの開始日時を表します。</span><span class="sxs-lookup"><span data-stu-id="40afd-105">Represents the start date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40afd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="40afd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40afd-107">dispidCommonStart</span><span class="sxs-lookup"><span data-stu-id="40afd-107">dispidCommonStart</span></span>  <br/> |
|<span data-ttu-id="40afd-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="40afd-108">Property set:</span></span>  <br/> |<span data-ttu-id="40afd-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="40afd-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="40afd-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="40afd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="40afd-111">0x00008516</span><span class="sxs-lookup"><span data-stu-id="40afd-111">0x00008516</span></span>  <br/> |
|<span data-ttu-id="40afd-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="40afd-112">Data type:</span></span>  <br/> |<span data-ttu-id="40afd-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="40afd-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="40afd-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="40afd-114">Area:</span></span>  <br/> |<span data-ttu-id="40afd-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="40afd-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40afd-116">注釈</span><span class="sxs-lookup"><span data-stu-id="40afd-116">Remarks</span></span>

<span data-ttu-id="40afd-117">このプロパティは、アイテムの開始時刻を示します。</span><span class="sxs-lookup"><span data-stu-id="40afd-117">This property indicates the start time for an item.</span></span> <span data-ttu-id="40afd-118">**dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) プロパティの値以下である必要があります。</span><span class="sxs-lookup"><span data-stu-id="40afd-118">It must be less than or equal to the value of the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="40afd-119">このプロパティの値は **、dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) プロパティと同等の協定世界時 (UTC) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="40afd-119">The value of this property must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="40afd-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="40afd-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40afd-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="40afd-121">Protocol specifications</span></span>

<span data-ttu-id="40afd-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40afd-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40afd-123">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="40afd-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="40afd-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40afd-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40afd-125">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="40afd-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="40afd-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40afd-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40afd-127">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="40afd-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40afd-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="40afd-128">Header files</span></span>

<span data-ttu-id="40afd-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40afd-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="40afd-130">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="40afd-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40afd-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="40afd-131">See also</span></span>



[<span data-ttu-id="40afd-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="40afd-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40afd-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="40afd-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40afd-134">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="40afd-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40afd-135">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="40afd-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

