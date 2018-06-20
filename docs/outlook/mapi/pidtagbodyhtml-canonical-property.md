---
title: PidTagBodyHtml の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 19f0398d5e36cce13467a4fae86c4ea1d4019dd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802521"
---
# <a name="pidtagbodyhtml-canonical-property"></a><span data-ttu-id="52f9b-103">PidTagBodyHtml の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="52f9b-103">PidTagBodyHtml Canonical Property</span></span>

  
  
<span data-ttu-id="52f9b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52f9b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52f9b-105">ハイパー テキスト マークアップ言語 (HTML) バージョン メッセージのテキストにはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="52f9b-105">Contains the Hypertext Markup Language (HTML) version of the message text.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52f9b-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="52f9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52f9b-107">PR_BODY_HTML、PR_BODY_HTML_A、PR_BODY_HTML_W</span><span class="sxs-lookup"><span data-stu-id="52f9b-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span></span>  <br/> |
|<span data-ttu-id="52f9b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="52f9b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52f9b-109">0x1013</span><span class="sxs-lookup"><span data-stu-id="52f9b-109">0x1013</span></span>  <br/> |
|<span data-ttu-id="52f9b-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="52f9b-110">Data type:</span></span>  <br/> |<span data-ttu-id="52f9b-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="52f9b-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="52f9b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="52f9b-112">Area:</span></span>  <br/> |<span data-ttu-id="52f9b-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="52f9b-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52f9b-114">備考</span><span class="sxs-lookup"><span data-stu-id="52f9b-114">Remarks</span></span>

<span data-ttu-id="52f9b-115">これらのプロパティには、 **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)) が、html 形式では、同じメッセージ テキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="52f9b-115">These properties contain the same message text as the **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), but in HTML.</span></span> 
  
<span data-ttu-id="52f9b-116">HTML をサポートしているメッセージ ・ ストアは、その**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) で**STORE_HTML_OK**フラグを設定することによってこれを示します。</span><span class="sxs-lookup"><span data-stu-id="52f9b-116">A message store that supports HTML indicates this by setting the **STORE_HTML_OK** flag in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span></span> 
  
 <span data-ttu-id="52f9b-117">**メモ****STORE_HTML_OK**は、Microsoft® Exchange 2000 Server 以前のバージョンとが含まれている Mapidefs.h のバージョンでは定義されていません。</span><span class="sxs-lookup"><span data-stu-id="52f9b-117">**Note** **STORE_HTML_OK** is not defined in versions of Mapidefs.h included with Microsoft® Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="52f9b-118">**STORE_HTML_OK**が定義されていない場合は、0x00010000 の値を使用してください。</span><span class="sxs-lookup"><span data-stu-id="52f9b-118">If **STORE_HTML_OK** is undefined, use the value 0x00010000 instead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="52f9b-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="52f9b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52f9b-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="52f9b-120">Protocol specifications</span></span>

<span data-ttu-id="52f9b-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52f9b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52f9b-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="52f9b-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="52f9b-123">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52f9b-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52f9b-124">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="52f9b-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52f9b-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="52f9b-125">Header files</span></span>

<span data-ttu-id="52f9b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52f9b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="52f9b-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="52f9b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="52f9b-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="52f9b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="52f9b-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="52f9b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52f9b-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="52f9b-130">See also</span></span>



[<span data-ttu-id="52f9b-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="52f9b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52f9b-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="52f9b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52f9b-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="52f9b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52f9b-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="52f9b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

