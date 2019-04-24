---
title: PidTagFormVersion 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormVersion
api_type:
- HeaderDef
ms.assetid: f2220060-65ea-4969-88d7-8348bd5aa242
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ec806ed3ab871d6a36778b0898b2977628ccdcec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316206"
---
# <a name="pidtagformversion-canonical-property"></a><span data-ttu-id="4402b-103">PidTagFormVersion 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4402b-103">PidTagFormVersion Canonical Property</span></span>

  
  
<span data-ttu-id="4402b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4402b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4402b-105">フォームのバージョンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4402b-105">Contains the version of a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4402b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4402b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4402b-107">PR_FORM_VERSION、PR_FORM_VERSION_A、PR_FORM_VERSION_W</span><span class="sxs-lookup"><span data-stu-id="4402b-107">PR_FORM_VERSION, PR_FORM_VERSION_A, PR_FORM_VERSION_W</span></span>  <br/> |
|<span data-ttu-id="4402b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4402b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4402b-109">0x3301</span><span class="sxs-lookup"><span data-stu-id="4402b-109">0x3301</span></span>  <br/> |
|<span data-ttu-id="4402b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4402b-110">Data type:</span></span>  <br/> |<span data-ttu-id="4402b-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4402b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4402b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="4402b-112">Area:</span></span>  <br/> |<span data-ttu-id="4402b-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="4402b-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4402b-114">解説</span><span class="sxs-lookup"><span data-stu-id="4402b-114">Remarks</span></span>

<span data-ttu-id="4402b-115">これらのプロパティは、フォームに対して現在有効なデザインバージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="4402b-115">These properties indicate what design version is currently in effect for the form.</span></span> <span data-ttu-id="4402b-116">バージョンはフォームのデザイナーによって定義され、管理されており、すべての MAPI コンポーネントのバージョンに関連しているとは限りません。</span><span class="sxs-lookup"><span data-stu-id="4402b-116">The version is defined and maintained by the form's designer and is not necessarily related to any MAPI component version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4402b-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4402b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4402b-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="4402b-118">Header files</span></span>

<span data-ttu-id="4402b-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4402b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4402b-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4402b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4402b-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="4402b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4402b-122">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4402b-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4402b-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="4402b-123">See also</span></span>



[<span data-ttu-id="4402b-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="4402b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4402b-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4402b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4402b-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4402b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4402b-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4402b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

