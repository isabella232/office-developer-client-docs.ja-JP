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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d463be4a14ecf478bdcbddc50b4ad9360829befc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355154"
---
# <a name="pidtagrenderingposition-canonical-property"></a><span data-ttu-id="aee84-103">PidTagRenderingPosition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aee84-103">PidTagRenderingPosition Canonical Property</span></span>

  
  
<span data-ttu-id="aee84-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aee84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aee84-105">メイン メッセージ テキスト内の添付ファイルのレンダリングに使用するオフセットを文字で含む。</span><span class="sxs-lookup"><span data-stu-id="aee84-105">Contains an offset, in characters, to use in rendering an attachment within the main message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aee84-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="aee84-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aee84-107">PR_RENDERING_POSITION</span><span class="sxs-lookup"><span data-stu-id="aee84-107">PR_RENDERING_POSITION</span></span>  <br/> |
|<span data-ttu-id="aee84-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="aee84-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aee84-109">0x370B</span><span class="sxs-lookup"><span data-stu-id="aee84-109">0x370B</span></span>  <br/> |
|<span data-ttu-id="aee84-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="aee84-110">Data type:</span></span>  <br/> |<span data-ttu-id="aee84-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="aee84-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="aee84-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="aee84-112">Area:</span></span>  <br/> |<span data-ttu-id="aee84-113">MAPI 添付ファイル</span><span class="sxs-lookup"><span data-stu-id="aee84-113">MAPI attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aee84-114">注釈</span><span class="sxs-lookup"><span data-stu-id="aee84-114">Remarks</span></span>

<span data-ttu-id="aee84-115">指定されたオフセットが -1 (0xFFFFFFFF) の場合、添付ファイルは、このプロパティを使用してレンダリングされません。</span><span class="sxs-lookup"><span data-stu-id="aee84-115">When the supplied offset is -1 (0xFFFFFFFF), the attachment is not rendered by using this property.</span></span> <span data-ttu-id="aee84-116">-1 以外のすべての値は、添付 **ファイルを** レンダリングする PR_BODY ([PidTagBody](pidtagbody-canonical-property.md)) プロパティ内の位置を示します。</span><span class="sxs-lookup"><span data-stu-id="aee84-116">All values other than -1 indicate the position within the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property at which the attachment is to be rendered.</span></span>
  
 <span data-ttu-id="aee84-117">**メモ** ファイル内のこのプロパティで示 **PR_BODY** は添付ファイルに置き換えられる。</span><span class="sxs-lookup"><span data-stu-id="aee84-117">**Note** The character indicated by this property in **PR_BODY** is replaced by the attachment.</span></span> <span data-ttu-id="aee84-118">通常、この文字はスペースですが、特別なプレースホルダー文字も使用できます。</span><span class="sxs-lookup"><span data-stu-id="aee84-118">Typically this character is a space, although a special placeholder character can also be used.</span></span> 
  
<span data-ttu-id="aee84-119">このプロパティは文字で表されます。</span><span class="sxs-lookup"><span data-stu-id="aee84-119">This property is expressed in characters.</span></span> <span data-ttu-id="aee84-120">一部の文字セットでは、これはバイトと同等ではありません。</span><span class="sxs-lookup"><span data-stu-id="aee84-120">In some character sets this is not equivalent to bytes.</span></span> <span data-ttu-id="aee84-121">Unicode アプリケーションは、2 バイト文字に基づいて位置を計算できます。</span><span class="sxs-lookup"><span data-stu-id="aee84-121">Unicode applications can compute the position based on two-byte characters.</span></span> <span data-ttu-id="aee84-122">Double-Byte文字セット (DBCS) アプリケーションは、文字表現が 1 文字あたり 1 バイトから 2 バイトの間で異なっているので、このプロパティ値までテキストをスキャンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aee84-122">Double-Byte Character Set (DBCS) applications must scan the text up to this property value, because their character representation varies between one and two bytes per character.</span></span>
  
<span data-ttu-id="aee84-123">このプロパティは、リッチ テキスト形式 (RTF) テキストと一緒に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aee84-123">This property should not be used with Rich Text Format (RTF) text.</span></span> <span data-ttu-id="aee84-124">レンダリング位置は、オブジェクト添付ファイルプレースホルダーと呼ばれるエスケープ シーケンスによって RTF で示されます。</span><span class="sxs-lookup"><span data-stu-id="aee84-124">The rendering position is indicated in RTF by an escape sequence called the object attachment placeholder.</span></span> <span data-ttu-id="aee84-125">このシーケンスは、文字列の後に単一の文字 (通常はスペース) が続き、添付ファイルのレンダリングに置き  `\objattph` 換えられる文字列で構成されます。</span><span class="sxs-lookup"><span data-stu-id="aee84-125">This sequence consists of the string  `\objattph` followed by a single character, normally a space, that will be replaced by the attachment rendering.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="aee84-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="aee84-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aee84-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="aee84-127">Protocol specifications</span></span>

<span data-ttu-id="aee84-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aee84-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aee84-129">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="aee84-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aee84-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aee84-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aee84-131">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="aee84-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aee84-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="aee84-132">Header files</span></span>

<span data-ttu-id="aee84-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aee84-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="aee84-134">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="aee84-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="aee84-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aee84-135">Mapitags.h</span></span>
  
> <span data-ttu-id="aee84-136">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="aee84-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aee84-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="aee84-137">See also</span></span>



[<span data-ttu-id="aee84-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="aee84-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aee84-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aee84-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aee84-140">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="aee84-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aee84-141">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="aee84-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

