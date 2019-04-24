---
title: PidLidSharingRemoteName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteName
api_type:
- COM
ms.assetid: be975f74-4b95-45a4-bbee-959fa8e4ad45
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3be288b606e197b350c1b053303077c1cb984e9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303095"
---
# <a name="pidlidsharingremotename-canonical-property"></a><span data-ttu-id="1a2ce-103">PidLidSharingRemoteName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a2ce-103">PidLidSharingRemoteName Canonical Property</span></span>

  
  
<span data-ttu-id="1a2ce-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a2ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a2ce-105">共有されているリモートフォルダーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="1a2ce-105">Specifies the name of the remote folder that is being shared.</span></span> <span data-ttu-id="1a2ce-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="1a2ce-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a2ce-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1a2ce-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a2ce-108">dispidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="1a2ce-108">dispidSharingRemoteName</span></span>  <br/> |
|<span data-ttu-id="1a2ce-109">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="1a2ce-109">Property set:</span></span>  <br/> |<span data-ttu-id="1a2ce-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="1a2ce-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="1a2ce-111">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1a2ce-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1a2ce-112">0x00008a05</span><span class="sxs-lookup"><span data-stu-id="1a2ce-112">0x00008A05</span></span>  <br/> |
|<span data-ttu-id="1a2ce-113">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1a2ce-113">Data type:</span></span>  <br/> |<span data-ttu-id="1a2ce-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1a2ce-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1a2ce-115">エリア:</span><span class="sxs-lookup"><span data-stu-id="1a2ce-115">Area:</span></span>  <br/> |<span data-ttu-id="1a2ce-116">共有</span><span class="sxs-lookup"><span data-stu-id="1a2ce-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a2ce-117">解説</span><span class="sxs-lookup"><span data-stu-id="1a2ce-117">Remarks</span></span>

<span data-ttu-id="1a2ce-118">このプロパティは、共有するフォルダーの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a2ce-118">This property must be set to the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property on the folder being shared.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1a2ce-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1a2ce-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a2ce-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1a2ce-120">Protocol specifications</span></span>

<span data-ttu-id="1a2ce-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a2ce-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a2ce-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1a2ce-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1a2ce-123">[[OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a2ce-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a2ce-124">クライアント間でメールボックスフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="1a2ce-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a2ce-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1a2ce-125">Header files</span></span>

<span data-ttu-id="1a2ce-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a2ce-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a2ce-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1a2ce-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a2ce-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a2ce-128">See also</span></span>



[<span data-ttu-id="1a2ce-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1a2ce-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a2ce-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a2ce-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a2ce-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1a2ce-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a2ce-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1a2ce-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

