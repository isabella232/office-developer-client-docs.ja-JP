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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3be288b606e197b350c1b053303077c1cb984e9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303095"
---
# <a name="pidlidsharingremotename-canonical-property"></a><span data-ttu-id="e8086-103">PidLidSharingRemoteName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8086-103">PidLidSharingRemoteName Canonical Property</span></span>

  
  
<span data-ttu-id="e8086-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8086-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8086-105">共有するリモート フォルダーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8086-105">Specifies the name of the remote folder that is being shared.</span></span> <span data-ttu-id="e8086-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="e8086-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8086-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e8086-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8086-108">dispidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="e8086-108">dispidSharingRemoteName</span></span>  <br/> |
|<span data-ttu-id="e8086-109">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="e8086-109">Property set:</span></span>  <br/> |<span data-ttu-id="e8086-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="e8086-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="e8086-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e8086-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e8086-112">0x00008A05</span><span class="sxs-lookup"><span data-stu-id="e8086-112">0x00008A05</span></span>  <br/> |
|<span data-ttu-id="e8086-113">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e8086-113">Data type:</span></span>  <br/> |<span data-ttu-id="e8086-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e8086-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e8086-115">エリア:</span><span class="sxs-lookup"><span data-stu-id="e8086-115">Area:</span></span>  <br/> |<span data-ttu-id="e8086-116">共有</span><span class="sxs-lookup"><span data-stu-id="e8086-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8086-117">注釈</span><span class="sxs-lookup"><span data-stu-id="e8086-117">Remarks</span></span>

<span data-ttu-id="e8086-118">このプロパティは、共有するフォルダーの PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8086-118">This property must be set to the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property on the folder being shared.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e8086-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e8086-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e8086-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e8086-120">Protocol specifications</span></span>

<span data-ttu-id="e8086-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8086-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8086-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="e8086-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e8086-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8086-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8086-124">クライアント間でメールボックス フォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="e8086-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e8086-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e8086-125">Header files</span></span>

<span data-ttu-id="e8086-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e8086-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8086-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e8086-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8086-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="e8086-128">See also</span></span>



[<span data-ttu-id="e8086-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e8086-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8086-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8086-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8086-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e8086-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8086-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e8086-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

