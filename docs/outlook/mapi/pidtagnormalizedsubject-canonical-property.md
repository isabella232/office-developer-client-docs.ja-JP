---
title: PidTagNormalizedSubject の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 74061f33a88dceb371cad00ef44f611b583f7ae2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803026"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a><span data-ttu-id="6f637-103">PidTagNormalizedSubject の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="6f637-103">PidTagNormalizedSubject Canonical Property</span></span>

  
  
<span data-ttu-id="6f637-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f637-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f637-105">削除任意のプレフィックスを持つメッセージの件名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6f637-105">Contains the message subject with any prefix removed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f637-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="6f637-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f637-107">PR_NORMALIZED_SUBJECT、PR_NORMALIZED_SUBJECT_A、PR_NORMALIZED_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="6f637-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="6f637-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6f637-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f637-109">0x0E1D</span><span class="sxs-lookup"><span data-stu-id="6f637-109">0x0E1D</span></span>  <br/> |
|<span data-ttu-id="6f637-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="6f637-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f637-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6f637-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6f637-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6f637-112">Area:</span></span>  <br/> |<span data-ttu-id="6f637-113">Email</span><span class="sxs-lookup"><span data-stu-id="6f637-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f637-114">備考</span><span class="sxs-lookup"><span data-stu-id="6f637-114">Remarks</span></span>

<span data-ttu-id="6f637-115">これらのプロパティは、メッセージ ・ ストアでは、計算またはトランスポート プロバイダーが**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) と**されて**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) のプロパティからの次のようにします。</span><span class="sxs-lookup"><span data-stu-id="6f637-115">These properties are computed by message store or transport providers from the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties in the following manner.</span></span>
  
- <span data-ttu-id="6f637-116">**されて**と**あるの PR_SUBJECT**の最初の部分文字列では、 **PR_NORMALIZED_SUBJECT**と関連するプロパティが**あるの PR_SUBJECT**の内容にプリフィックスを削除した設定です。</span><span class="sxs-lookup"><span data-stu-id="6f637-116">If the **PR_SUBJECT_PREFIX** is present and is an initial substring of **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** and associated properties are set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
- <span data-ttu-id="6f637-117">**されて**が削除され、次の規則を使用して**あるの PR_SUBJECT**から再計算**されて**がある場合は、**あるの PR_SUBJECT**の最初の部分文字列ではありません: 文字列が**あるの PR_SUBJECT**に含まれている場合コロンとスペースの後に数字以外の文字を 1 ~ 3 から始まるとコロン、空白文字列のプレフィックスになります。</span><span class="sxs-lookup"><span data-stu-id="6f637-117">If **PR_SUBJECT_PREFIX** is present, but it is not an initial substring of **PR_SUBJECT**, **PR_SUBJECT_PREFIX** is deleted and recalculated from **PR_SUBJECT** using the following rule: If the string contained in **PR_SUBJECT** begins with one to three non-numeric characters followed by a colon and a space, then the string together with the colon and the blank becomes the prefix.</span></span> <span data-ttu-id="6f637-118">数値、空白、および句読点の文字は、文字の有効なプレフィックスではありません。</span><span class="sxs-lookup"><span data-stu-id="6f637-118">Numbers, blanks, and punctuation characters are not valid prefix characters.</span></span> 
    
- <span data-ttu-id="6f637-119">**されて**がない場合は、前の手順に記載されているルールを使用して**あるの PR_SUBJECT**から計算されます。</span><span class="sxs-lookup"><span data-stu-id="6f637-119">If **PR_SUBJECT_PREFIX** is not present, it is calculated from **PR_SUBJECT** using the rule outlined in the previous step.</span></span> <span data-ttu-id="6f637-120">このし、プロパティが**あるの PR_SUBJECT**の内容を削除するプレフィックスを持つ。</span><span class="sxs-lookup"><span data-stu-id="6f637-120">This property then is set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
 <span data-ttu-id="6f637-121">**メモ****されて**空の文字列がある場合、**あるの PR_SUBJECT**このプロパティは、同じです。</span><span class="sxs-lookup"><span data-stu-id="6f637-121">**Note** When **PR_SUBJECT_PREFIX** is an empty string, **PR_SUBJECT** and this property are the same.</span></span> 
  
<span data-ttu-id="6f637-122">最終的には、このプロパティには、**あるの PR_SUBJECT**の接頭辞の後の部分があります。</span><span class="sxs-lookup"><span data-stu-id="6f637-122">Ultimately, this property should be the part of **PR_SUBJECT** following the prefix.</span></span> <span data-ttu-id="6f637-123">プレフィックスがない場合、このプロパティが**あるの PR_SUBJECT**と同じになります。</span><span class="sxs-lookup"><span data-stu-id="6f637-123">If there is no prefix, this property becomes the same as **PR_SUBJECT**.</span></span>
  
 <span data-ttu-id="6f637-124">**されて**このプロパティは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)の実装の一部として計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f637-124">**PR_SUBJECT_PREFIX** and this property should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="6f637-125">コミットされた後になるまで、クライアント アプリケーションで値を[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドのメッセージを表示しない**IMAPIProp::SaveChanges**の呼び出しによって、です。</span><span class="sxs-lookup"><span data-stu-id="6f637-125">A client application should not prompt the [IMAPIProp::GetProps](imapiprop-getprops.md) method for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="6f637-126">256 文字は、通常は短い文字列は、件名のプロパティと、メッセージ ストア プロバイダーがそれらのオブジェクトのリンクと埋め込み (OLE) の**IStream**インターフェイスをサポートする義務を負いません。</span><span class="sxs-lookup"><span data-stu-id="6f637-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="6f637-127">クライアントは、 **IMAPIProp**インターフェイスを介してアクセスを最初に試行し、MAPI_E_NOT_ENOUGH_MEMORY が返された場合にのみ、 **IStream**に頼る必要があります常に。</span><span class="sxs-lookup"><span data-stu-id="6f637-127">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if MAPI_E_NOT_ENOUGH_MEMORY is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6f637-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6f637-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f637-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6f637-129">Protocol specifications</span></span>

<span data-ttu-id="6f637-130">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f637-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f637-131">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6f637-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6f637-132">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f637-132">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f637-133">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="6f637-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6f637-134">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f637-134">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f637-135">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6f637-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6f637-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6f637-136">Header files</span></span>

<span data-ttu-id="6f637-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f637-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f637-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6f637-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f637-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6f637-139">Mapitags.h</span></span>
  
> <span data-ttu-id="6f637-140">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6f637-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f637-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f637-141">See also</span></span>



[<span data-ttu-id="6f637-142">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6f637-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f637-143">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6f637-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f637-144">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="6f637-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f637-145">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="6f637-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

