---
title: PidLidContactLinkSearchKey の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactLinkSearchKey
api_type:
- COM
ms.assetid: 82d21d38-a6c6-4e12-85b1-8158b2f5cce7
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 65a54475afe526cce40030cbfd1cdb9e86126554
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801852"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a><span data-ttu-id="14469-103">PidLidContactLinkSearchKey の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="14469-103">PidLidContactLinkSearchKey Canonical Property</span></span>

<span data-ttu-id="14469-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="14469-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="14469-105">このメッセージ オブジェクトにリンクされている連絡先の**SearchKeys**の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="14469-105">Contains the list of **SearchKeys** for the contact linked to by this message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="14469-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="14469-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="14469-107">dispidContactLinkSearchKey</span><span class="sxs-lookup"><span data-stu-id="14469-107">dispidContactLinkSearchKey</span></span>  <br/> |
|<span data-ttu-id="14469-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="14469-108">Property set:</span></span>  <br/> |<span data-ttu-id="14469-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="14469-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="14469-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="14469-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="14469-111">0x00008584</span><span class="sxs-lookup"><span data-stu-id="14469-111">0x00008584</span></span>  <br/> |
|<span data-ttu-id="14469-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="14469-112">Data type:</span></span>  <br/> |<span data-ttu-id="14469-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="14469-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="14469-114">領域:</span><span class="sxs-lookup"><span data-stu-id="14469-114">Area:</span></span>  <br/> |<span data-ttu-id="14469-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="14469-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14469-116">備考</span><span class="sxs-lookup"><span data-stu-id="14469-116">Remarks</span></span>

|<span data-ttu-id="14469-117">**長さ (バイト単位)**</span><span class="sxs-lookup"><span data-stu-id="14469-117">**Length in bytes**</span></span>|<span data-ttu-id="14469-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="14469-118">**Description**</span></span>|<span data-ttu-id="14469-119">**メモ**</span><span class="sxs-lookup"><span data-stu-id="14469-119">**Notes**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="14469-120">2</span><span class="sxs-lookup"><span data-stu-id="14469-120">2</span></span>  <br/> |<span data-ttu-id="14469-121">ContactEntryCount</span><span class="sxs-lookup"><span data-stu-id="14469-121">ContactEntryCount</span></span>  <br/> |<span data-ttu-id="14469-122">なし</span><span class="sxs-lookup"><span data-stu-id="14469-122">None</span></span>  <br/> |
|<span data-ttu-id="14469-123">変数</span><span class="sxs-lookup"><span data-stu-id="14469-123">variable</span></span>  <br/> |<span data-ttu-id="14469-124">SearchKey データ</span><span class="sxs-lookup"><span data-stu-id="14469-124">SearchKey data</span></span>  <br/> |<span data-ttu-id="14469-125">ContactEntryCount 回繰り返されます</span><span class="sxs-lookup"><span data-stu-id="14469-125">Repeats ContactEntryCount times</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="14469-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="14469-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="14469-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="14469-127">Protocol specifications</span></span>

<span data-ttu-id="14469-128">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14469-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14469-129">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="14469-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="14469-130">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14469-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14469-131">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="14469-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="14469-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="14469-132">Header files</span></span>

<span data-ttu-id="14469-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="14469-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="14469-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="14469-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14469-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="14469-135">See also</span></span>

- [<span data-ttu-id="14469-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="14469-136">MAPI Properties</span></span>](mapi-properties.md) 
- [<span data-ttu-id="14469-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="14469-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="14469-138">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="14469-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="14469-139">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="14469-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

