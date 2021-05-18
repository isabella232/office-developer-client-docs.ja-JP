---
title: PidLidFExceptionalAttendees 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalAttendees
api_type:
- COM
ms.assetid: f1f489a3-e83a-4e96-bf9a-d98bc17d29f5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 544b5b5ac945eeedf787af0e311491da1f9d0217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327476"
---
# <a name="pidlidfexceptionalattendees-canonical-property"></a><span data-ttu-id="6b42c-103">PidLidFExceptionalAttendees 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b42c-103">PidLidFExceptionalAttendees Canonical Property</span></span>

  
  
<span data-ttu-id="6b42c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b42c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b42c-105">このプロパティが 1 つ以上の例外を持つ定期的な予定表オブジェクトであるかどうかを示し、少なくとも 1 つの例外埋め込みメッセージに少なくとも 1 つの RecipientRow が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6b42c-105">Indicates whether this property is a recurring calendar object with one or more exceptions, and at least one of the exception embedded messages has at least one RecipientRow.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6b42c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6b42c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6b42c-107">dispidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="6b42c-107">dispidFExceptionalAttendees</span></span>  <br/> |
|<span data-ttu-id="6b42c-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="6b42c-108">Property set:</span></span>  <br/> |<span data-ttu-id="6b42c-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="6b42c-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="6b42c-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6b42c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6b42c-111">0x0000822B</span><span class="sxs-lookup"><span data-stu-id="6b42c-111">0x0000822B</span></span>  <br/> |
|<span data-ttu-id="6b42c-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6b42c-112">Data type:</span></span>  <br/> |<span data-ttu-id="6b42c-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6b42c-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6b42c-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="6b42c-114">Area:</span></span>  <br/> |<span data-ttu-id="6b42c-115">会議</span><span class="sxs-lookup"><span data-stu-id="6b42c-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b42c-116">注釈</span><span class="sxs-lookup"><span data-stu-id="6b42c-116">Remarks</span></span>

<span data-ttu-id="6b42c-117">FALSE の値、またはこのプロパティがない場合は、calendar オブジェクトに例外がないか、例外の埋め込みメッセージに RecipientRows がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="6b42c-117">A value of FALSE, or the absence of this property, indicates that the calendar object either has no exceptions, or none of the exception embedded messages has RecipientRows.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6b42c-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6b42c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6b42c-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6b42c-119">Protocol specifications</span></span>

<span data-ttu-id="6b42c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b42c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b42c-121">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="6b42c-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6b42c-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b42c-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b42c-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b42c-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6b42c-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6b42c-124">Header files</span></span>

<span data-ttu-id="6b42c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b42c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="6b42c-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6b42c-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6b42c-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b42c-127">See also</span></span>



[<span data-ttu-id="6b42c-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="6b42c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6b42c-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b42c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6b42c-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="6b42c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6b42c-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="6b42c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

