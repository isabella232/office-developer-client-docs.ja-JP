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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e22b8905901f16606614ac918896f3afe0093752
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437344"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a><span data-ttu-id="11c77-103">PidTagCommonViewsEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="11c77-103">PidTagCommonViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="11c77-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11c77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11c77-105">定義済みの共通ビュー フォルダーのエントリ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="11c77-105">Contains the entry identifier of the predefined common view folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11c77-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="11c77-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11c77-107">PR_COMMON_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="11c77-107">PR_COMMON_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="11c77-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="11c77-108">Identifier:</span></span>  <br/> |<span data-ttu-id="11c77-109">0x35E6</span><span class="sxs-lookup"><span data-stu-id="11c77-109">0x35E6</span></span>  <br/> |
|<span data-ttu-id="11c77-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="11c77-110">Data type:</span></span>  <br/> |<span data-ttu-id="11c77-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="11c77-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="11c77-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="11c77-112">Area:</span></span>  <br/> |<span data-ttu-id="11c77-113">Outlookアプリケーション</span><span class="sxs-lookup"><span data-stu-id="11c77-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11c77-114">注釈</span><span class="sxs-lookup"><span data-stu-id="11c77-114">Remarks</span></span>

<span data-ttu-id="11c77-115">共通ビュー フォルダーには定義済みの標準ビュー指定子のセットが含まれる一方、ビュー フォルダーにはメッセージング ユーザーによって定義された指定子が含まれる。</span><span class="sxs-lookup"><span data-stu-id="11c77-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="11c77-116">これらのフォルダーは、対人間メッセージ (IPM) 階層には表示されませんが、多くのビュー指定子を保持できます。各フォルダーはメッセージとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="11c77-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="11c77-117">クライアント アプリケーションは、2 つの指定子セットを結合し、両方を使用できます。</span><span class="sxs-lookup"><span data-stu-id="11c77-117">A client application can choose to merge the two sets of specifiers and make them both available.</span></span> 
  
<span data-ttu-id="11c77-118">ビューの詳細については、「フォルダーの表示」 [を参照してください](mapi-view-folders.md)。</span><span class="sxs-lookup"><span data-stu-id="11c77-118">For more information on views, see [View Folders](mapi-view-folders.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="11c77-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="11c77-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="11c77-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="11c77-120">Header files</span></span>

<span data-ttu-id="11c77-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11c77-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="11c77-122">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="11c77-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="11c77-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="11c77-123">Mapitags.h</span></span>
  
> <span data-ttu-id="11c77-124">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="11c77-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11c77-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="11c77-125">See also</span></span>



[<span data-ttu-id="11c77-126">PidTagDefaultViewEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="11c77-126">PidTagDefaultViewEntryId Canonical Property</span></span>](pidtagdefaultviewentryid-canonical-property.md)
  
[<span data-ttu-id="11c77-127">PidTagViewsEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="11c77-127">PidTagViewsEntryId Canonical Property</span></span>](pidtagviewsentryid-canonical-property.md)


[<span data-ttu-id="11c77-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="11c77-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11c77-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="11c77-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11c77-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="11c77-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11c77-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="11c77-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

