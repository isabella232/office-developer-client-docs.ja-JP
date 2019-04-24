---
title: PidLidCleanGlobalObjectId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c48fa333d407492b69da5287fa75c565bfd10e11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349218"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a><span data-ttu-id="47eca-103">PidLidCleanGlobalObjectId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="47eca-103">PidLidCleanGlobalObjectId Canonical Property</span></span>

  
  
<span data-ttu-id="47eca-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47eca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47eca-105">クリーンなグローバル**ObjectID**を指定します。</span><span class="sxs-lookup"><span data-stu-id="47eca-105">Specifies the clean global **ObjectID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47eca-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="47eca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47eca-107">dispidCleanGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="47eca-107">dispidCleanGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="47eca-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="47eca-108">Property set:</span></span>  <br/> |<span data-ttu-id="47eca-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="47eca-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="47eca-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="47eca-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="47eca-111">0x00000023</span><span class="sxs-lookup"><span data-stu-id="47eca-111">0x00000023</span></span>  <br/> |
|<span data-ttu-id="47eca-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="47eca-112">Data type:</span></span>  <br/> |<span data-ttu-id="47eca-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="47eca-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="47eca-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="47eca-114">Area:</span></span>  <br/> |<span data-ttu-id="47eca-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="47eca-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47eca-116">解説</span><span class="sxs-lookup"><span data-stu-id="47eca-116">Remarks</span></span>

<span data-ttu-id="47eca-117">このプロパティの形式は、 **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) の形式と同じです。</span><span class="sxs-lookup"><span data-stu-id="47eca-117">The format of this property is the same as that of **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span></span> <span data-ttu-id="47eca-118">このプロパティの値は、 **LID_GLOBAL_OBJID**の値と等しくなければなりません。ただし、yh、YL、M、D の各フィールドは0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="47eca-118">The value of this property must be equal to the value of **LID_GLOBAL_OBJID**, except the YH, YL, M, and D fields must be zero.</span></span> <span data-ttu-id="47eca-119">定期的なアイテム (孤立インスタンスを含む) のインスタンスを参照するすべてのオブジェクトは、このプロパティの値が同じになります。</span><span class="sxs-lookup"><span data-stu-id="47eca-119">All objects that refer to an Instance of a recurring series (including an orphan instance), as well as the recurring series itself, will have the same value for this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="47eca-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="47eca-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47eca-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="47eca-121">Protocol specifications</span></span>

<span data-ttu-id="47eca-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47eca-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47eca-123">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="47eca-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="47eca-124">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47eca-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47eca-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="47eca-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47eca-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="47eca-126">Header files</span></span>

<span data-ttu-id="47eca-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47eca-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="47eca-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="47eca-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47eca-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="47eca-129">See also</span></span>



[<span data-ttu-id="47eca-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="47eca-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47eca-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="47eca-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47eca-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="47eca-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47eca-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="47eca-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

