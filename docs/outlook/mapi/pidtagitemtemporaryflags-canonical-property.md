---
title: PidTagItemTemporaryflags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagItemTemporaryflags
api_type:
- HeaderDef
ms.assetid: 8066de8e-2b77-4bac-8df3-e64b03ee42b9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ec092e6cc6174e156dbfe7784143c9d74715eef7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357702"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a><span data-ttu-id="5a70c-103">PidTagItemTemporaryflags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5a70c-103">PidTagItemTemporaryflags Canonical Property</span></span>

  
  
<span data-ttu-id="5a70c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a70c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a70c-105">メッセージが読み取り済みで、読み取りとしてマークされていないかどうかを示すフラグが含まれる。</span><span class="sxs-lookup"><span data-stu-id="5a70c-105">Contains a flag that indicates that a message has been read, but not marked as read.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a70c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5a70c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a70c-107">PR_ITEM_TMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="5a70c-107">PR_ITEM_TMPFLAGS</span></span>  <br/> |
|<span data-ttu-id="5a70c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5a70c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a70c-109">0x1097</span><span class="sxs-lookup"><span data-stu-id="5a70c-109">0x1097</span></span>  <br/> |
|<span data-ttu-id="5a70c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5a70c-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a70c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5a70c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5a70c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="5a70c-112">Area:</span></span>  <br/> |<span data-ttu-id="5a70c-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="5a70c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a70c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5a70c-114">Remarks</span></span>

<span data-ttu-id="5a70c-115">このプロパティは、Outlook の [未読メッセージ] 検索フォルダーで使用され、実際に読み取りとしてマークせずに読み取ったメッセージを追跡し、フォルダーから削除します。</span><span class="sxs-lookup"><span data-stu-id="5a70c-115">This property is used in Outlook's Unread Messages search folder to keep track of which messages have been read without actually marking them as read, which would remove them from the folder.</span></span> <span data-ttu-id="5a70c-116">ビューが変更されると、このプロパティは削除され、アイテムは読み取りとしてマークされます。</span><span class="sxs-lookup"><span data-stu-id="5a70c-116">When the view changes this property is removed and the item is marked as read.</span></span> <span data-ttu-id="5a70c-117">このプロパティは、このプロパティと同期Exchange Server。</span><span class="sxs-lookup"><span data-stu-id="5a70c-117">This property will not synchronize to the Exchange Server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5a70c-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5a70c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a70c-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5a70c-119">Protocol specifications</span></span>

<span data-ttu-id="5a70c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a70c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a70c-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="5a70c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a70c-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a70c-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a70c-123">フォルダー操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="5a70c-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a70c-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5a70c-124">Header files</span></span>

<span data-ttu-id="5a70c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a70c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a70c-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a70c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a70c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5a70c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="5a70c-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="5a70c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a70c-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a70c-129">See also</span></span>



[<span data-ttu-id="5a70c-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5a70c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a70c-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5a70c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a70c-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5a70c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a70c-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5a70c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

