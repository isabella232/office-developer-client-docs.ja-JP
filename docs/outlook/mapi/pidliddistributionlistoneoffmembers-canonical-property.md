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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fed4395274cb790ab8ab7ecf0456d4ecb9ec0134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335050"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a><span data-ttu-id="6cf2c-103">PidLidDistributionListOneOffMembers 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6cf2c-103">PidLidDistributionListOneOffMembers Canonical Property</span></span>

  
  
<span data-ttu-id="6cf2c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cf2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cf2c-105">個人用配布リストのメンバーに対応する1回限りの entryids のリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="6cf2c-105">Specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6cf2c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6cf2c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6cf2c-107">dispidDLOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="6cf2c-107">dispidDLOneOffMembers</span></span>  <br/> |
|<span data-ttu-id="6cf2c-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="6cf2c-108">Property set:</span></span>  <br/> |<span data-ttu-id="6cf2c-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="6cf2c-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="6cf2c-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6cf2c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6cf2c-111">0x00008054</span><span class="sxs-lookup"><span data-stu-id="6cf2c-111">0x00008054</span></span>  <br/> |
|<span data-ttu-id="6cf2c-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6cf2c-112">Data type:</span></span>  <br/> |<span data-ttu-id="6cf2c-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="6cf2c-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="6cf2c-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="6cf2c-114">Area:</span></span>  <br/> |<span data-ttu-id="6cf2c-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="6cf2c-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6cf2c-116">解説</span><span class="sxs-lookup"><span data-stu-id="6cf2c-116">Remarks</span></span>

<span data-ttu-id="6cf2c-117">これらの1回限りの entryids は、個人用配布リストのメンバーの表示名と電子メールアドレスをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="6cf2c-117">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="6cf2c-118">クライアントまたはサーバーがこのプロパティを設定する場合は、 **dispiddlmembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) プロパティと同期する必要があります。 **dispidDLOneOffMembers**プロパティの各エントリに対して、同じエントリが存在する必要があります。**dispiddlmembers**プロパティ内の位置。</span><span class="sxs-lookup"><span data-stu-id="6cf2c-118">If the client or the server set this property, it must be synchronized with the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property: for each entry in the **dispidDLOneOffMembers** property, there must be an entry in the same position in the **dispidDLMembers** property.</span></span> 
  
<span data-ttu-id="6cf2c-119">**dispidDLOneOffMembers**を設定する場合、クライアントまたはサーバーは、その合計サイズが15000バイトのサイズよりも小さいことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cf2c-119">When setting **dispidDLOneOffMembers**, the client or the server must ensure that its total size is less than 15,000 bytes in size.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6cf2c-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6cf2c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6cf2c-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6cf2c-121">Protocol specifications</span></span>

<span data-ttu-id="6cf2c-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cf2c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cf2c-123">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6cf2c-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6cf2c-124">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cf2c-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cf2c-125">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6cf2c-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6cf2c-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="6cf2c-126">Header files</span></span>

<span data-ttu-id="6cf2c-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6cf2c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6cf2c-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6cf2c-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6cf2c-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="6cf2c-129">See also</span></span>



[<span data-ttu-id="6cf2c-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="6cf2c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6cf2c-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6cf2c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6cf2c-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6cf2c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6cf2c-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6cf2c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

