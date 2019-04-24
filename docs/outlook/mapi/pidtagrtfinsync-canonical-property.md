---
title: PidTagRtfInSync 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ed038faf44f350b041191373cf573e7e185337c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357877"
---
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="cb8c1-103">PidTagRtfInSync 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cb8c1-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="cb8c1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb8c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb8c1-105">**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティのテキストコンテンツが、このメッセージの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティと同じである場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb8c1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="cb8c1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb8c1-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="cb8c1-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="cb8c1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="cb8c1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cb8c1-109">0x0e1f</span><span class="sxs-lookup"><span data-stu-id="cb8c1-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="cb8c1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="cb8c1-110">Data type:</span></span>  <br/> |<span data-ttu-id="cb8c1-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="cb8c1-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="cb8c1-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="cb8c1-112">Area:</span></span>  <br/> |<span data-ttu-id="cb8c1-113">電子メール</span><span class="sxs-lookup"><span data-stu-id="cb8c1-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb8c1-114">解説</span><span class="sxs-lookup"><span data-stu-id="cb8c1-114">Remarks</span></span>

<span data-ttu-id="cb8c1-115">値 TRUE は、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティ、このメッセージのプレーンテキストバージョン、および**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティ (リッチテキスト形式 (RTF)) が同一であることを意味します。ただし、**PR_BODY**の空白スペースと**PR_RTF_COMPRESSED**の書式設定。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="cb8c1-116">2つのバージョンのテキストは、同じシーケンスの同じ文字で構成されています。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="cb8c1-117">値が FALSE の場合は、テキストコンテンツに対して2つのバージョンが同期されませんが、 [rtfsync](rtfsync.md)関数による同期が可能であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="cb8c1-118">1つのバージョンが変更され、もう一方のバージョンにはがありません。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="cb8c1-119">値がない場合、2つのバージョンが存在しているか、存在していた場合は、同期できないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="cb8c1-120">1つのバージョンが削除または変更されたため、同期を実行できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="cb8c1-121">**PR_RTF_COMPRESSED**を変更したクライアントアプリケーションでは、このプロパティの値を FALSE に設定して同期を強制する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="cb8c1-122">RTF 対応のメッセージストアは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)呼び出しの間に**rtfsync**を使用して同期を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="cb8c1-123">RTF 対応クライアントは**PR_RTF_COMPRESSED**を読み取る前に**PR_RTF_IN_SYNC**の設定を確認し、必要に応じて**rtfsync**を最初に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="cb8c1-124">**PR_BODY**に空白以外の変更があった場合、メッセージストアは、同期を終了するために**PR_RTF_IN_SYNC**を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cb8c1-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cb8c1-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cb8c1-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="cb8c1-126">Protocol specifications</span></span>

<span data-ttu-id="cb8c1-127">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb8c1-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb8c1-128">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb8c1-129">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb8c1-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb8c1-130">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb8c1-131">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="cb8c1-131">Header files</span></span>

<span data-ttu-id="cb8c1-132">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb8c1-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb8c1-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="cb8c1-134">Mapitags</span><span class="sxs-lookup"><span data-stu-id="cb8c1-134">Mapitags.h</span></span>
  
> <span data-ttu-id="cb8c1-135">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb8c1-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb8c1-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="cb8c1-136">See also</span></span>



[<span data-ttu-id="cb8c1-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="cb8c1-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb8c1-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cb8c1-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb8c1-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cb8c1-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb8c1-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cb8c1-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

