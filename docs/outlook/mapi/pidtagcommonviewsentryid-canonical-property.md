---
title: PidTagCommonViewsEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCommonViewsEntryId
api_type:
- HeaderDef
ms.assetid: cd9e6a46-2112-4663-891e-5e57b22c0950
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7449e59227b147d34c2329175d0251dbb9c427b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581343"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a><span data-ttu-id="fe3ea-103">PidTagCommonViewsEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fe3ea-103">PidTagCommonViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="fe3ea-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe3ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe3ea-105">定義済みの一般的なビュー フォルダーのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fe3ea-105">Contains the entry identifier of the predefined common view folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe3ea-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fe3ea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe3ea-107">PR_COMMON_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fe3ea-107">PR_COMMON_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="fe3ea-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fe3ea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fe3ea-109">0x35E6</span><span class="sxs-lookup"><span data-stu-id="fe3ea-109">0x35E6</span></span>  <br/> |
|<span data-ttu-id="fe3ea-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fe3ea-110">Data type:</span></span>  <br/> |<span data-ttu-id="fe3ea-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fe3ea-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fe3ea-112">領域:</span><span class="sxs-lookup"><span data-stu-id="fe3ea-112">Area:</span></span>  <br/> |<span data-ttu-id="fe3ea-113">Outlook アプリケーション</span><span class="sxs-lookup"><span data-stu-id="fe3ea-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe3ea-114">注釈</span><span class="sxs-lookup"><span data-stu-id="fe3ea-114">Remarks</span></span>

<span data-ttu-id="fe3ea-115">共通のフォルダー ビューにはには、フォルダーのビューには、メッセージングのユーザーによって定義された指定子が含まれているときに標準のビューの指定子の定義済みセットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fe3ea-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="fe3ea-116">表示指定子が多く、各メッセージとして格納されているこれらのフォルダーは、個人間メッセージ (IPM) の階層構造で表示されていないを保持できます。</span><span class="sxs-lookup"><span data-stu-id="fe3ea-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="fe3ea-117">指定子のセットの 2 つをマージして両方使用できるようにするクライアント アプリケーションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="fe3ea-117">A client application can choose to merge the two sets of specifiers and make them both available.</span></span> 
  
<span data-ttu-id="fe3ea-118">ビューの詳細については、[フォルダーの表示](mapi-view-folders.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe3ea-118">For more information on views, see [View Folders](mapi-view-folders.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fe3ea-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fe3ea-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fe3ea-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fe3ea-120">Header files</span></span>

<span data-ttu-id="fe3ea-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe3ea-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe3ea-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fe3ea-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="fe3ea-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fe3ea-123">Mapitags.h</span></span>
  
> <span data-ttu-id="fe3ea-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fe3ea-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe3ea-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe3ea-125">See also</span></span>



[<span data-ttu-id="fe3ea-126">PidTagDefaultViewEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fe3ea-126">PidTagDefaultViewEntryId Canonical Property</span></span>](pidtagdefaultviewentryid-canonical-property.md)
  
[<span data-ttu-id="fe3ea-127">PidTagViewsEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fe3ea-127">PidTagViewsEntryId Canonical Property</span></span>](pidtagviewsentryid-canonical-property.md)


[<span data-ttu-id="fe3ea-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fe3ea-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe3ea-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fe3ea-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe3ea-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fe3ea-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe3ea-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fe3ea-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

