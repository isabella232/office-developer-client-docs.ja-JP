---
title: PidTagContentUnreadCount 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9572a053182aaa59020a6816736b8a4b92e778b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331872"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a><span data-ttu-id="013c8-103">PidTagContentUnreadCount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="013c8-103">PidTagContentUnreadCount Canonical Property</span></span>

  
  
<span data-ttu-id="013c8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="013c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="013c8-105">メッセージ ストアによって計算される、フォルダー内の未読メッセージの数を格納します。</span><span class="sxs-lookup"><span data-stu-id="013c8-105">Contains the number of unread messages in a folder, as computed by the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="013c8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="013c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="013c8-107">PR_CONTENT_UNREAD</span><span class="sxs-lookup"><span data-stu-id="013c8-107">PR_CONTENT_UNREAD</span></span>  <br/> |
|<span data-ttu-id="013c8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="013c8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="013c8-109">0x3603</span><span class="sxs-lookup"><span data-stu-id="013c8-109">0x3603</span></span>  <br/> |
|<span data-ttu-id="013c8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="013c8-110">Data type:</span></span>  <br/> |<span data-ttu-id="013c8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="013c8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="013c8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="013c8-112">Area:</span></span>  <br/> |<span data-ttu-id="013c8-113">Folder</span><span class="sxs-lookup"><span data-stu-id="013c8-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="013c8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="013c8-114">Remarks</span></span>

<span data-ttu-id="013c8-115">メッセージ ストアによって計算されるこのプロパティは、関連する 2 つの異なる目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="013c8-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="013c8-116">MAPI フォルダー オブジェクトには、フォルダー内のメッセージの数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="013c8-116">On a MAPI folder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="013c8-117">分類された MAPI テーブルの見出し行には、その見出し行に対応するカテゴリ内の未読の非関連メッセージの数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="013c8-117">In a heading row in categorized MAPI tables, it contains the number of unread non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="013c8-118">このプロパティには、PR_MESSAGE_FLAGS **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティで MSGFLAG_READ フラグが設定されていないフォルダーコンテンツ テーブル内のメッセージの数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="013c8-118">This property contains the number of messages in the folder contents table for which the MSGFLAG_READ flag is not set in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="013c8-119">プロパティ **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) プロパティには、フォルダーの合計メッセージ数が含まれる。</span><span class="sxs-lookup"><span data-stu-id="013c8-119">The **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) property contains the total message count for the folder.</span></span> <span data-ttu-id="013c8-120">クライアント **PR_CONTENT_COUNT** このプロパティは、クライアントへの読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="013c8-120">The **PR_CONTENT_COUNT** and this property are read-only to clients.</span></span> 
  
<span data-ttu-id="013c8-121">一部のクライアント アプリケーションでは、このプロパティの値に応じてカテゴリの見出し行が異なります。</span><span class="sxs-lookup"><span data-stu-id="013c8-121">Some client applications display the heading row of a category differently depending on the value of this property.</span></span> <span data-ttu-id="013c8-122">たとえば、クライアントは、未読メッセージを太字で含むカテゴリを表示できます。</span><span class="sxs-lookup"><span data-stu-id="013c8-122">For example, a client can display a category that includes unread messages in bold.</span></span> <span data-ttu-id="013c8-123">このプロパティをカテゴリとして使用することはできません。そのため [、IMAPITable::SortTable](imapitable-sorttable.md) メソッドから MAPI_E_INVALID_PARAMETER 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="013c8-123">This property cannot be used as a category and an attempt to do so results in the MAPI_E_INVALID_PARAMETER value being returned from the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="013c8-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="013c8-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="013c8-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="013c8-125">Protocol specifications</span></span>

<span data-ttu-id="013c8-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="013c8-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="013c8-127">関連するプロトコル仕様へのMicrosoft Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="013c8-127">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="013c8-128">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="013c8-128">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="013c8-129">フォルダー操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="013c8-129">Handles folder operations.</span></span>
    
<span data-ttu-id="013c8-130">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="013c8-130">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="013c8-131">コア テーブル オブジェクトに対して許容される操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="013c8-131">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="013c8-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="013c8-132">Header files</span></span>

<span data-ttu-id="013c8-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="013c8-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="013c8-134">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="013c8-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="013c8-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="013c8-135">Mapitags.h</span></span>
  
> <span data-ttu-id="013c8-136">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="013c8-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="013c8-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="013c8-137">See also</span></span>



[<span data-ttu-id="013c8-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="013c8-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="013c8-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="013c8-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="013c8-140">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="013c8-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="013c8-141">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="013c8-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

