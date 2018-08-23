---
title: PidTagFormDesignerGuid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormDesignerGuid
api_type:
- HeaderDef
ms.assetid: 8d7f5789-610c-47f6-a109-5513d677ef60
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 30c8f31c104be52da2900eb81c7b7c29dfa55015
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586530"
---
# <a name="pidtagformdesignerguid-canonical-property"></a><span data-ttu-id="b0291-103">PidTagFormDesignerGuid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b0291-103">PidTagFormDesignerGuid Canonical Property</span></span>

  
  
<span data-ttu-id="b0291-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0291-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0291-105">フォームをデザインするために使用されるオブジェクトの一意の識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b0291-105">Contains the unique identifier for the object that is used to design a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0291-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b0291-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0291-107">PR_FORM_DESIGNER_GUID</span><span class="sxs-lookup"><span data-stu-id="b0291-107">PR_FORM_DESIGNER_GUID</span></span>  <br/> |
|<span data-ttu-id="b0291-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b0291-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b0291-109">0x3309</span><span class="sxs-lookup"><span data-stu-id="b0291-109">0x3309</span></span>  <br/> |
|<span data-ttu-id="b0291-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b0291-110">Data type:</span></span>  <br/> |<span data-ttu-id="b0291-111">PT_GUID</span><span class="sxs-lookup"><span data-stu-id="b0291-111">PT_GUID</span></span>  <br/> |
|<span data-ttu-id="b0291-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b0291-112">Area:</span></span>  <br/> |<span data-ttu-id="b0291-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="b0291-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0291-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b0291-114">Remarks</span></span>

<span data-ttu-id="b0291-115">通常、このプロパティは、フォームの作成に使用するデザイン プログラムのグローバル一意識別子 (GUID) を含みます。</span><span class="sxs-lookup"><span data-stu-id="b0291-115">This property usually contains the globally unique identifier (GUID) of the design program that is used to create the form.</span></span> <span data-ttu-id="b0291-116">このプロパティを空にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b0291-116">This property can be empty.</span></span> 
  
<span data-ttu-id="b0291-117">[MAPIUID](mapiuid.md)構造体には、一意の識別子の定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b0291-117">The [MAPIUID](mapiuid.md) structure contains the definition of the unique identifier.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b0291-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b0291-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b0291-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b0291-119">Header files</span></span>

<span data-ttu-id="b0291-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0291-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0291-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b0291-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="b0291-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b0291-122">Mapitags.h</span></span>
  
> <span data-ttu-id="b0291-123">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b0291-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0291-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="b0291-124">See also</span></span>



[<span data-ttu-id="b0291-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b0291-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0291-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b0291-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0291-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b0291-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0291-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b0291-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

