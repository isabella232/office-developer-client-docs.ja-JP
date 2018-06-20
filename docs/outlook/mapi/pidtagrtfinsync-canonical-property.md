---
title: PidTagRtfInSync の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 85e517601d291f144652befa267d8fd8f76dea64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803393"
---
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="9107f-103">PidTagRtfInSync の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="9107f-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="9107f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9107f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9107f-105">([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) である**PR_RTF_COMPRESSED**プロパティにこのメッセージの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) のプロパティと同じテキストの内容がある場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="9107f-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9107f-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="9107f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9107f-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="9107f-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="9107f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9107f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9107f-109">0x0E1F</span><span class="sxs-lookup"><span data-stu-id="9107f-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="9107f-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="9107f-110">Data type:</span></span>  <br/> |<span data-ttu-id="9107f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9107f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9107f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="9107f-112">Area:</span></span>  <br/> |<span data-ttu-id="9107f-113">Email</span><span class="sxs-lookup"><span data-stu-id="9107f-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9107f-114">備考</span><span class="sxs-lookup"><span data-stu-id="9107f-114">Remarks</span></span>

<span data-ttu-id="9107f-115">値が ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティをこのメッセージのテキスト形式のバージョンと、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティをリッチ テキスト形式 (RTF) バージョンが同じ以外の場合は TRUE の場合**PR_BODY**と**PR_RTF_COMPRESSED**の書式設定に空白文字です。</span><span class="sxs-lookup"><span data-stu-id="9107f-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="9107f-116">2 つのバージョンのテキストは、同じ順序で同じ文字で構成されます。</span><span class="sxs-lookup"><span data-stu-id="9107f-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="9107f-117">FALSE は、2 つのバージョンがテキスト コンテンツは同期されません[へ](rtfsync.md)の関数によって同期されるの値です。</span><span class="sxs-lookup"><span data-stu-id="9107f-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="9107f-118">1 つのバージョンが変更されているし、他のバージョンには、ありません。</span><span class="sxs-lookup"><span data-stu-id="9107f-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="9107f-119">値は、なし、2 つのバージョンでは、両方が存在か、以前存在していた場合は同期できません。</span><span class="sxs-lookup"><span data-stu-id="9107f-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="9107f-120">1 つのバージョンは削除されたり、大幅に同期が可能ではないことに変更します。</span><span class="sxs-lookup"><span data-stu-id="9107f-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="9107f-121">**PR_RTF_COMPRESSED**を変更したクライアント アプリケーションは、強制的に同期するには、このプロパティに false を指定の値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9107f-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="9107f-122">RTF に対応してメッセージ ・ ストアには、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)の呼び出し中に**行う**を使用して、同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="9107f-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="9107f-123">RTF に対応していないクライアントが**PR_RTF_COMPRESSED**を読む前に**PR_RTF_IN_SYNC**の設定を確認して必要な場合は最初の**行う**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9107f-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="9107f-124">**PR_BODY**が空白以外の値に変更がある場合、メッセージ ・ ストアは、同期を終了するのには**PR_RTF_IN_SYNC**を削除しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="9107f-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9107f-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9107f-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9107f-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9107f-126">Protocol specifications</span></span>

<span data-ttu-id="9107f-127">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9107f-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9107f-128">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9107f-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9107f-129">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9107f-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9107f-130">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="9107f-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9107f-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9107f-131">Header files</span></span>

<span data-ttu-id="9107f-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9107f-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="9107f-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9107f-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="9107f-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9107f-134">Mapitags.h</span></span>
  
> <span data-ttu-id="9107f-135">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9107f-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9107f-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="9107f-136">See also</span></span>



[<span data-ttu-id="9107f-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9107f-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9107f-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9107f-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9107f-139">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="9107f-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9107f-140">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="9107f-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

