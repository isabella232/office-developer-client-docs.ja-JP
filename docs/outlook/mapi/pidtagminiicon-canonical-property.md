---
title: PidTagMiniIcon 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356232"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="e4321-103">PidTagMiniIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e4321-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="e4321-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4321-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4321-105">フォームの半分サイズのアイコンのビットマップが格納されています。</span><span class="sxs-lookup"><span data-stu-id="e4321-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e4321-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e4321-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e4321-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="e4321-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="e4321-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e4321-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e4321-109">0x0ffc</span><span class="sxs-lookup"><span data-stu-id="e4321-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="e4321-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e4321-110">Data type:</span></span>  <br/> |<span data-ttu-id="e4321-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e4321-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e4321-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e4321-112">Area:</span></span>  <br/> |<span data-ttu-id="e4321-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="e4321-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4321-114">解説</span><span class="sxs-lookup"><span data-stu-id="e4321-114">Remarks</span></span>

<span data-ttu-id="e4321-115">このプロパティには、アイコンの32×32ピクセルのイメージが含まれています。これは、のコンテンツと同じです。.ico ファイル。ただし、左上の16×16ピクセルのみが重要であると見なされます。</span><span class="sxs-lookup"><span data-stu-id="e4321-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="e4321-116">通常、このプロパティはからコピーされます。フォーム構成ファイルの該当する [Description] セクションの SmallIcon 行で指定された .ico ファイル。</span><span class="sxs-lookup"><span data-stu-id="e4321-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="e4321-117">**メモ**一部のプラットフォームは16×16ピクセルのアイコンをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="e4321-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="e4321-118">このような場合、このプロパティの32×32形式は使用できますが、クライアントアプリケーションは表示の不整合を認識する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4321-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e4321-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e4321-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e4321-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e4321-120">Header files</span></span>

<span data-ttu-id="e4321-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e4321-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="e4321-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e4321-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="e4321-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="e4321-123">Mapitags.h</span></span>
  
> <span data-ttu-id="e4321-124">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e4321-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e4321-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="e4321-125">See also</span></span>



[<span data-ttu-id="e4321-126">PidTagIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e4321-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="e4321-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e4321-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e4321-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e4321-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e4321-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e4321-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e4321-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e4321-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

