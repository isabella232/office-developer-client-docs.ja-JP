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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 474df017954618e6411494454c1405445563b862
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386993"
---
# <a name="pidlidverbresponse-canonical-property"></a><span data-ttu-id="8bfb9-103">PidLidVerbResponse 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8bfb9-103">PidLidVerbResponse Canonical Property</span></span>

  
  
<span data-ttu-id="8bfb9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bfb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bfb9-105">回答者が選択した返信のオプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="8bfb9-105">Specifies the voting option that a respondent selected.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8bfb9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8bfb9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8bfb9-107">dispidVerbResponse</span><span class="sxs-lookup"><span data-stu-id="8bfb9-107">dispidVerbResponse</span></span>  <br/> |
|<span data-ttu-id="8bfb9-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8bfb9-108">Property set:</span></span>  <br/> |<span data-ttu-id="8bfb9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="8bfb9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="8bfb9-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8bfb9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8bfb9-111">0x00008524</span><span class="sxs-lookup"><span data-stu-id="8bfb9-111">0x00008524</span></span>  <br/> |
|<span data-ttu-id="8bfb9-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8bfb9-112">Data type:</span></span>  <br/> |<span data-ttu-id="8bfb9-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8bfb9-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8bfb9-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="8bfb9-114">Area:</span></span>  <br/> |<span data-ttu-id="8bfb9-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="8bfb9-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8bfb9-116">備考</span><span class="sxs-lookup"><span data-stu-id="8bfb9-116">Remarks</span></span>

<span data-ttu-id="8bfb9-117">このプロパティは通常、回答者が投票する**dispidVerbStream** ([PidLidVerbStream](pidlidverbstream-canonical-property.md)) のプロパティに含まれる区切られた値のいずれかに設定します。</span><span class="sxs-lookup"><span data-stu-id="8bfb9-117">This property is usually set to one of the delimited values that are contained in the **dispidVerbStream** ([PidLidVerbStream](pidlidverbstream-canonical-property.md)) property on which the respondent votes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8bfb9-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8bfb9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8bfb9-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8bfb9-119">Protocol specifications</span></span>

<span data-ttu-id="8bfb9-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bfb9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bfb9-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8bfb9-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8bfb9-122">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bfb9-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bfb9-123">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8bfb9-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8bfb9-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8bfb9-124">Header files</span></span>

<span data-ttu-id="8bfb9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8bfb9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8bfb9-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8bfb9-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8bfb9-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="8bfb9-127">See also</span></span>



[<span data-ttu-id="8bfb9-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8bfb9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8bfb9-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8bfb9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8bfb9-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8bfb9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8bfb9-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8bfb9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

