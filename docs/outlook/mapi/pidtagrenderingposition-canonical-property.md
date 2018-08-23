---
title: PidTagRenderingPosition 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRenderingPosition
api_type:
- COM
ms.assetid: bce46687-17dc-4a3f-96be-303d8755158e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: aa149a81102a4981712ea3ca897d8b1ad448a1eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803332"
---
# <a name="pidtagrenderingposition-canonical-property"></a><span data-ttu-id="bf5bf-103">PidTagRenderingPosition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bf5bf-103">PidTagRenderingPosition Canonical Property</span></span>

  
  
<span data-ttu-id="bf5bf-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf5bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf5bf-105">メインのメッセージのテキスト内の添付ファイルのレンダリングに使用する文字数で、オフセットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-105">Contains an offset, in characters, to use in rendering an attachment within the main message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf5bf-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bf5bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf5bf-107">PR_RENDERING_POSITION</span><span class="sxs-lookup"><span data-stu-id="bf5bf-107">PR_RENDERING_POSITION</span></span>  <br/> |
|<span data-ttu-id="bf5bf-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bf5bf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf5bf-109">0x370B</span><span class="sxs-lookup"><span data-stu-id="bf5bf-109">0x370B</span></span>  <br/> |
|<span data-ttu-id="bf5bf-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bf5bf-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf5bf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bf5bf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bf5bf-112">領域:</span><span class="sxs-lookup"><span data-stu-id="bf5bf-112">Area:</span></span>  <br/> |<span data-ttu-id="bf5bf-113">MAPI 添付ファイル</span><span class="sxs-lookup"><span data-stu-id="bf5bf-113">MAPI attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf5bf-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bf5bf-114">Remarks</span></span>

<span data-ttu-id="bf5bf-115">指定されたオフセットが-1 (0 xffffffff) の場合、このプロパティを使用して、添付ファイルは表示されません。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-115">When the supplied offset is -1 (0xFFFFFFFF), the attachment is not rendered by using this property.</span></span> <span data-ttu-id="bf5bf-116">-1 以外のすべての値は、添付ファイルを表示するには ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティ内の位置を示します。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-116">All values other than -1 indicate the position within the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property at which the attachment is to be rendered.</span></span>
  
 <span data-ttu-id="bf5bf-117">**メモ**この**PR_BODY**プロパティで指定した文字は、添付ファイルに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-117">**Note** The character indicated by this property in **PR_BODY** is replaced by the attachment.</span></span> <span data-ttu-id="bf5bf-118">通常この文字がスペース、特別なプレース ホルダー文字を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-118">Typically this character is a space, although a special placeholder character can also be used.</span></span> 
  
<span data-ttu-id="bf5bf-119">このプロパティは、文字で表されます。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-119">This property is expressed in characters.</span></span> <span data-ttu-id="bf5bf-120">一部の文字セットでこれはバイトに相当します。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-120">In some character sets this is not equivalent to bytes.</span></span> <span data-ttu-id="bf5bf-121">Unicode アプリケーションには、2 バイト文字の位置を計算できます。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-121">Unicode applications can compute the position based on two-byte characters.</span></span> <span data-ttu-id="bf5bf-122">2 バイト文字セット (DBCS) アプリケーションでは、1 文字につき 1 つと 2 つのバイトの間でそれらの文字の表現が異なるために、このプロパティの値までのテキストをスキャンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-122">Double-Byte Character Set (DBCS) applications must scan the text up to this property value, because their character representation varies between one and two bytes per character.</span></span>
  
<span data-ttu-id="bf5bf-123">テキストをリッチ テキスト形式 (RTF) で、このプロパティを使用しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-123">This property should not be used with Rich Text Format (RTF) text.</span></span> <span data-ttu-id="bf5bf-124">オブジェクトの添付ファイルのプレース ホルダーと呼ばれるエスケープ シーケンスで rtf 形式の描画位置が示されます。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-124">The rendering position is indicated in RTF by an escape sequence called the object attachment placeholder.</span></span> <span data-ttu-id="bf5bf-125">このシーケンスは、文字列で構成されています`\objattph`通常、スペース、添付ファイルのレンダリングによって置き換えられる、1 つの文字の後にします。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-125">This sequence consists of the string  `\objattph` followed by a single character, normally a space, that will be replaced by the attachment rendering.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bf5bf-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bf5bf-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bf5bf-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bf5bf-127">Protocol specifications</span></span>

<span data-ttu-id="bf5bf-128">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf5bf-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf5bf-129">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bf5bf-130">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf5bf-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf5bf-131">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bf5bf-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bf5bf-132">Header files</span></span>

<span data-ttu-id="bf5bf-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf5bf-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf5bf-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf5bf-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bf5bf-135">Mapitags.h</span></span>
  
> <span data-ttu-id="bf5bf-136">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bf5bf-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf5bf-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf5bf-137">See also</span></span>



[<span data-ttu-id="bf5bf-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bf5bf-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf5bf-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bf5bf-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf5bf-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bf5bf-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf5bf-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bf5bf-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

