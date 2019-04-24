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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360558"
---
# <a name="pidlidverbresponse-canonical-property"></a><span data-ttu-id="9396e-103">PidLidVerbResponse 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9396e-103">PidLidVerbResponse Canonical Property</span></span>

  
  
<span data-ttu-id="9396e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9396e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9396e-105">回答者が選択した投票オプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="9396e-105">Specifies the voting option that a respondent selected.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9396e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9396e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9396e-107">dispidVerbResponse</span><span class="sxs-lookup"><span data-stu-id="9396e-107">dispidVerbResponse</span></span>  <br/> |
|<span data-ttu-id="9396e-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="9396e-108">Property set:</span></span>  <br/> |<span data-ttu-id="9396e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="9396e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9396e-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9396e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9396e-111">0x00008524</span><span class="sxs-lookup"><span data-stu-id="9396e-111">0x00008524</span></span>  <br/> |
|<span data-ttu-id="9396e-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9396e-112">Data type:</span></span>  <br/> |<span data-ttu-id="9396e-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9396e-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9396e-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="9396e-114">Area:</span></span>  <br/> |<span data-ttu-id="9396e-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="9396e-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9396e-116">解説</span><span class="sxs-lookup"><span data-stu-id="9396e-116">Remarks</span></span>

<span data-ttu-id="9396e-117">このプロパティは、通常、回答者が投票を行う**dispidVerbStream** ([PidLidVerbStream](pidlidverbstream-canonical-property.md)) プロパティに含まれている区切られた値の1つに設定されます。</span><span class="sxs-lookup"><span data-stu-id="9396e-117">This property is usually set to one of the delimited values that are contained in the **dispidVerbStream** ([PidLidVerbStream](pidlidverbstream-canonical-property.md)) property on which the respondent votes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9396e-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9396e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9396e-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9396e-119">Protocol specifications</span></span>

<span data-ttu-id="9396e-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9396e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9396e-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9396e-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9396e-122">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9396e-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9396e-123">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9396e-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9396e-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9396e-124">Header files</span></span>

<span data-ttu-id="9396e-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9396e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9396e-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9396e-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9396e-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="9396e-127">See also</span></span>



[<span data-ttu-id="9396e-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9396e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9396e-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9396e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9396e-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9396e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9396e-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9396e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

