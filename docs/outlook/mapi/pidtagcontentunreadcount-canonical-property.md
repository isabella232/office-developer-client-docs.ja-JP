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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9572a053182aaa59020a6816736b8a4b92e778b7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383836"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a><span data-ttu-id="00c4b-103">PidTagContentUnreadCount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="00c4b-103">PidTagContentUnreadCount Canonical Property</span></span>

  
  
<span data-ttu-id="00c4b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00c4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00c4b-105">メッセージ ・ ストアによって計算される、フォルダー内の未読メ ッ セージの数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="00c4b-105">Contains the number of unread messages in a folder, as computed by the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00c4b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="00c4b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00c4b-107">PR_CONTENT_UNREAD</span><span class="sxs-lookup"><span data-stu-id="00c4b-107">PR_CONTENT_UNREAD</span></span>  <br/> |
|<span data-ttu-id="00c4b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="00c4b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="00c4b-109">0x3603</span><span class="sxs-lookup"><span data-stu-id="00c4b-109">0x3603</span></span>  <br/> |
|<span data-ttu-id="00c4b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="00c4b-110">Data type:</span></span>  <br/> |<span data-ttu-id="00c4b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="00c4b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="00c4b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="00c4b-112">Area:</span></span>  <br/> |<span data-ttu-id="00c4b-113">Folder</span><span class="sxs-lookup"><span data-stu-id="00c4b-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00c4b-114">備考</span><span class="sxs-lookup"><span data-stu-id="00c4b-114">Remarks</span></span>

<span data-ttu-id="00c4b-115">関連は、目的が異なる、2 つのメッセージ ・ ストアによって計算されるこのプロパティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="00c4b-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="00c4b-116">MAPI フォルダーのオブジェクトでは、フォルダー内のメッセージの数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="00c4b-116">On a MAPI folder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="00c4b-117">カテゴリ別の MAPI テーブル内の見出し行には見出し行に対応するカテゴリ内の関連付けられていない未読メ ッ セージの数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="00c4b-117">In a heading row in categorized MAPI tables, it contains the number of unread non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="00c4b-118">このプロパティには、対象の MSGFLAG_READ フラグを**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティで設定しないフォルダー コンテンツ テーブル内のメッセージの数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="00c4b-118">This property contains the number of messages in the folder contents table for which the MSGFLAG_READ flag is not set in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="00c4b-119">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) のプロパティには、フォルダーのメッセージの合計数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="00c4b-119">The **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) property contains the total message count for the folder.</span></span> <span data-ttu-id="00c4b-120">**PR_CONTENT_COUNT**し、このプロパティは、クライアントには読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="00c4b-120">The **PR_CONTENT_COUNT** and this property are read-only to clients.</span></span> 
  
<span data-ttu-id="00c4b-121">一部のクライアント アプリケーションは、このプロパティの値により異なる方法でカテゴリの見出し行を表示します。</span><span class="sxs-lookup"><span data-stu-id="00c4b-121">Some client applications display the heading row of a category differently depending on the value of this property.</span></span> <span data-ttu-id="00c4b-122">たとえば、クライアントでは、太字で未読メ ッ セージを含むカテゴリを表示できます。</span><span class="sxs-lookup"><span data-stu-id="00c4b-122">For example, a client can display a category that includes unread messages in bold.</span></span> <span data-ttu-id="00c4b-123">このプロパティは、MAPI_E_INVALID_PARAMETER 値は、 [IMAPITable::SortTable](imapitable-sorttable.md)メソッドから返されるように分類しようとすると使用できません。</span><span class="sxs-lookup"><span data-stu-id="00c4b-123">This property cannot be used as a category and an attempt to do so results in the MAPI_E_INVALID_PARAMETER value being returned from the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="00c4b-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="00c4b-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00c4b-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="00c4b-125">Protocol specifications</span></span>

<span data-ttu-id="00c4b-126">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00c4b-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00c4b-127">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="00c4b-127">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00c4b-128">[[MS OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00c4b-128">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00c4b-129">フォルダーの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="00c4b-129">Handles folder operations.</span></span>
    
<span data-ttu-id="00c4b-130">[[MS OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00c4b-130">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00c4b-131">テーブルのコア オブジェクトに許容される操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="00c4b-131">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00c4b-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="00c4b-132">Header files</span></span>

<span data-ttu-id="00c4b-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00c4b-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="00c4b-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="00c4b-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="00c4b-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="00c4b-135">Mapitags.h</span></span>
  
> <span data-ttu-id="00c4b-136">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="00c4b-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00c4b-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="00c4b-137">See also</span></span>



[<span data-ttu-id="00c4b-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="00c4b-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00c4b-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="00c4b-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00c4b-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="00c4b-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00c4b-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="00c4b-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

