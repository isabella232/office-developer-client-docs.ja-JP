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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c48fa333d407492b69da5287fa75c565bfd10e11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349218"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a><span data-ttu-id="56190-103">PidLidCleanGlobalObjectId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="56190-103">PidLidCleanGlobalObjectId Canonical Property</span></span>

  
  
<span data-ttu-id="56190-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56190-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56190-105">クリーン グローバル **ObjectID を指定します**。</span><span class="sxs-lookup"><span data-stu-id="56190-105">Specifies the clean global **ObjectID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="56190-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="56190-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="56190-107">dispidCleanGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="56190-107">dispidCleanGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="56190-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="56190-108">Property set:</span></span>  <br/> |<span data-ttu-id="56190-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="56190-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="56190-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="56190-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="56190-111">0x00000023</span><span class="sxs-lookup"><span data-stu-id="56190-111">0x00000023</span></span>  <br/> |
|<span data-ttu-id="56190-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="56190-112">Data type:</span></span>  <br/> |<span data-ttu-id="56190-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="56190-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="56190-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="56190-114">Area:</span></span>  <br/> |<span data-ttu-id="56190-115">会議</span><span class="sxs-lookup"><span data-stu-id="56190-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56190-116">注釈</span><span class="sxs-lookup"><span data-stu-id="56190-116">Remarks</span></span>

<span data-ttu-id="56190-117">このプロパティの形式は、 ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md) **)** LID_GLOBAL_OBJIDと同じです。</span><span class="sxs-lookup"><span data-stu-id="56190-117">The format of this property is the same as that of **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span></span> <span data-ttu-id="56190-118">このプロパティの値は、YH、YL、M、および D フィールド **を** 除き、LID_GLOBAL_OBJID の値と等しくする必要があります。</span><span class="sxs-lookup"><span data-stu-id="56190-118">The value of this property must be equal to the value of **LID_GLOBAL_OBJID**, except the YH, YL, M, and D fields must be zero.</span></span> <span data-ttu-id="56190-119">定期的な系列のインスタンス (孤立したインスタンスを含む) と定期的な系列自体を参照するオブジェクトはすべて、このプロパティの値が同じになります。</span><span class="sxs-lookup"><span data-stu-id="56190-119">All objects that refer to an Instance of a recurring series (including an orphan instance), as well as the recurring series itself, will have the same value for this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="56190-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="56190-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="56190-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="56190-121">Protocol specifications</span></span>

<span data-ttu-id="56190-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56190-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56190-123">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="56190-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="56190-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56190-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56190-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="56190-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="56190-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="56190-126">Header files</span></span>

<span data-ttu-id="56190-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56190-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="56190-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="56190-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56190-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="56190-129">See also</span></span>



[<span data-ttu-id="56190-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="56190-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56190-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="56190-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56190-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="56190-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56190-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="56190-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

