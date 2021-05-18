---
title: PidLidVerbResponse 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidVerbResponse
api_type:
- COM
ms.assetid: 6f3db5ac-f1cb-4c55-ab88-c126dd5f48ee
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 474df017954618e6411494454c1405445563b862
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360558"
---
# <a name="pidlidverbresponse-canonical-property"></a><span data-ttu-id="7a96b-103">PidLidVerbResponse 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a96b-103">PidLidVerbResponse Canonical Property</span></span>

  
  
<span data-ttu-id="7a96b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a96b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a96b-105">回答者が選択した投票オプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="7a96b-105">Specifies the voting option that a respondent selected.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7a96b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7a96b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7a96b-107">dispidVerbResponse</span><span class="sxs-lookup"><span data-stu-id="7a96b-107">dispidVerbResponse</span></span>  <br/> |
|<span data-ttu-id="7a96b-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="7a96b-108">Property set:</span></span>  <br/> |<span data-ttu-id="7a96b-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="7a96b-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="7a96b-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7a96b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7a96b-111">0x00008524</span><span class="sxs-lookup"><span data-stu-id="7a96b-111">0x00008524</span></span>  <br/> |
|<span data-ttu-id="7a96b-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7a96b-112">Data type:</span></span>  <br/> |<span data-ttu-id="7a96b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7a96b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7a96b-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="7a96b-114">Area:</span></span>  <br/> |<span data-ttu-id="7a96b-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="7a96b-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a96b-116">注釈</span><span class="sxs-lookup"><span data-stu-id="7a96b-116">Remarks</span></span>

<span data-ttu-id="7a96b-117">通常、このプロパティは、回答者が投票する **dispidVerbStream** ([PidLidVerbStream](pidlidverbstream-canonical-property.md)) プロパティに含まれる区切られた値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7a96b-117">This property is usually set to one of the delimited values that are contained in the **dispidVerbStream** ([PidLidVerbStream](pidlidverbstream-canonical-property.md)) property on which the respondent votes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7a96b-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7a96b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7a96b-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7a96b-119">Protocol specifications</span></span>

<span data-ttu-id="7a96b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a96b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a96b-121">プロパティ セットの定義と、関連するプロトコル仕様Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="7a96b-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7a96b-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a96b-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a96b-123">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7a96b-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7a96b-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7a96b-124">Header files</span></span>

<span data-ttu-id="7a96b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a96b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7a96b-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7a96b-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a96b-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a96b-127">See also</span></span>



[<span data-ttu-id="7a96b-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7a96b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7a96b-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a96b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7a96b-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7a96b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7a96b-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7a96b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

