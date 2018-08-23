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
ms.openlocfilehash: f95b97fc4150695c77871f8c4f768f6b5488ceb4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572462"
---
# <a name="pidtagtemplateid-canonical-property"></a><span data-ttu-id="0870a-103">PidTagTemplateid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0870a-103">PidTagTemplateid Canonical Property</span></span>

  
  
<span data-ttu-id="0870a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0870a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0870a-105">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、永続的なエントリ ID の形式で表されますが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0870a-105">Contains the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), expressed as a permanent entry ID format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0870a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0870a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0870a-107">PR_TEMPLATEID</span><span class="sxs-lookup"><span data-stu-id="0870a-107">PR_TEMPLATEID</span></span>  <br/> |
|<span data-ttu-id="0870a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0870a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0870a-109">0x3902</span><span class="sxs-lookup"><span data-stu-id="0870a-109">0x3902</span></span>  <br/> |
|<span data-ttu-id="0870a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0870a-110">Data type:</span></span>  <br/> |<span data-ttu-id="0870a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0870a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0870a-112">領域:</span><span class="sxs-lookup"><span data-stu-id="0870a-112">Area:</span></span>  <br/> |<span data-ttu-id="0870a-113">MAPI �A�h���X��</span><span class="sxs-lookup"><span data-stu-id="0870a-113">MAPI Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0870a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="0870a-114">Remarks</span></span>

<span data-ttu-id="0870a-115">この値は、ネーム サービス プロバイダー インターフェイス (NSPI) サーバー上のすべてのアドレス帳オブジェクトのために存在する必要があります。、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) の値に一致する必要があります。、識別名 (DN) およびその識別名が DN の形式に従う必要があります。仕様のオブジェクトの種類を特定します。</span><span class="sxs-lookup"><span data-stu-id="0870a-115">This value must be present for all address book objects on an Name Service Provider Interface (NSPI) server, its distinguished name (DN) must match the value for **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and its DN must follow the DN format specification particular to the type of object.</span></span> 
  
<span data-ttu-id="0870a-116">このプロパティは、オフライン アドレス帳内のオブジェクトに存在しません。</span><span class="sxs-lookup"><span data-stu-id="0870a-116">This property is not present on objects in an offline address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0870a-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0870a-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0870a-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0870a-118">Protocol specifications</span></span>

<span data-ttu-id="0870a-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0870a-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0870a-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0870a-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0870a-121">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0870a-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0870a-122">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0870a-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0870a-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0870a-123">Header files</span></span>

<span data-ttu-id="0870a-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0870a-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="0870a-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0870a-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="0870a-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0870a-126">Mapitags.h</span></span>
  
> <span data-ttu-id="0870a-127">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0870a-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0870a-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="0870a-128">See also</span></span>



[<span data-ttu-id="0870a-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0870a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0870a-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0870a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0870a-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0870a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0870a-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0870a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

