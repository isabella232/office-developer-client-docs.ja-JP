---
title: PidTagPstPathHint の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 295b20ebc0c41104a8b1c8e46e2064c3ef32f99e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803240"
---
# <a name="pidtagpstpathhint-canonical-property"></a><span data-ttu-id="ed124-103">PidTagPstPathHint の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ed124-103">PidTagPstPathHint Canonical Property</span></span>

  
  
<span data-ttu-id="ed124-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed124-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed124-105">構成] ダイアログ ボックスには、ユーザーが編集できる、個人用領域 (.pst ファイル) のテーブル名を提供します。</span><span class="sxs-lookup"><span data-stu-id="ed124-105">Provides the personal storage table (.pst file) name, which the user can edit, for the configuration dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed124-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="ed124-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed124-107">PR_PST_PATH_HINT、PR_PST_PATH_HINT_A、PR_PST_PATH_HINT_W</span><span class="sxs-lookup"><span data-stu-id="ed124-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span></span>  <br/> |
|<span data-ttu-id="ed124-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ed124-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed124-109">0x6771</span><span class="sxs-lookup"><span data-stu-id="ed124-109">0x6771</span></span>  <br/> |
|<span data-ttu-id="ed124-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="ed124-110">Data type:</span></span>  <br/> |<span data-ttu-id="ed124-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ed124-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ed124-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ed124-112">Area:</span></span>  <br/> |<span data-ttu-id="ed124-113">パーソナル ストレージ表 (.pst) 内部</span><span class="sxs-lookup"><span data-stu-id="ed124-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed124-114">備考</span><span class="sxs-lookup"><span data-stu-id="ed124-114">Remarks</span></span>

<span data-ttu-id="ed124-115">代わりに**PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) プロパティを使用する場合、[構成] ダイアログ ボックスが開きが、ユーザーは、パスとその他の多くのプロパティを編集するのには使用できません。</span><span class="sxs-lookup"><span data-stu-id="ed124-115">If the **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) property is used instead, the configuration dialog box will open, but the user will not be allowed to edit the path and many other properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ed124-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ed124-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ed124-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ed124-117">Protocol specifications</span></span>

<span data-ttu-id="ed124-118">[MS OXPROPS]</span><span class="sxs-lookup"><span data-stu-id="ed124-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="ed124-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ed124-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed124-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ed124-120">Header files</span></span>

<span data-ttu-id="ed124-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed124-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed124-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ed124-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed124-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ed124-123">Mapitags.h</span></span>
  
> <span data-ttu-id="ed124-124">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ed124-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed124-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed124-125">See also</span></span>



[<span data-ttu-id="ed124-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed124-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed124-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed124-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed124-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="ed124-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed124-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="ed124-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

