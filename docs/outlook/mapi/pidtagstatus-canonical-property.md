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
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278793"
---
# <a name="pidtagstatus-canonical-property"></a><span data-ttu-id="f0cd8-103">PidTagStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0cd8-103">PidTagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="f0cd8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0cd8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0cd8-105">フォルダーの状態を定義するフラグの32ビットビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-105">Contains a 32-bit bitmask of flags that define folder status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f0cd8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f0cd8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f0cd8-107">PR_STATUS</span><span class="sxs-lookup"><span data-stu-id="f0cd8-107">PR_STATUS</span></span>  <br/> |
|<span data-ttu-id="f0cd8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f0cd8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f0cd8-109">0x360b</span><span class="sxs-lookup"><span data-stu-id="f0cd8-109">0x360B</span></span>  <br/> |
|<span data-ttu-id="f0cd8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f0cd8-110">Data type:</span></span>  <br/> |<span data-ttu-id="f0cd8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f0cd8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f0cd8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f0cd8-112">Area:</span></span>  <br/> |<span data-ttu-id="f0cd8-113">MAPI コンテナー</span><span class="sxs-lookup"><span data-stu-id="f0cd8-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0cd8-114">解説</span><span class="sxs-lookup"><span data-stu-id="f0cd8-114">Remarks</span></span>

<span data-ttu-id="f0cd8-115">フォルダーのこのプロパティは、メッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティに似ています。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-115">This property for folders is analogous to the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property for messages.</span></span> <span data-ttu-id="f0cd8-116">このフラグは、クライアントアプリケーションに対してのみ提供され、メッセージストアには影響しません。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-116">Its flags are provided for the client application only and do not affect the message store.</span></span> <span data-ttu-id="f0cd8-117">クライアントは、これらの設定を使用または無視できます。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-117">Clients can use or ignore these settings.</span></span> <span data-ttu-id="f0cd8-118">クライアントは、このプロパティのクライアントで定義可能なビットに対して独自の値を定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-118">The client can also define its own values for the client-definable bits of this property.</span></span>
  
<span data-ttu-id="f0cd8-119">ビットマスクには、次の1つ以上のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-119">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="f0cd8-120">FLDSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="f0cd8-120">FLDSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="f0cd8-121">フォルダーは削除するように設定されています。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-121">The folder is marked for deletion.</span></span> <span data-ttu-id="f0cd8-122">クライアントアプリケーションがこのフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-122">The client application sets this flag.</span></span>
    
<span data-ttu-id="f0cd8-123">FLDSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="f0cd8-123">FLDSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="f0cd8-124">フォルダーは表示されません。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-124">The folder is hidden.</span></span>
    
<span data-ttu-id="f0cd8-125">FLDSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="f0cd8-125">FLDSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="f0cd8-126">フォルダーが強調表示されます。たとえば、[リバースビデオ] に示されています。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-126">The folder is highlighted, for example, shown in reverse video.</span></span>
    
<span data-ttu-id="f0cd8-127">FLDSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="f0cd8-127">FLDSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="f0cd8-128">フォルダーにタグが付けられます。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-128">The folder is tagged.</span></span>
    
<span data-ttu-id="f0cd8-129">メッセージストアプロバイダーは、フォルダーのこのプロパティをこれらの値の1つ以上に設定し、クライアントはアプリケーションに応じて状態を解釈します。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-129">Message store providers set this property on a folder to one or more of these values and clients interpret the status as appropriate for their applications.</span></span> <span data-ttu-id="f0cd8-130">たとえば、クライアントはフォルダーの状態を使用して、階層テーブル内のフォルダーを視覚的に区別し、同じ状態のフォルダーを同じ方法で表示することができます。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-130">For example, a client can use the folder status to visually differentiate between folders in a hierarchy table, displaying folders with the same status in the same way.</span></span> <span data-ttu-id="f0cd8-131">強調表示されたフォルダーを反転表示することができます。タグ付きフォルダーや削除用のマークが付いたフォルダーは、わかりやすいアイコンで表示できます。隠しフォルダーは非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-131">Highlighted folders can be shown in reverse video, tagged folders and folders marked for deletion can be shown with a meaningful icon, and hidden folders can be concealed.</span></span>
  
<span data-ttu-id="f0cd8-132">このプロパティのビット16から 31 (";" ~ "0x80000000") は、IPM クライアントアプリケーションで使用できます。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-132">Bits 16 through 31 ("0x10000" through "0x80000000") of this property are available for use by the IPM client application.</span></span> <span data-ttu-id="f0cd8-133">他のすべてのビットは MAPI での使用のために予約されています。前述のリストで定義されていないものは、最初は0に設定され、変更されません。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-133">All other bits are reserved for use by MAPI; those not defined in the preceding list should be initially set to zero and not altered.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f0cd8-134">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f0cd8-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f0cd8-135">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f0cd8-135">Protocol specifications</span></span>

<span data-ttu-id="f0cd8-136">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0cd8-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0cd8-137">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f0cd8-138">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0cd8-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0cd8-139">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-139">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f0cd8-140">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="f0cd8-140">Header files</span></span>

<span data-ttu-id="f0cd8-141">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0cd8-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="f0cd8-142">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="f0cd8-143">Mapitags</span><span class="sxs-lookup"><span data-stu-id="f0cd8-143">Mapitags.h</span></span>
  
> <span data-ttu-id="f0cd8-144">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f0cd8-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0cd8-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0cd8-145">See also</span></span>



[<span data-ttu-id="f0cd8-146">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f0cd8-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f0cd8-147">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0cd8-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f0cd8-148">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f0cd8-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f0cd8-149">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f0cd8-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

