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
ms.openlocfilehash: b0e0847a3a9e21f080a852738ec8afbc98a2263f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316234"
---
# <a name="pidtagformdesignerguid-canonical-property"></a><span data-ttu-id="1bfc3-103">PidTagFormDesignerGuid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1bfc3-103">PidTagFormDesignerGuid Canonical Property</span></span>

  
  
<span data-ttu-id="1bfc3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1bfc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1bfc3-105">フォームのデザインに使用されるオブジェクトの一意の識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="1bfc3-105">Contains the unique identifier for the object that is used to design a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1bfc3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1bfc3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1bfc3-107">PR_FORM_DESIGNER_GUID</span><span class="sxs-lookup"><span data-stu-id="1bfc3-107">PR_FORM_DESIGNER_GUID</span></span>  <br/> |
|<span data-ttu-id="1bfc3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1bfc3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1bfc3-109">0x3309</span><span class="sxs-lookup"><span data-stu-id="1bfc3-109">0x3309</span></span>  <br/> |
|<span data-ttu-id="1bfc3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1bfc3-110">Data type:</span></span>  <br/> |<span data-ttu-id="1bfc3-111">PT_GUID</span><span class="sxs-lookup"><span data-stu-id="1bfc3-111">PT_GUID</span></span>  <br/> |
|<span data-ttu-id="1bfc3-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1bfc3-112">Area:</span></span>  <br/> |<span data-ttu-id="1bfc3-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="1bfc3-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bfc3-114">解説</span><span class="sxs-lookup"><span data-stu-id="1bfc3-114">Remarks</span></span>

<span data-ttu-id="1bfc3-115">通常、このプロパティには、フォームの作成に使用されるデザインプログラムのグローバル一意識別子 (GUID) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1bfc3-115">This property usually contains the globally unique identifier (GUID) of the design program that is used to create the form.</span></span> <span data-ttu-id="1bfc3-116">このプロパティは空にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1bfc3-116">This property can be empty.</span></span> 
  
<span data-ttu-id="1bfc3-117">[MAPIUID](mapiuid.md)構造体には、一意の識別子の定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1bfc3-117">The [MAPIUID](mapiuid.md) structure contains the definition of the unique identifier.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1bfc3-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1bfc3-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1bfc3-119">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1bfc3-119">Header files</span></span>

<span data-ttu-id="1bfc3-120">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1bfc3-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="1bfc3-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1bfc3-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="1bfc3-122">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1bfc3-122">Mapitags.h</span></span>
  
> <span data-ttu-id="1bfc3-123">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1bfc3-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1bfc3-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="1bfc3-124">See also</span></span>



[<span data-ttu-id="1bfc3-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1bfc3-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1bfc3-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1bfc3-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1bfc3-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1bfc3-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1bfc3-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1bfc3-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

