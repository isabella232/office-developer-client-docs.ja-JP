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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6415ddcec2823192967b8869b46b22b58b08ba5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437309"
---
# <a name="pidtagpstpathhint-canonical-property"></a><span data-ttu-id="54eb5-103">PidTagPstPathHint 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="54eb5-103">PidTagPstPathHint Canonical Property</span></span>

  
  
<span data-ttu-id="54eb5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54eb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54eb5-105">構成ダイアログ ボックスに対して、ユーザーが編集できる個人用ストレージ テーブル (.pst ファイル) 名を指定します。</span><span class="sxs-lookup"><span data-stu-id="54eb5-105">Provides the personal storage table (.pst file) name, which the user can edit, for the configuration dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54eb5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="54eb5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54eb5-107">PR_PST_PATH_HINT、PR_PST_PATH_HINT_A、PR_PST_PATH_HINT_W</span><span class="sxs-lookup"><span data-stu-id="54eb5-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span></span>  <br/> |
|<span data-ttu-id="54eb5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="54eb5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="54eb5-109">0x6771</span><span class="sxs-lookup"><span data-stu-id="54eb5-109">0x6771</span></span>  <br/> |
|<span data-ttu-id="54eb5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="54eb5-110">Data type:</span></span>  <br/> |<span data-ttu-id="54eb5-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="54eb5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="54eb5-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="54eb5-112">Area:</span></span>  <br/> |<span data-ttu-id="54eb5-113">個人用ストレージ テーブル (.pst) 内部</span><span class="sxs-lookup"><span data-stu-id="54eb5-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54eb5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="54eb5-114">Remarks</span></span>

<span data-ttu-id="54eb5-115">代わりに **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) プロパティを使用すると、構成ダイアログ ボックスが開きますが、ユーザーはパスや他の多くのプロパティを編集できません。</span><span class="sxs-lookup"><span data-stu-id="54eb5-115">If the **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) property is used instead, the configuration dialog box will open, but the user will not be allowed to edit the path and many other properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="54eb5-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="54eb5-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="54eb5-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="54eb5-117">Protocol specifications</span></span>

<span data-ttu-id="54eb5-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="54eb5-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="54eb5-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="54eb5-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="54eb5-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="54eb5-120">Header files</span></span>

<span data-ttu-id="54eb5-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54eb5-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="54eb5-122">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="54eb5-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="54eb5-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="54eb5-123">Mapitags.h</span></span>
  
> <span data-ttu-id="54eb5-124">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="54eb5-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54eb5-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="54eb5-125">See also</span></span>



[<span data-ttu-id="54eb5-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="54eb5-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54eb5-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="54eb5-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54eb5-128">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="54eb5-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54eb5-129">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="54eb5-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

