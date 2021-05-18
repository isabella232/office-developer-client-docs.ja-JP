---
title: PidLidIsException 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsException
api_type:
- COM
ms.assetid: 802321fb-4261-4c3e-9de3-8b4f490dae13
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 18dfa8a5936902afe0272274f7a48d01b28f94f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315450"
---
# <a name="pidlidisexception-canonical-property"></a><span data-ttu-id="5ff56-103">PidLidIsException 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5ff56-103">PidLidIsException Canonical Property</span></span>

  
  
<span data-ttu-id="5ff56-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ff56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ff56-105">例外を表すオブジェクト (孤立したインスタンスを含む) を示します。</span><span class="sxs-lookup"><span data-stu-id="5ff56-105">Indicates that the object that represents an exception (including an orphan instance).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ff56-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5ff56-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ff56-107">LID_IS_EXCEPTION</span><span class="sxs-lookup"><span data-stu-id="5ff56-107">LID_IS_EXCEPTION</span></span>  <br/> |
|<span data-ttu-id="5ff56-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="5ff56-108">Property set:</span></span>  <br/> |<span data-ttu-id="5ff56-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="5ff56-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="5ff56-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5ff56-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5ff56-111">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="5ff56-111">0x0000000A</span></span>  <br/> |
|<span data-ttu-id="5ff56-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5ff56-112">Data type:</span></span>  <br/> |<span data-ttu-id="5ff56-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5ff56-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5ff56-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="5ff56-114">Area:</span></span>  <br/> |<span data-ttu-id="5ff56-115">会議</span><span class="sxs-lookup"><span data-stu-id="5ff56-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ff56-116">注釈</span><span class="sxs-lookup"><span data-stu-id="5ff56-116">Remarks</span></span>

<span data-ttu-id="5ff56-117">FALSE の値は、定期的な系列または 1 つのインスタンスを表すオブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="5ff56-117">A value of FALSE indicates that the object that represents a recurring series or a single instance.</span></span> <span data-ttu-id="5ff56-118">オブジェクトに対してこのプロパティがない場合は、例外埋め込みメッセージを除く FALSE の値を示します。これは TRUE の値を前提とします。</span><span class="sxs-lookup"><span data-stu-id="5ff56-118">The absence of this property for any object indicates a value of FALSE except for the exception embedded message, which assumes a value of TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5ff56-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5ff56-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5ff56-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5ff56-120">Protocol specifications</span></span>

<span data-ttu-id="5ff56-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ff56-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ff56-122">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="5ff56-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5ff56-123">[[MS-OXOCAL] ](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ff56-123">[[MS-OXOCAL] ](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ff56-124">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ff56-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5ff56-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5ff56-125">Header files</span></span>

<span data-ttu-id="5ff56-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ff56-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ff56-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5ff56-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ff56-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ff56-128">See also</span></span>



[<span data-ttu-id="5ff56-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5ff56-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ff56-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5ff56-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ff56-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5ff56-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ff56-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5ff56-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

