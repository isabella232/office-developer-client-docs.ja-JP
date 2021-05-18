---
title: PidLidContactLinkSearchKey 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ea815631f63b5585a3f2705cfbd2639b8c655e6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319776"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a><span data-ttu-id="928b0-103">PidLidContactLinkSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="928b0-103">PidLidContactLinkSearchKey Canonical Property</span></span>

<span data-ttu-id="928b0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="928b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="928b0-105">このメッセージ オブジェクトによってリンクされた連絡先の **SearchKeys** の一覧を格納します。</span><span class="sxs-lookup"><span data-stu-id="928b0-105">Contains the list of **SearchKeys** for the contact linked to by this message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="928b0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="928b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="928b0-107">dispidContactLinkSearchKey</span><span class="sxs-lookup"><span data-stu-id="928b0-107">dispidContactLinkSearchKey</span></span>  <br/> |
|<span data-ttu-id="928b0-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="928b0-108">Property set:</span></span>  <br/> |<span data-ttu-id="928b0-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="928b0-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="928b0-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="928b0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="928b0-111">0x00008584</span><span class="sxs-lookup"><span data-stu-id="928b0-111">0x00008584</span></span>  <br/> |
|<span data-ttu-id="928b0-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="928b0-112">Data type:</span></span>  <br/> |<span data-ttu-id="928b0-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="928b0-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="928b0-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="928b0-114">Area:</span></span>  <br/> |<span data-ttu-id="928b0-115">Contact</span><span class="sxs-lookup"><span data-stu-id="928b0-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="928b0-116">注釈</span><span class="sxs-lookup"><span data-stu-id="928b0-116">Remarks</span></span>

|<span data-ttu-id="928b0-117">**長さ (バイト単位)**</span><span class="sxs-lookup"><span data-stu-id="928b0-117">**Length in bytes**</span></span>|<span data-ttu-id="928b0-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="928b0-118">**Description**</span></span>|<span data-ttu-id="928b0-119">**メモ**</span><span class="sxs-lookup"><span data-stu-id="928b0-119">**Notes**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="928b0-120">2</span><span class="sxs-lookup"><span data-stu-id="928b0-120">2</span></span>  <br/> |<span data-ttu-id="928b0-121">ContactEntryCount</span><span class="sxs-lookup"><span data-stu-id="928b0-121">ContactEntryCount</span></span>  <br/> |<span data-ttu-id="928b0-122">なし</span><span class="sxs-lookup"><span data-stu-id="928b0-122">None</span></span>  <br/> |
|<span data-ttu-id="928b0-123">変数</span><span class="sxs-lookup"><span data-stu-id="928b0-123">variable</span></span>  <br/> |<span data-ttu-id="928b0-124">SearchKey データ</span><span class="sxs-lookup"><span data-stu-id="928b0-124">SearchKey data</span></span>  <br/> |<span data-ttu-id="928b0-125">ContactEntryCount の繰り返し回数</span><span class="sxs-lookup"><span data-stu-id="928b0-125">Repeats ContactEntryCount times</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="928b0-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="928b0-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="928b0-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="928b0-127">Protocol specifications</span></span>

<span data-ttu-id="928b0-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="928b0-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="928b0-129">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="928b0-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="928b0-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="928b0-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="928b0-131">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="928b0-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="928b0-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="928b0-132">Header files</span></span>

<span data-ttu-id="928b0-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="928b0-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="928b0-134">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="928b0-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="928b0-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="928b0-135">See also</span></span>

- [<span data-ttu-id="928b0-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="928b0-136">MAPI Properties</span></span>](mapi-properties.md) 
- [<span data-ttu-id="928b0-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="928b0-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="928b0-138">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="928b0-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="928b0-139">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="928b0-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

