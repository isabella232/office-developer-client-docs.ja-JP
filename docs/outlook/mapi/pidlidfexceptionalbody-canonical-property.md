---
title: PidLidFExceptionalBody 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalBody
api_type:
- COM
ms.assetid: 327516e8-ed3f-40fc-9604-03a70aecef5a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 93eb98aee19ea3f46a4e01e2c80150c3efe893a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327462"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a><span data-ttu-id="50d12-103">PidLidFExceptionalBody 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="50d12-103">PidLidFExceptionalBody Canonical Property</span></span>

  
  
<span data-ttu-id="50d12-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50d12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50d12-105">例外埋め込みメッセージ オブジェクトに、定期的な予定表オブジェクトとは異なる本文が含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="50d12-105">Indicates that the exception embedded message object has a body that differs from the recurring calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50d12-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="50d12-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50d12-107">dispidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="50d12-107">dispidFExceptionalBody</span></span>  <br/> |
|<span data-ttu-id="50d12-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="50d12-108">Property set:</span></span>  <br/> |<span data-ttu-id="50d12-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="50d12-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="50d12-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="50d12-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="50d12-111">0x00008206</span><span class="sxs-lookup"><span data-stu-id="50d12-111">0x00008206</span></span>  <br/> |
|<span data-ttu-id="50d12-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="50d12-112">Data type:</span></span>  <br/> |<span data-ttu-id="50d12-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="50d12-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="50d12-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="50d12-114">Area:</span></span>  <br/> |<span data-ttu-id="50d12-115">会議</span><span class="sxs-lookup"><span data-stu-id="50d12-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50d12-116">注釈</span><span class="sxs-lookup"><span data-stu-id="50d12-116">Remarks</span></span>

<span data-ttu-id="50d12-117">このプロパティの値が TRUE の場合、例外埋め込みメッセージ オブジェクトには本文が必要です。</span><span class="sxs-lookup"><span data-stu-id="50d12-117">If the value of this property is TRUE, then the exception embedded message object must have a body.</span></span> <span data-ttu-id="50d12-118">このプロパティの値が FALSE の場合、またはプロパティが存在しない場合は、クライアントまたはサーバーが定期的な予定表オブジェクトから本文を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50d12-118">If the value of this property is FALSE, or if the property does not exist, then a client or server must obtain the body from the recurring calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50d12-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="50d12-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="50d12-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="50d12-120">Protocol specifications</span></span>

<span data-ttu-id="50d12-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50d12-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50d12-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="50d12-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="50d12-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50d12-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50d12-124">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="50d12-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="50d12-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="50d12-125">Header files</span></span>

<span data-ttu-id="50d12-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50d12-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="50d12-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="50d12-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50d12-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="50d12-128">See also</span></span>



[<span data-ttu-id="50d12-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="50d12-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50d12-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="50d12-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50d12-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="50d12-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50d12-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="50d12-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

