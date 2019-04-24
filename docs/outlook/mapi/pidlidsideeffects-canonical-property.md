---
title: PidLidSideEffects 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2d57e6a195036ead9eb42666876e91a72f65eb8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331298"
---
# <a name="pidlidsideeffects-canonical-property"></a><span data-ttu-id="37c15-103">PidLidSideEffects 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="37c15-103">PidLidSideEffects Canonical Property</span></span>

  
  
<span data-ttu-id="37c15-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37c15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37c15-105">エンドユーザーの入力に対してアクションを処理するときに、クライアントがメッセージオブジェクトを処理する方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="37c15-105">Controls how a message object is handled by the client when acting on end-user input.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37c15-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="37c15-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37c15-107">dispidsideeffects</span><span class="sxs-lookup"><span data-stu-id="37c15-107">dispidSideEffects</span></span>  <br/> |
|<span data-ttu-id="37c15-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="37c15-108">Property set:</span></span>  <br/> |<span data-ttu-id="37c15-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="37c15-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="37c15-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="37c15-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="37c15-111">0x00008510</span><span class="sxs-lookup"><span data-stu-id="37c15-111">0x00008510</span></span>  <br/> |
|<span data-ttu-id="37c15-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="37c15-112">Data type:</span></span>  <br/> |<span data-ttu-id="37c15-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="37c15-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="37c15-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="37c15-114">Area:</span></span>  <br/> |<span data-ttu-id="37c15-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="37c15-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37c15-116">解説</span><span class="sxs-lookup"><span data-stu-id="37c15-116">Remarks</span></span>

<span data-ttu-id="37c15-117">次のフラグのビット単位または0以上に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37c15-117">Must be set to a bitwise or zero or more of the following flags.</span></span>
  
|<span data-ttu-id="37c15-118">**名前**</span><span class="sxs-lookup"><span data-stu-id="37c15-118">**Name**</span></span>|<span data-ttu-id="37c15-119">**値**</span><span class="sxs-lookup"><span data-stu-id="37c15-119">**Value**</span></span>|<span data-ttu-id="37c15-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="37c15-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="37c15-121">seOpenToDelete</span><span class="sxs-lookup"><span data-stu-id="37c15-121">seOpenToDelete</span></span>  <br/> |<span data-ttu-id="37c15-122">0x0001</span><span class="sxs-lookup"><span data-stu-id="37c15-122">0x0001</span></span>  <br/> |<span data-ttu-id="37c15-123">メッセージオブジェクトを削除するときに、追加の処理が必要になります。</span><span class="sxs-lookup"><span data-stu-id="37c15-123">Additional processing is required on the message object when deleting.</span></span>  <br/> |
|<span data-ttu-id="37c15-124">senoframe</span><span class="sxs-lookup"><span data-stu-id="37c15-124">seNoFrame</span></span>  <br/> |<span data-ttu-id="37c15-125">0x0008</span><span class="sxs-lookup"><span data-stu-id="37c15-125">0x0008</span></span>  <br/> |<span data-ttu-id="37c15-126">メッセージオブジェクトに関連付けられている UI はありません。</span><span class="sxs-lookup"><span data-stu-id="37c15-126">No UI is associated with the message object.</span></span>  <br/> |
|<span data-ttu-id="37c15-127">secoercetoinbox</span><span class="sxs-lookup"><span data-stu-id="37c15-127">seCoerceToInbox</span></span>  <br/> |<span data-ttu-id="37c15-128">0x0010</span><span class="sxs-lookup"><span data-stu-id="37c15-128">0x0010</span></span>  <br/> |<span data-ttu-id="37c15-129">"IPF" という**PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) プロパティを使用して folder オブジェクトに移動またはコピーするときは、message オブジェクトで追加の処理が必要になります。メモ "です。</span><span class="sxs-lookup"><span data-stu-id="37c15-129">Additional processing is required on the message object when moving or copying to a folder object with a **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of "IPF.Note".</span></span>  <br/> |
|<span data-ttu-id="37c15-130">seOpenTocopy</span><span class="sxs-lookup"><span data-stu-id="37c15-130">seOpenTocopy</span></span>  <br/> |<span data-ttu-id="37c15-131">0x0020</span><span class="sxs-lookup"><span data-stu-id="37c15-131">0x0020</span></span>  <br/> |<span data-ttu-id="37c15-132">別のフォルダーにコピーする場合は、message オブジェクトで追加の処理が必要になります。</span><span class="sxs-lookup"><span data-stu-id="37c15-132">Additional processing is required on the message object when copying to another folder.</span></span>  <br/> |
|<span data-ttu-id="37c15-133">seopentomove</span><span class="sxs-lookup"><span data-stu-id="37c15-133">seOpenToMove</span></span>  <br/> |<span data-ttu-id="37c15-134">0x0040</span><span class="sxs-lookup"><span data-stu-id="37c15-134">0x0040</span></span>  <br/> |<span data-ttu-id="37c15-135">別のフォルダーに移動するときは、message オブジェクトで追加の処理が必要になります。</span><span class="sxs-lookup"><span data-stu-id="37c15-135">Additional processing is required on the message object when moving to another folder.</span></span>  <br/> |
|<span data-ttu-id="37c15-136">seopenforctxmenu</span><span class="sxs-lookup"><span data-stu-id="37c15-136">seOpenForCtxMenu</span></span>  <br/> |<span data-ttu-id="37c15-137">0x0100</span><span class="sxs-lookup"><span data-stu-id="37c15-137">0x0100</span></span>  <br/> |<span data-ttu-id="37c15-138">動詞をエンドユーザーに表示するときは、message オブジェクトで追加の処理が必要になります。</span><span class="sxs-lookup"><span data-stu-id="37c15-138">Additional processing is required on the message object when displaying verbs to the end-user.</span></span>  <br/> |
|<span data-ttu-id="37c15-139">seCannotUndoDelete</span><span class="sxs-lookup"><span data-stu-id="37c15-139">seCannotUndoDelete</span></span>  <br/> |<span data-ttu-id="37c15-140">0x0400</span><span class="sxs-lookup"><span data-stu-id="37c15-140">0x0400</span></span>  <br/> |<span data-ttu-id="37c15-141">削除操作を元に戻すことはできません。 "seOpenToDelete" が設定されていない限り、設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="37c15-141">Cannot undo delete operation, must not be set unless "seOpenToDelete" is set.</span></span>  <br/> |
|<span data-ttu-id="37c15-142">seCannotUndoCopy</span><span class="sxs-lookup"><span data-stu-id="37c15-142">seCannotUndoCopy</span></span>  <br/> |<span data-ttu-id="37c15-143">0x0800</span><span class="sxs-lookup"><span data-stu-id="37c15-143">0x0800</span></span>  <br/> |<span data-ttu-id="37c15-144">コピー操作を元に戻すことはできません。 "seOpenTocopy" が設定されていない限り、設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="37c15-144">Cannot undo copy operation, must not be set unless "seOpenTocopy" is set.</span></span>  <br/> |
|<span data-ttu-id="37c15-145">seCannotUndoMove</span><span class="sxs-lookup"><span data-stu-id="37c15-145">seCannotUndoMove</span></span>  <br/> |<span data-ttu-id="37c15-146">0x1000</span><span class="sxs-lookup"><span data-stu-id="37c15-146">0x1000</span></span>  <br/> |<span data-ttu-id="37c15-147">移動操作を元に戻すことはできません。 "seopentomove" が設定されている場合を除き、設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="37c15-147">Cannot undo move operation, must not be set unless "seOpenToMove" is set.</span></span>  <br/> |
|<span data-ttu-id="37c15-148">seHasScript</span><span class="sxs-lookup"><span data-stu-id="37c15-148">seHasScript</span></span>  <br/> |<span data-ttu-id="37c15-149">0x2000</span><span class="sxs-lookup"><span data-stu-id="37c15-149">0x2000</span></span>  <br/> |<span data-ttu-id="37c15-150">メッセージオブジェクトには、エンドユーザースクリプトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="37c15-150">The message object contains end-user script.</span></span>  <br/> |
|<span data-ttu-id="37c15-151">seOpenToPermDelete</span><span class="sxs-lookup"><span data-stu-id="37c15-151">seOpenToPermDelete</span></span>  <br/> |<span data-ttu-id="37c15-152">0x4000</span><span class="sxs-lookup"><span data-stu-id="37c15-152">0x4000</span></span>  <br/> |<span data-ttu-id="37c15-153">message オブジェクトを完全に削除するには、追加の処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="37c15-153">Additional processing is required to permanently delete the message object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="37c15-154">関連リソース</span><span class="sxs-lookup"><span data-stu-id="37c15-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="37c15-155">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="37c15-155">Protocol specifications</span></span>

<span data-ttu-id="37c15-156">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37c15-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37c15-157">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="37c15-157">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="37c15-158">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37c15-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37c15-159">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="37c15-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="37c15-160">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37c15-160">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37c15-161">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="37c15-161">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="37c15-162">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="37c15-162">Header files</span></span>

<span data-ttu-id="37c15-163">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="37c15-163">Mapidefs.h</span></span>
  
> <span data-ttu-id="37c15-164">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="37c15-164">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37c15-165">関連項目</span><span class="sxs-lookup"><span data-stu-id="37c15-165">See also</span></span>



[<span data-ttu-id="37c15-166">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="37c15-166">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37c15-167">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="37c15-167">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37c15-168">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="37c15-168">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37c15-169">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="37c15-169">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

