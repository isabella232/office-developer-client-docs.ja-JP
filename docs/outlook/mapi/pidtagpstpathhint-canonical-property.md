---
title: PidTagPstPathHint 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6415ddcec2823192967b8869b46b22b58b08ba5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286358"
---
# <a name="pidtagpstpathhint-canonical-property"></a><span data-ttu-id="292d4-103">PidTagPstPathHint 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="292d4-103">PidTagPstPathHint Canonical Property</span></span>

  
  
<span data-ttu-id="292d4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="292d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="292d4-105">ユーザーが編集できる個人用ストレージテーブル (.pst ファイル) 名を [構成] ダイアログボックスで提供します。</span><span class="sxs-lookup"><span data-stu-id="292d4-105">Provides the personal storage table (.pst file) name, which the user can edit, for the configuration dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="292d4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="292d4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="292d4-107">PR_PST_PATH_HINT、PR_PST_PATH_HINT_A、PR_PST_PATH_HINT_W</span><span class="sxs-lookup"><span data-stu-id="292d4-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span></span>  <br/> |
|<span data-ttu-id="292d4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="292d4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="292d4-109">0x6771</span><span class="sxs-lookup"><span data-stu-id="292d4-109">0x6771</span></span>  <br/> |
|<span data-ttu-id="292d4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="292d4-110">Data type:</span></span>  <br/> |<span data-ttu-id="292d4-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="292d4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="292d4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="292d4-112">Area:</span></span>  <br/> |<span data-ttu-id="292d4-113">パーソナルストレージテーブル (.pst) 内部</span><span class="sxs-lookup"><span data-stu-id="292d4-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="292d4-114">解説</span><span class="sxs-lookup"><span data-stu-id="292d4-114">Remarks</span></span>

<span data-ttu-id="292d4-115">**PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) プロパティが代わりに使用されている場合は、[構成] ダイアログボックスが開きますが、ユーザーはパスやその他の多くのプロパティを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="292d4-115">If the **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) property is used instead, the configuration dialog box will open, but the user will not be allowed to edit the path and many other properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="292d4-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="292d4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="292d4-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="292d4-117">Protocol specifications</span></span>

<span data-ttu-id="292d4-118">[[OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="292d4-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="292d4-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="292d4-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="292d4-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="292d4-120">Header files</span></span>

<span data-ttu-id="292d4-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="292d4-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="292d4-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="292d4-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="292d4-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="292d4-123">Mapitags.h</span></span>
  
> <span data-ttu-id="292d4-124">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="292d4-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="292d4-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="292d4-125">See also</span></span>



[<span data-ttu-id="292d4-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="292d4-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="292d4-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="292d4-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="292d4-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="292d4-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="292d4-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="292d4-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

