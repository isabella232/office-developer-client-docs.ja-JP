---
title: PidLidDistributionListOneOffMembers 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListOneOffMembers
api_type:
- COM
ms.assetid: 0b92e654-9e2d-4c2e-9a63-d5fac603b0c0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fed4395274cb790ab8ab7ecf0456d4ecb9ec0134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335050"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a><span data-ttu-id="3db67-103">PidLidDistributionListOneOffMembers 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3db67-103">PidLidDistributionListOneOffMembers Canonical Property</span></span>

  
  
<span data-ttu-id="3db67-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3db67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3db67-105">個人用配布リストのメンバーに対応する 1 回限定の EntryId の一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="3db67-105">Specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3db67-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3db67-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3db67-107">dispidDLOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="3db67-107">dispidDLOneOffMembers</span></span>  <br/> |
|<span data-ttu-id="3db67-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="3db67-108">Property set:</span></span>  <br/> |<span data-ttu-id="3db67-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="3db67-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="3db67-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="3db67-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3db67-111">0x00008054</span><span class="sxs-lookup"><span data-stu-id="3db67-111">0x00008054</span></span>  <br/> |
|<span data-ttu-id="3db67-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3db67-112">Data type:</span></span>  <br/> |<span data-ttu-id="3db67-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="3db67-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="3db67-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="3db67-114">Area:</span></span>  <br/> |<span data-ttu-id="3db67-115">Contact</span><span class="sxs-lookup"><span data-stu-id="3db67-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3db67-116">注釈</span><span class="sxs-lookup"><span data-stu-id="3db67-116">Remarks</span></span>

<span data-ttu-id="3db67-117">これらの 1 回限定の EntryIds は、個人用配布リスト メンバーの表示名と電子メール アドレスをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="3db67-117">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="3db67-118">クライアントまたはサーバーでこのプロパティを設定する場合は **、dispidDLMembers** [(PidLidDistributionListMembers)](pidliddistributionlistmembers-canonical-property.md)プロパティと同期する必要があります **。dispidDLOneOffMembers** プロパティの各エントリに対して **、dispidDLMembers** プロパティ内に同じ位置にエントリが必要です。</span><span class="sxs-lookup"><span data-stu-id="3db67-118">If the client or the server set this property, it must be synchronized with the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property: for each entry in the **dispidDLOneOffMembers** property, there must be an entry in the same position in the **dispidDLMembers** property.</span></span> 
  
<span data-ttu-id="3db67-119">**dispidDLOneOffMembers** を設定する場合、クライアントまたはサーバーは、その合計サイズが 15,000 バイト未満のサイズである必要があります。</span><span class="sxs-lookup"><span data-stu-id="3db67-119">When setting **dispidDLOneOffMembers**, the client or the server must ensure that its total size is less than 15,000 bytes in size.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3db67-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3db67-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3db67-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3db67-121">Protocol specifications</span></span>

<span data-ttu-id="3db67-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3db67-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3db67-123">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="3db67-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3db67-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3db67-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3db67-125">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3db67-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3db67-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3db67-126">Header files</span></span>

<span data-ttu-id="3db67-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3db67-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="3db67-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3db67-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3db67-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="3db67-129">See also</span></span>



[<span data-ttu-id="3db67-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3db67-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3db67-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3db67-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3db67-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3db67-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3db67-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3db67-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

