---
title: PidLidSharingRemoteUid の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteUid
api_type:
- COM
ms.assetid: cfe3b728-317b-4871-adea-e2fdf8441da7
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: cb8b4a7c71f3ad81949f3eac6cab230f40c6d487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802170"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="68ab3-103">PidLidSharingRemoteUid の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="68ab3-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="68ab3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68ab3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68ab3-105">リモート共有フォルダーのエントリ ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="68ab3-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="68ab3-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="68ab3-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68ab3-107">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="68ab3-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="68ab3-108">dispidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="68ab3-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="68ab3-109">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="68ab3-109">Property set:</span></span>  <br/> |<span data-ttu-id="68ab3-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="68ab3-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="68ab3-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="68ab3-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="68ab3-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="68ab3-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="68ab3-113">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="68ab3-113">Data type:</span></span>  <br/> |<span data-ttu-id="68ab3-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="68ab3-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="68ab3-115">領域:</span><span class="sxs-lookup"><span data-stu-id="68ab3-115">Area:</span></span>  <br/> |<span data-ttu-id="68ab3-116">共有</span><span class="sxs-lookup"><span data-stu-id="68ab3-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68ab3-117">備考</span><span class="sxs-lookup"><span data-stu-id="68ab3-117">Remarks</span></span>

<span data-ttu-id="68ab3-118">このプロパティは、共有されているフォルダーに PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティの値の 16 進数の文字列形式に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68ab3-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="68ab3-119">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="68ab3-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="68ab3-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="68ab3-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="68ab3-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="68ab3-121">Protocol specifications</span></span>

<span data-ttu-id="68ab3-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68ab3-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68ab3-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="68ab3-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="68ab3-124">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68ab3-124">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68ab3-125">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="68ab3-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="68ab3-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="68ab3-126">Header files</span></span>

<span data-ttu-id="68ab3-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="68ab3-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="68ab3-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="68ab3-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68ab3-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="68ab3-129">See also</span></span>



[<span data-ttu-id="68ab3-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="68ab3-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="68ab3-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="68ab3-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="68ab3-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="68ab3-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="68ab3-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="68ab3-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

