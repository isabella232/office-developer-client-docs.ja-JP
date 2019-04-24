---
title: PidLidSharingRemoteUid 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c3e783934367ad7c5c1a9a760aa8a24525901832
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331263"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="ffd96-103">PidLidSharingRemoteUid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ffd96-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="ffd96-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffd96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffd96-105">共有するリモートフォルダーのエントリ ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="ffd96-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="ffd96-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="ffd96-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ffd96-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ffd96-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="ffd96-108">dispidsharingremoteuid</span><span class="sxs-lookup"><span data-stu-id="ffd96-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="ffd96-109">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="ffd96-109">Property set:</span></span>  <br/> |<span data-ttu-id="ffd96-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="ffd96-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="ffd96-111">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ffd96-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ffd96-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="ffd96-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="ffd96-113">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ffd96-113">Data type:</span></span>  <br/> |<span data-ttu-id="ffd96-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ffd96-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ffd96-115">エリア:</span><span class="sxs-lookup"><span data-stu-id="ffd96-115">Area:</span></span>  <br/> |<span data-ttu-id="ffd96-116">共有</span><span class="sxs-lookup"><span data-stu-id="ffd96-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffd96-117">解説</span><span class="sxs-lookup"><span data-stu-id="ffd96-117">Remarks</span></span>

<span data-ttu-id="ffd96-118">このプロパティは、共有されているフォルダーの PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティの値を表す16進数文字列で設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffd96-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="ffd96-119">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="ffd96-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ffd96-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ffd96-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ffd96-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ffd96-121">Protocol specifications</span></span>

<span data-ttu-id="ffd96-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffd96-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffd96-123">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ffd96-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ffd96-124">[[OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffd96-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffd96-125">クライアント間でメールボックスフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="ffd96-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ffd96-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="ffd96-126">Header files</span></span>

<span data-ttu-id="ffd96-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ffd96-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="ffd96-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ffd96-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ffd96-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="ffd96-129">See also</span></span>



[<span data-ttu-id="ffd96-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ffd96-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ffd96-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ffd96-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ffd96-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ffd96-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ffd96-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ffd96-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

