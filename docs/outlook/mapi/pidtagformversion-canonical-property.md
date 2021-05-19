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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ec806ed3ab871d6a36778b0898b2977628ccdcec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409868"
---
# <a name="pidtagformversion-canonical-property"></a><span data-ttu-id="85843-103">PidTagFormVersion 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="85843-103">PidTagFormVersion Canonical Property</span></span>

  
  
<span data-ttu-id="85843-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85843-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85843-105">フォームのバージョンが含まれる。</span><span class="sxs-lookup"><span data-stu-id="85843-105">Contains the version of a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85843-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="85843-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="85843-107">PR_FORM_VERSION、PR_FORM_VERSION_A、PR_FORM_VERSION_W</span><span class="sxs-lookup"><span data-stu-id="85843-107">PR_FORM_VERSION, PR_FORM_VERSION_A, PR_FORM_VERSION_W</span></span>  <br/> |
|<span data-ttu-id="85843-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="85843-108">Identifier:</span></span>  <br/> |<span data-ttu-id="85843-109">0x3301</span><span class="sxs-lookup"><span data-stu-id="85843-109">0x3301</span></span>  <br/> |
|<span data-ttu-id="85843-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="85843-110">Data type:</span></span>  <br/> |<span data-ttu-id="85843-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="85843-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="85843-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="85843-112">Area:</span></span>  <br/> |<span data-ttu-id="85843-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="85843-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85843-114">注釈</span><span class="sxs-lookup"><span data-stu-id="85843-114">Remarks</span></span>

<span data-ttu-id="85843-115">これらのプロパティは、フォームに対して現在有効なデザイン バージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="85843-115">These properties indicate what design version is currently in effect for the form.</span></span> <span data-ttu-id="85843-116">バージョンはフォームのデザイナーによって定義および管理され、必ずしも MAPI コンポーネントのバージョンに関連する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85843-116">The version is defined and maintained by the form's designer and is not necessarily related to any MAPI component version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="85843-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="85843-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="85843-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="85843-118">Header files</span></span>

<span data-ttu-id="85843-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="85843-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="85843-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="85843-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="85843-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="85843-121">Mapitags.h</span></span>
  
> <span data-ttu-id="85843-122">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="85843-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="85843-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="85843-123">See also</span></span>



[<span data-ttu-id="85843-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="85843-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="85843-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="85843-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="85843-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="85843-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="85843-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="85843-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

