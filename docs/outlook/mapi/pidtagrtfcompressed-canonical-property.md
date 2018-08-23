---
title: PidTagRtfCompressed 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c93d850551e766e97292d5417c3be5577f557af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803382"
---
# <a name="pidtagrtfcompressed-canonical-property"></a><span data-ttu-id="8fd80-103">PidTagRtfCompressed 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8fd80-103">PidTagRtfCompressed Canonical Property</span></span>

  
  
<span data-ttu-id="8fd80-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8fd80-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8fd80-105">リッチ テキスト形式 (RTF) バージョン圧縮形式では通常、メッセージのテキストにはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8fd80-105">Contains the Rich Text Format (RTF) version of the message text, usually in compressed form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8fd80-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8fd80-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8fd80-107">PR_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="8fd80-107">PR_RTF_COMPRESSED</span></span>  <br/> |
|<span data-ttu-id="8fd80-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8fd80-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8fd80-109">0x1009</span><span class="sxs-lookup"><span data-stu-id="8fd80-109">0x1009</span></span>  <br/> |
|<span data-ttu-id="8fd80-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8fd80-110">Data type:</span></span>  <br/> |<span data-ttu-id="8fd80-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8fd80-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8fd80-112">領域:</span><span class="sxs-lookup"><span data-stu-id="8fd80-112">Area:</span></span>  <br/> |<span data-ttu-id="8fd80-113">メール</span><span class="sxs-lookup"><span data-stu-id="8fd80-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fd80-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8fd80-114">Remarks</span></span>

<span data-ttu-id="8fd80-115">このプロパティには、([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティとしては、rtf 形式では、同じメッセージ テキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8fd80-115">This property contains the same message text as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property but in RTF.</span></span> 
  
<span data-ttu-id="8fd80-116">Rtf 形式のメッセージのテキストは通常、圧縮形式で格納します。</span><span class="sxs-lookup"><span data-stu-id="8fd80-116">Message text in RTF is normally stored in compressed form.</span></span> <span data-ttu-id="8fd80-117">ただし、いくつかのシステムでは、書式設定されたテキストは圧縮の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="8fd80-117">However, some systems do not compress formatted text.</span></span> <span data-ttu-id="8fd80-118">MAPI が圧縮されていない rtf 形式、およびメッセージの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) で、 **STORE_UNCOMPRESSED_RTF**フラグを指定するようにストリーム ヘッダーの dwMagicUncompressedRTF 値を提供する対応するためにを保存すると、非圧縮の rtf 形式を格納できることを示します。</span><span class="sxs-lookup"><span data-stu-id="8fd80-118">To accommodate them, MAPI provides the dwMagicUncompressedRTF value for a stream header to identify uncompressed RTF, and the **STORE_UNCOMPRESSED_RTF** flag in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) for the message store to indicate it can store uncompressed RTF.</span></span> 
  
<span data-ttu-id="8fd80-119">このプロパティの内容を取得するには、 **OpenProperty**を呼び出してから、 **MAPI_READ**フラグを使用して[WrapCompressedRTFStream](wrapcompressedrtfstream.md)をコールします。</span><span class="sxs-lookup"><span data-stu-id="8fd80-119">To obtain the contents of this property, call **OpenProperty**, then call [WrapCompressedRTFStream](wrapcompressedrtfstream.md) with the **MAPI_READ** flag.</span></span> <span data-ttu-id="8fd80-120">このプロパティに書き込むには、 **MAPI_MODIFY**と**タグ**のフラグが設定されたことを開きます。</span><span class="sxs-lookup"><span data-stu-id="8fd80-120">To write into this property, open it with the **MAPI_MODIFY** and **MAPI_CREATE** flags.</span></span> <span data-ttu-id="8fd80-121">これにより、新しいデータは、古いデータを完全に置き換えるし、更新プログラムの格納の最小数を使用して書き込みを実行することです。</span><span class="sxs-lookup"><span data-stu-id="8fd80-121">This ensures that the new data completely replace any old data and that the writes are performed using the minimum number of store updates.</span></span> 
  
<span data-ttu-id="8fd80-122">RTF をサポートしているメッセージ ・ ストアは、メッセージのテキスト内の空白への変更を無視します。</span><span class="sxs-lookup"><span data-stu-id="8fd80-122">Message stores that support RTF ignore any changes to white space in the message text.</span></span> <span data-ttu-id="8fd80-123">**PR_BODY**が最初に保存されると、メッセージ ・ ストアによっても生成し、このプロパティを格納します。</span><span class="sxs-lookup"><span data-stu-id="8fd80-123">When **PR_BODY** is stored for the first time, the message store also generates and stores this property.</span></span> <span data-ttu-id="8fd80-124">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出された後で、 **PR_BODY**が変更された場合は、メッセージ ・ ストアは、rtf 形式のバージョンとの同期を確実に[行う](rtfsync.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8fd80-124">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="8fd80-125">プロパティを左の空白が変更されているだけの場合そのままです。</span><span class="sxs-lookup"><span data-stu-id="8fd80-125">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="8fd80-126">これには、任意の複雑な RTF メッセージが RTF に対応していないクライアントを通過するときの書式を設定して、メッセージング システムが保持されます。</span><span class="sxs-lookup"><span data-stu-id="8fd80-126">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8fd80-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8fd80-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8fd80-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8fd80-128">Protocol specifications</span></span>

<span data-ttu-id="8fd80-129">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8fd80-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8fd80-130">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8fd80-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8fd80-131">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8fd80-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8fd80-132">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="8fd80-132">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="8fd80-133">[[MS OXRTFCP]](http://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8fd80-133">[[MS-OXRTFCP]](http://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8fd80-134">エンコードし、圧縮された RTF メッセージの本文のストリームをデコードします。</span><span class="sxs-lookup"><span data-stu-id="8fd80-134">Encodes and decodes a compressed stream in RTF message bodies.</span></span>
    
<span data-ttu-id="8fd80-135">[[MS OXRTFEX]](http://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8fd80-135">[[MS-OXRTFEX]](http://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8fd80-136">内のメッセージと添付ファイルの rtf 形式の本文のプロパティ (HTML) などの他のコンテンツ形式をカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="8fd80-136">Encapsulates additional content formats (such as HTML) within the RTF body property of messages and attachments.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8fd80-137">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8fd80-137">Header files</span></span>

<span data-ttu-id="8fd80-138">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8fd80-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="8fd80-139">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8fd80-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="8fd80-140">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8fd80-140">Mapitags.h</span></span>
  
> <span data-ttu-id="8fd80-141">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8fd80-141">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8fd80-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="8fd80-142">See also</span></span>



[<span data-ttu-id="8fd80-143">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8fd80-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8fd80-144">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8fd80-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8fd80-145">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8fd80-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8fd80-146">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8fd80-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

