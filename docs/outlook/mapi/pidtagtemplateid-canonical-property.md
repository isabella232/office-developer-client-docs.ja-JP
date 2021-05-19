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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 96bcd15606771bd112568ad94133507ab14b2bcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358822"
---
# <a name="pidtagtemplateid-canonical-property"></a><span data-ttu-id="4037f-103">PidTagTemplateid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4037f-103">PidTagTemplateid Canonical Property</span></span>

  
  
<span data-ttu-id="4037f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4037f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4037f-105">永続的なエントリ **ID PR_ENTRYID** 形式で表される文字列 [(PidTagEntryId)](pidtagentryid-canonical-property.md)が含まれる。</span><span class="sxs-lookup"><span data-stu-id="4037f-105">Contains the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), expressed as a permanent entry ID format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4037f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4037f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4037f-107">PR_TEMPLATEID</span><span class="sxs-lookup"><span data-stu-id="4037f-107">PR_TEMPLATEID</span></span>  <br/> |
|<span data-ttu-id="4037f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4037f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4037f-109">0x3902</span><span class="sxs-lookup"><span data-stu-id="4037f-109">0x3902</span></span>  <br/> |
|<span data-ttu-id="4037f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4037f-110">Data type:</span></span>  <br/> |<span data-ttu-id="4037f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4037f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4037f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="4037f-112">Area:</span></span>  <br/> |<span data-ttu-id="4037f-113">MAPI �A�h���X��</span><span class="sxs-lookup"><span data-stu-id="4037f-113">MAPI Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4037f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4037f-114">Remarks</span></span>

<span data-ttu-id="4037f-115">この値は、ネーム サービス プロバイダー インターフェイス (NSPI) サーバー上のすべてのアドレス帳オブジェクトに対して存在する必要があります。識別名 (DN) は **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) の値と一致する必要があります。その DN はオブジェクトの種類に特定の DN 形式の仕様に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="4037f-115">This value must be present for all address book objects on an Name Service Provider Interface (NSPI) server, its distinguished name (DN) must match the value for **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and its DN must follow the DN format specification particular to the type of object.</span></span> 
  
<span data-ttu-id="4037f-116">このプロパティは、オフライン アドレス帳内のオブジェクトには存在しません。</span><span class="sxs-lookup"><span data-stu-id="4037f-116">This property is not present on objects in an offline address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4037f-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4037f-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4037f-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4037f-118">Protocol specifications</span></span>

<span data-ttu-id="4037f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4037f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4037f-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="4037f-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4037f-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4037f-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4037f-122">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4037f-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4037f-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4037f-123">Header files</span></span>

<span data-ttu-id="4037f-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4037f-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4037f-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4037f-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4037f-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4037f-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4037f-127">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="4037f-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4037f-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="4037f-128">See also</span></span>



[<span data-ttu-id="4037f-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="4037f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4037f-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4037f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4037f-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="4037f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4037f-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="4037f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

