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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400219"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a><span data-ttu-id="6b055-103">PidLidCleanGlobalObjectId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b055-103">PidLidCleanGlobalObjectId Canonical Property</span></span>

  
  
<span data-ttu-id="6b055-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b055-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b055-105">クリーンなグローバル**オブジェクト Id**を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b055-105">Specifies the clean global **ObjectID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6b055-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6b055-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6b055-107">dispidCleanGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="6b055-107">dispidCleanGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="6b055-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6b055-108">Property set:</span></span>  <br/> |<span data-ttu-id="6b055-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="6b055-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="6b055-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6b055-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6b055-111">0x00000023</span><span class="sxs-lookup"><span data-stu-id="6b055-111">0x00000023</span></span>  <br/> |
|<span data-ttu-id="6b055-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6b055-112">Data type:</span></span>  <br/> |<span data-ttu-id="6b055-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6b055-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6b055-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="6b055-114">Area:</span></span>  <br/> |<span data-ttu-id="6b055-115">会議</span><span class="sxs-lookup"><span data-stu-id="6b055-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b055-116">備考</span><span class="sxs-lookup"><span data-stu-id="6b055-116">Remarks</span></span>

<span data-ttu-id="6b055-117">このプロパティの形式は、 **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) のものと同じです。</span><span class="sxs-lookup"><span data-stu-id="6b055-117">The format of this property is the same as that of **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span></span> <span data-ttu-id="6b055-118">このプロパティの値は、 **LID_GLOBAL_OBJID**YH、YL、M 以外の値に等しいである必要があり、D のフィールドは 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b055-118">The value of this property must be equal to the value of **LID_GLOBAL_OBJID**, except the YH, YL, M, and D fields must be zero.</span></span> <span data-ttu-id="6b055-119">自体には、定期的な系列だけでなく、(孤立したインスタンスを含む)、定期的な系列のインスタンスを参照するすべてのオブジェクトには、このプロパティに対して同じ値があります。</span><span class="sxs-lookup"><span data-stu-id="6b055-119">All objects that refer to an Instance of a recurring series (including an orphan instance), as well as the recurring series itself, will have the same value for this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6b055-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6b055-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6b055-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6b055-121">Protocol specifications</span></span>

<span data-ttu-id="6b055-122">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b055-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b055-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6b055-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6b055-124">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b055-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b055-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b055-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6b055-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6b055-126">Header files</span></span>

<span data-ttu-id="6b055-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b055-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6b055-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6b055-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6b055-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b055-129">See also</span></span>



[<span data-ttu-id="6b055-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b055-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6b055-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b055-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6b055-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6b055-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6b055-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6b055-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

