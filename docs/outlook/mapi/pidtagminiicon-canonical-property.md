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
ms.openlocfilehash: 5514e0553f719e2e875aad7001bb38a6a52e8e08
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589778"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="b7948-103">PidTagMiniIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7948-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="b7948-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7948-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7948-105">フォームの半分のサイズのアイコンのビットマップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b7948-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7948-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b7948-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7948-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="b7948-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="b7948-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b7948-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b7948-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="b7948-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="b7948-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b7948-110">Data type:</span></span>  <br/> |<span data-ttu-id="b7948-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b7948-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b7948-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b7948-112">Area:</span></span>  <br/> |<span data-ttu-id="b7948-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="b7948-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7948-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b7948-114">Remarks</span></span>

<span data-ttu-id="b7948-115">このプロパティには、内容と同じアイコンの 32 × 32 ピクセルのイメージが含まれているのです。ICO ファイルですが、左上の 16 × 16 ピクセルだけは、重要と見なされます。</span><span class="sxs-lookup"><span data-stu-id="b7948-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="b7948-116">このプロパティは通常からコピーします。ICO ファイルが小さい行のフォーム構成ファイルの該当する [説明] セクションで指定されています。</span><span class="sxs-lookup"><span data-stu-id="b7948-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="b7948-117">**メモ**いくつかのプラットフォームのサポート 16 × 16 ピクセル アイコンではない操作を行います。</span><span class="sxs-lookup"><span data-stu-id="b7948-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="b7948-118">32 × 32 の形式このプロパティは、このようなケースでは使用できませんが、クライアント アプリケーションは表示の矛盾に注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7948-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b7948-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b7948-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b7948-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b7948-120">Header files</span></span>

<span data-ttu-id="b7948-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7948-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7948-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7948-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="b7948-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b7948-123">Mapitags.h</span></span>
  
> <span data-ttu-id="b7948-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b7948-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7948-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7948-125">See also</span></span>



[<span data-ttu-id="b7948-126">PidTagIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7948-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="b7948-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7948-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7948-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7948-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7948-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b7948-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7948-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b7948-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

