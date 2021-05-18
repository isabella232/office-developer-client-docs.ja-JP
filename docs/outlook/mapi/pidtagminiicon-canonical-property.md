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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405416"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="d10bb-103">PidTagMiniIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d10bb-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="d10bb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d10bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d10bb-105">フォームのハーフサイズ アイコンのビットマップを含む。</span><span class="sxs-lookup"><span data-stu-id="d10bb-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d10bb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d10bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d10bb-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="d10bb-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="d10bb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d10bb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d10bb-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="d10bb-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="d10bb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d10bb-110">Data type:</span></span>  <br/> |<span data-ttu-id="d10bb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d10bb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d10bb-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d10bb-112">Area:</span></span>  <br/> |<span data-ttu-id="d10bb-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="d10bb-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d10bb-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d10bb-114">Remarks</span></span>

<span data-ttu-id="d10bb-115">このプロパティには、アイコンの 32 × 32 ピクセルの画像が含まれる。これは、 の内容と同じです。ICO ファイルですが、左上 16 ピクセル× 16 ピクセルだけが重要と見なされます。</span><span class="sxs-lookup"><span data-stu-id="d10bb-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="d10bb-116">このプロパティは、通常は . からコピーされます。フォーム構成ファイルの適切な [Description] セクションの SmallIcon 行で指定された ICO ファイル。</span><span class="sxs-lookup"><span data-stu-id="d10bb-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="d10bb-117">**メモ** 一部のプラットフォームでは、16 ピクセル×アイコンがサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d10bb-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="d10bb-118">このプロパティの 32 × 32 形式は、このような場合に使用できますが、クライアント アプリケーションは、表示の不整合に注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d10bb-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d10bb-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d10bb-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d10bb-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d10bb-120">Header files</span></span>

<span data-ttu-id="d10bb-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d10bb-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="d10bb-122">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d10bb-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="d10bb-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d10bb-123">Mapitags.h</span></span>
  
> <span data-ttu-id="d10bb-124">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d10bb-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d10bb-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="d10bb-125">See also</span></span>



[<span data-ttu-id="d10bb-126">PidTagIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d10bb-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="d10bb-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d10bb-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d10bb-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d10bb-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d10bb-129">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d10bb-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d10bb-130">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d10bb-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

