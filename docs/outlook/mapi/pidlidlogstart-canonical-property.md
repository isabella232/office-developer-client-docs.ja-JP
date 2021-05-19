---
title: PidLidLogStart 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogStart
api_type:
- COM
ms.assetid: b8c0c871-51d8-4752-ad4b-607463a9f837
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dd5805cb0ee6b172506a532a513d06f57c583eee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337017"
---
# <a name="pidlidlogstart-canonical-property"></a><span data-ttu-id="25278-103">PidLidLogStart 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="25278-103">PidLidLogStart Canonical Property</span></span>

  
  
<span data-ttu-id="25278-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25278-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25278-105">ジャーナル メッセージの開始日時を表します。</span><span class="sxs-lookup"><span data-stu-id="25278-105">Represents the start date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25278-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="25278-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25278-107">dispidLogStart</span><span class="sxs-lookup"><span data-stu-id="25278-107">dispidLogStart</span></span>  <br/> |
|<span data-ttu-id="25278-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="25278-108">Property set:</span></span>  <br/> |<span data-ttu-id="25278-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="25278-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="25278-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="25278-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="25278-111">0x00008706</span><span class="sxs-lookup"><span data-stu-id="25278-111">0x00008706</span></span>  <br/> |
|<span data-ttu-id="25278-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="25278-112">Data type:</span></span>  <br/> |<span data-ttu-id="25278-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="25278-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="25278-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="25278-114">Area:</span></span>  <br/> |<span data-ttu-id="25278-115">ジャーナル</span><span class="sxs-lookup"><span data-stu-id="25278-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25278-116">注釈</span><span class="sxs-lookup"><span data-stu-id="25278-116">Remarks</span></span>

<span data-ttu-id="25278-117">アクティビティが開始された協定世界時 (UTC) の時刻は **、dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) プロパティと等しくする必要があります。</span><span class="sxs-lookup"><span data-stu-id="25278-117">The time in Coordinated Universal Time (UTC) when the activity began must be equal to the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="25278-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="25278-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25278-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="25278-119">Protocol specifications</span></span>

<span data-ttu-id="25278-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25278-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25278-121">プロパティ セットの定義と、関連するプロトコル仕様Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="25278-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="25278-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25278-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25278-123">ジャーナルに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="25278-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25278-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="25278-124">Header files</span></span>

<span data-ttu-id="25278-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25278-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="25278-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="25278-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25278-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="25278-127">See also</span></span>



[<span data-ttu-id="25278-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="25278-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25278-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="25278-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25278-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="25278-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25278-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="25278-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

