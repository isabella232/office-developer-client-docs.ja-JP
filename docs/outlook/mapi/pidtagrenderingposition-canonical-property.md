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
ms.openlocfilehash: d463be4a14ecf478bdcbddc50b4ad9360829befc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355154"
---
# <a name="pidtagrenderingposition-canonical-property"></a><span data-ttu-id="0cdb7-103">PidTagRenderingPosition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0cdb7-103">PidTagRenderingPosition Canonical Property</span></span>

  
  
<span data-ttu-id="0cdb7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0cdb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0cdb7-105">メインメッセージテキスト内で添付ファイルをレンダリングするときに使用するオフセット (文字数) を含みます。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-105">Contains an offset, in characters, to use in rendering an attachment within the main message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0cdb7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0cdb7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0cdb7-107">PR_RENDERING_POSITION</span><span class="sxs-lookup"><span data-stu-id="0cdb7-107">PR_RENDERING_POSITION</span></span>  <br/> |
|<span data-ttu-id="0cdb7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0cdb7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0cdb7-109">0x370b</span><span class="sxs-lookup"><span data-stu-id="0cdb7-109">0x370B</span></span>  <br/> |
|<span data-ttu-id="0cdb7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0cdb7-110">Data type:</span></span>  <br/> |<span data-ttu-id="0cdb7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0cdb7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0cdb7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="0cdb7-112">Area:</span></span>  <br/> |<span data-ttu-id="0cdb7-113">MAPI 添付ファイル</span><span class="sxs-lookup"><span data-stu-id="0cdb7-113">MAPI attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cdb7-114">解説</span><span class="sxs-lookup"><span data-stu-id="0cdb7-114">Remarks</span></span>

<span data-ttu-id="0cdb7-115">指定したオフセットが-1 (0xffffffff) の場合、添付ファイルはこのプロパティを使用してレンダリングされません。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-115">When the supplied offset is -1 (0xFFFFFFFF), the attachment is not rendered by using this property.</span></span> <span data-ttu-id="0cdb7-116">-1 以外のすべての値は、添付ファイルがレンダリングされる**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティ内の位置を示します。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-116">All values other than -1 indicate the position within the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property at which the attachment is to be rendered.</span></span>
  
 <span data-ttu-id="0cdb7-117">**メモ\*\*\*\*PR_BODY**でこのプロパティによって示される文字は、添付ファイルに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-117">**Note** The character indicated by this property in **PR_BODY** is replaced by the attachment.</span></span> <span data-ttu-id="0cdb7-118">通常、この文字はスペースですが、特別なプレースホルダー文字を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-118">Typically this character is a space, although a special placeholder character can also be used.</span></span> 
  
<span data-ttu-id="0cdb7-119">このプロパティは、文字で表されます。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-119">This property is expressed in characters.</span></span> <span data-ttu-id="0cdb7-120">一部の文字セットでは、これはバイト数と同じではありません。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-120">In some character sets this is not equivalent to bytes.</span></span> <span data-ttu-id="0cdb7-121">Unicode アプリケーションは、2バイト文字に基づいて位置を計算できます。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-121">Unicode applications can compute the position based on two-byte characters.</span></span> <span data-ttu-id="0cdb7-122">2バイト文字セット (DBCS) アプリケーションがこのプロパティ値までテキストをスキャンする必要があるのは、文字ごとに1文字と2バイトの文字表現が異なるためです。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-122">Double-Byte Character Set (DBCS) applications must scan the text up to this property value, because their character representation varies between one and two bytes per character.</span></span>
  
<span data-ttu-id="0cdb7-123">このプロパティは、リッチテキスト形式 (RTF) テキストには使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-123">This property should not be used with Rich Text Format (RTF) text.</span></span> <span data-ttu-id="0cdb7-124">レンダリング位置は、RTF では、オブジェクトの添付ファイルプレースホルダーと呼ばれるエスケープシーケンスによって示されます。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-124">The rendering position is indicated in RTF by an escape sequence called the object attachment placeholder.</span></span> <span data-ttu-id="0cdb7-125">このシーケンスは、文字列`\objattph`の後に1つの文字 (通常はスペース) で構成され、添付ファイルのレンダリングによって置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-125">This sequence consists of the string  `\objattph` followed by a single character, normally a space, that will be replaced by the attachment rendering.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0cdb7-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0cdb7-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0cdb7-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0cdb7-127">Protocol specifications</span></span>

<span data-ttu-id="0cdb7-128">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0cdb7-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0cdb7-129">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0cdb7-130">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0cdb7-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0cdb7-131">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0cdb7-132">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="0cdb7-132">Header files</span></span>

<span data-ttu-id="0cdb7-133">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0cdb7-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="0cdb7-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="0cdb7-135">Mapitags</span><span class="sxs-lookup"><span data-stu-id="0cdb7-135">Mapitags.h</span></span>
  
> <span data-ttu-id="0cdb7-136">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0cdb7-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0cdb7-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="0cdb7-137">See also</span></span>



[<span data-ttu-id="0cdb7-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0cdb7-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0cdb7-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0cdb7-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0cdb7-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0cdb7-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0cdb7-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0cdb7-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

