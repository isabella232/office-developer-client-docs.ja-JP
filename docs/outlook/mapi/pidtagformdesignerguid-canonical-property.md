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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b0e0847a3a9e21f080a852738ec8afbc98a2263f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412241"
---
# <a name="pidtagformdesignerguid-canonical-property"></a><span data-ttu-id="948c1-103">PidTagFormDesignerGuid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="948c1-103">PidTagFormDesignerGuid Canonical Property</span></span>

  
  
<span data-ttu-id="948c1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="948c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="948c1-105">フォームのデザインに使用されるオブジェクトの一意の識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="948c1-105">Contains the unique identifier for the object that is used to design a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="948c1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="948c1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="948c1-107">PR_FORM_DESIGNER_GUID</span><span class="sxs-lookup"><span data-stu-id="948c1-107">PR_FORM_DESIGNER_GUID</span></span>  <br/> |
|<span data-ttu-id="948c1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="948c1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="948c1-109">0x3309</span><span class="sxs-lookup"><span data-stu-id="948c1-109">0x3309</span></span>  <br/> |
|<span data-ttu-id="948c1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="948c1-110">Data type:</span></span>  <br/> |<span data-ttu-id="948c1-111">PT_GUID</span><span class="sxs-lookup"><span data-stu-id="948c1-111">PT_GUID</span></span>  <br/> |
|<span data-ttu-id="948c1-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="948c1-112">Area:</span></span>  <br/> |<span data-ttu-id="948c1-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="948c1-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="948c1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="948c1-114">Remarks</span></span>

<span data-ttu-id="948c1-115">通常、このプロパティには、フォームの作成に使用されるデザインプログラムのグローバル一意識別子 (GUID) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="948c1-115">This property usually contains the globally unique identifier (GUID) of the design program that is used to create the form.</span></span> <span data-ttu-id="948c1-116">このプロパティは空にすることができます。</span><span class="sxs-lookup"><span data-stu-id="948c1-116">This property can be empty.</span></span> 
  
<span data-ttu-id="948c1-117">[MAPIUID](mapiuid.md)構造体には、一意の識別子の定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="948c1-117">The [MAPIUID](mapiuid.md) structure contains the definition of the unique identifier.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="948c1-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="948c1-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="948c1-119">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="948c1-119">Header files</span></span>

<span data-ttu-id="948c1-120">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="948c1-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="948c1-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="948c1-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="948c1-122">Mapitags</span><span class="sxs-lookup"><span data-stu-id="948c1-122">Mapitags.h</span></span>
  
> <span data-ttu-id="948c1-123">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="948c1-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="948c1-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="948c1-124">See also</span></span>



[<span data-ttu-id="948c1-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="948c1-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="948c1-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="948c1-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="948c1-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="948c1-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="948c1-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="948c1-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

