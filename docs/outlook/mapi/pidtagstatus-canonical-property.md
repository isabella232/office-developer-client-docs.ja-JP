---
title: PidTagStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: eb04983015e8557541e69981ec130ebf07598655
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588371"
---
# <a name="pidtagstatus-canonical-property"></a><span data-ttu-id="ca56d-103">PidTagStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca56d-103">PidTagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="ca56d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca56d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca56d-105">フォルダーの状態を定義するフラグのビットマスクで、32 ビットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca56d-105">Contains a 32-bit bitmask of flags that define folder status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca56d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ca56d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca56d-107">PR_STATUS</span><span class="sxs-lookup"><span data-stu-id="ca56d-107">PR_STATUS</span></span>  <br/> |
|<span data-ttu-id="ca56d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ca56d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ca56d-109">0x360B</span><span class="sxs-lookup"><span data-stu-id="ca56d-109">0x360B</span></span>  <br/> |
|<span data-ttu-id="ca56d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ca56d-110">Data type:</span></span>  <br/> |<span data-ttu-id="ca56d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ca56d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ca56d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ca56d-112">Area:</span></span>  <br/> |<span data-ttu-id="ca56d-113">MAPI のコンテナー</span><span class="sxs-lookup"><span data-stu-id="ca56d-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca56d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ca56d-114">Remarks</span></span>

<span data-ttu-id="ca56d-115">フォルダーに対してこのプロパティは、メッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティに似ています。</span><span class="sxs-lookup"><span data-stu-id="ca56d-115">This property for folders is analogous to the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property for messages.</span></span> <span data-ttu-id="ca56d-116">そのフラグは、クライアント アプリケーションのみに提供され、メッセージ ・ ストアには影響しません。</span><span class="sxs-lookup"><span data-stu-id="ca56d-116">Its flags are provided for the client application only and do not affect the message store.</span></span> <span data-ttu-id="ca56d-117">クライアントでは、使用したり、これらの設定を無視することができます。</span><span class="sxs-lookup"><span data-stu-id="ca56d-117">Clients can use or ignore these settings.</span></span> <span data-ttu-id="ca56d-118">クライアントでは、このプロパティのクライアントが定義可能なビットの値も定義できます。</span><span class="sxs-lookup"><span data-stu-id="ca56d-118">The client can also define its own values for the client-definable bits of this property.</span></span>
  
<span data-ttu-id="ca56d-119">1 つ以上次のフラグのビットマスクを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ca56d-119">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="ca56d-120">FLDSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="ca56d-120">FLDSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="ca56d-121">フォルダーが削除対象としてマークします。</span><span class="sxs-lookup"><span data-stu-id="ca56d-121">The folder is marked for deletion.</span></span> <span data-ttu-id="ca56d-122">クライアント アプリケーションでは、このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="ca56d-122">The client application sets this flag.</span></span>
    
<span data-ttu-id="ca56d-123">FLDSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="ca56d-123">FLDSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="ca56d-124">フォルダーが非表示にします。</span><span class="sxs-lookup"><span data-stu-id="ca56d-124">The folder is hidden.</span></span>
    
<span data-ttu-id="ca56d-125">FLDSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="ca56d-125">FLDSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="ca56d-126">フォルダーがハイライトされます、たとえば、ビデオの逆の順序で表示されています。</span><span class="sxs-lookup"><span data-stu-id="ca56d-126">The folder is highlighted, for example, shown in reverse video.</span></span>
    
<span data-ttu-id="ca56d-127">FLDSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="ca56d-127">FLDSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="ca56d-128">フォルダーがタグ付けされます。</span><span class="sxs-lookup"><span data-stu-id="ca56d-128">The folder is tagged.</span></span>
    
<span data-ttu-id="ca56d-129">メッセージ ストア プロバイダーは、このプロパティを設定する 1 つのフォルダーにまたは、アプリケーションに適切な状態を解釈のこれらの値とクライアントです。</span><span class="sxs-lookup"><span data-stu-id="ca56d-129">Message store providers set this property on a folder to one or more of these values and clients interpret the status as appropriate for their applications.</span></span> <span data-ttu-id="ca56d-130">たとえば、クライアントは、同じ方法で同じステータスを持つフォルダーを表示する階層テーブル内のフォルダー間で視覚的に区別するためにフォルダーの状態を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ca56d-130">For example, a client can use the folder status to visually differentiate between folders in a hierarchy table, displaying folders with the same status in the same way.</span></span> <span data-ttu-id="ca56d-131">ビデオ、タグ付きのフォルダーを逆に強調表示されているフォルダーを表示できるし、わかりやすいアイコンが削除対象としてマークされているフォルダーを表示できる隠しフォルダーを非表示にできます。</span><span class="sxs-lookup"><span data-stu-id="ca56d-131">Highlighted folders can be shown in reverse video, tagged folders and folders marked for deletion can be shown with a meaningful icon, and hidden folders can be concealed.</span></span>
  
<span data-ttu-id="ca56d-132">31 (「0x80000000」からの「0x10000」) をこのプロパティの 16 ビットは IPM のクライアント アプリケーションで使用できます。</span><span class="sxs-lookup"><span data-stu-id="ca56d-132">Bits 16 through 31 ("0x10000" through "0x80000000") of this property are available for use by the IPM client application.</span></span> <span data-ttu-id="ca56d-133">他のすべてのビットは、使用するため、MAPI ので予約されています上記の一覧で定義されていないものは、最初に 0 に設定する必要があり、変更されません。</span><span class="sxs-lookup"><span data-stu-id="ca56d-133">All other bits are reserved for use by MAPI; those not defined in the preceding list should be initially set to zero and not altered.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ca56d-134">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ca56d-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca56d-135">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ca56d-135">Protocol specifications</span></span>

<span data-ttu-id="ca56d-136">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca56d-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca56d-137">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ca56d-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ca56d-138">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca56d-138">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca56d-139">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="ca56d-139">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca56d-140">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ca56d-140">Header files</span></span>

<span data-ttu-id="ca56d-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca56d-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca56d-142">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ca56d-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="ca56d-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ca56d-143">Mapitags.h</span></span>
  
> <span data-ttu-id="ca56d-144">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca56d-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca56d-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="ca56d-145">See also</span></span>



[<span data-ttu-id="ca56d-146">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca56d-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca56d-147">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca56d-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca56d-148">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ca56d-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca56d-149">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ca56d-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

