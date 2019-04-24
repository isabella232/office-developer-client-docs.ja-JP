---
title: PidTagTemplateid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTemplateid
api_type:
- COM
ms.assetid: 1a418c76-ebc7-47f2-ac91-797162e6e099
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 96bcd15606771bd112568ad94133507ab14b2bcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358822"
---
# <a name="pidtagtemplateid-canonical-property"></a><span data-ttu-id="baf83-103">PidTagTemplateid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="baf83-103">PidTagTemplateid Canonical Property</span></span>

  
  
<span data-ttu-id="baf83-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="baf83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="baf83-105">永続的なエントリ ID 形式として表される、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) を含みます。</span><span class="sxs-lookup"><span data-stu-id="baf83-105">Contains the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), expressed as a permanent entry ID format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="baf83-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="baf83-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="baf83-107">PR_TEMPLATEID</span><span class="sxs-lookup"><span data-stu-id="baf83-107">PR_TEMPLATEID</span></span>  <br/> |
|<span data-ttu-id="baf83-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="baf83-108">Identifier:</span></span>  <br/> |<span data-ttu-id="baf83-109">0x3902</span><span class="sxs-lookup"><span data-stu-id="baf83-109">0x3902</span></span>  <br/> |
|<span data-ttu-id="baf83-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="baf83-110">Data type:</span></span>  <br/> |<span data-ttu-id="baf83-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="baf83-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="baf83-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="baf83-112">Area:</span></span>  <br/> |<span data-ttu-id="baf83-113">MAPI �A�h���X��</span><span class="sxs-lookup"><span data-stu-id="baf83-113">MAPI Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="baf83-114">解説</span><span class="sxs-lookup"><span data-stu-id="baf83-114">Remarks</span></span>

<span data-ttu-id="baf83-115">この値は、ネームサービスプロバイダインターフェイス (NSPI) サーバー上のすべてのアドレス帳オブジェクトに存在する必要があり、その識別名 (dn) は**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) の値と一致する必要があります。 dn は、dn 形式に従う必要があります。オブジェクトの種類に固有の仕様。</span><span class="sxs-lookup"><span data-stu-id="baf83-115">This value must be present for all address book objects on an Name Service Provider Interface (NSPI) server, its distinguished name (DN) must match the value for **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and its DN must follow the DN format specification particular to the type of object.</span></span> 
  
<span data-ttu-id="baf83-116">このプロパティは、オフラインアドレス帳のオブジェクトには存在しません。</span><span class="sxs-lookup"><span data-stu-id="baf83-116">This property is not present on objects in an offline address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="baf83-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="baf83-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="baf83-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="baf83-118">Protocol specifications</span></span>

<span data-ttu-id="baf83-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="baf83-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="baf83-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="baf83-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="baf83-121">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="baf83-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="baf83-122">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="baf83-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="baf83-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="baf83-123">Header files</span></span>

<span data-ttu-id="baf83-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="baf83-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="baf83-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="baf83-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="baf83-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="baf83-126">Mapitags.h</span></span>
  
> <span data-ttu-id="baf83-127">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="baf83-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="baf83-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="baf83-128">See also</span></span>



[<span data-ttu-id="baf83-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="baf83-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="baf83-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="baf83-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="baf83-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="baf83-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="baf83-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="baf83-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

