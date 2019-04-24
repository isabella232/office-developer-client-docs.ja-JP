---
title: PidLidSharingInitiatorEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorEntryId
api_type:
- COM
ms.assetid: 47f00706-83df-49cb-bda7-ef572d76a020
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bfe682fc3263278c6e1d02a29a8b6432f41ac79e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309528"
---
# <a name="pidlidsharinginitiatorentryid-canonical-property"></a><span data-ttu-id="649f3-103">PidLidSharingInitiatorEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="649f3-103">PidLidSharingInitiatorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="649f3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="649f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="649f3-105">共有メッセージのプロパティとして指定します。</span><span class="sxs-lookup"><span data-stu-id="649f3-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="649f3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="649f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="649f3-107">dispidSharingInitiatorEid</span><span class="sxs-lookup"><span data-stu-id="649f3-107">dispidSharingInitiatorEid</span></span>  <br/> |
|<span data-ttu-id="649f3-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="649f3-108">Property set:</span></span>  <br/> |<span data-ttu-id="649f3-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="649f3-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="649f3-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="649f3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="649f3-111">0x00008a09</span><span class="sxs-lookup"><span data-stu-id="649f3-111">0x00008A09</span></span>  <br/> |
|<span data-ttu-id="649f3-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="649f3-112">Data type:</span></span>  <br/> |<span data-ttu-id="649f3-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="649f3-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="649f3-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="649f3-114">Area:</span></span>  <br/> |<span data-ttu-id="649f3-115">共有</span><span class="sxs-lookup"><span data-stu-id="649f3-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="649f3-116">解説</span><span class="sxs-lookup"><span data-stu-id="649f3-116">Remarks</span></span>

<span data-ttu-id="649f3-117">このプロパティは、現在ログオンしているユーザーのアドレス帳の**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティの値に設定する必要があります ( [[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)を参照)。</span><span class="sxs-lookup"><span data-stu-id="649f3-117">This property must be set to the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property for the Address Book of the currently logged-on user (see [[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="649f3-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="649f3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="649f3-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="649f3-119">Protocol specifications</span></span>

<span data-ttu-id="649f3-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="649f3-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="649f3-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="649f3-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="649f3-122">[[OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="649f3-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="649f3-123">クライアント間でメールボックスフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="649f3-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="649f3-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="649f3-124">Header files</span></span>

<span data-ttu-id="649f3-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="649f3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="649f3-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="649f3-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="649f3-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="649f3-127">See also</span></span>



[<span data-ttu-id="649f3-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="649f3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="649f3-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="649f3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="649f3-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="649f3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="649f3-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="649f3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

