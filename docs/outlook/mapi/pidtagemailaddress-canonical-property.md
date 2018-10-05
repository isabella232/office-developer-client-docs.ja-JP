---
title: PidTagEmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmailAddress
api_type:
- HeaderDef
ms.assetid: bbd1e187-172e-4612-9efe-7c8e52967dfe
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: efcb72d872836adce544f3a90cf093de1f3713a7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393881"
---
# <a name="pidtagemailaddress-canonical-property"></a><span data-ttu-id="6ab61-103">PidTagEmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6ab61-103">PidTagEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="6ab61-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ab61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ab61-105">メッセージング ユーザーの電子メール アドレスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6ab61-105">Contains the messaging user's email address.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ab61-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6ab61-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ab61-107">PR_EMAIL_ADDRESS、PR_EMAIL_ADDRESS_A、PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="6ab61-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="6ab61-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6ab61-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6ab61-109">0x3003</span><span class="sxs-lookup"><span data-stu-id="6ab61-109">0x3003</span></span>  <br/> |
|<span data-ttu-id="6ab61-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6ab61-110">Data type:</span></span>  <br/> |<span data-ttu-id="6ab61-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6ab61-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6ab61-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="6ab61-112">Area:</span></span>  <br/> |<span data-ttu-id="6ab61-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="6ab61-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ab61-114">備考</span><span class="sxs-lookup"><span data-stu-id="6ab61-114">Remarks</span></span>

<span data-ttu-id="6ab61-115">これらのプロパティでは、すべてのメッセージング ユーザーのベース アドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="6ab61-115">These properties are examples of the base address properties for all messaging users.</span></span> <span data-ttu-id="6ab61-116">フォーマットが基になるメッセージング システムに対してのみ意味を持つ null で終わる文字列することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6ab61-116">It is a null-terminated string whose format has meaning only for the underlying messaging system.</span></span> 
  
<span data-ttu-id="6ab61-117">これらのプロパティは、 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) およびメッセージのアドレス指定で**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティと組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="6ab61-117">These properties are used in conjunction with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) properties in addressing messages.</span></span> <span data-ttu-id="6ab61-118">文字列の形式は、 **PR_ADDRTYPE**によって修飾されます。</span><span class="sxs-lookup"><span data-stu-id="6ab61-118">The string format is qualified by **PR_ADDRTYPE**.</span></span> 
  
<span data-ttu-id="6ab61-119">このプロパティの有効値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6ab61-119">Valid values for this property include:</span></span> 
  
```cpp
network/postoffice/user 
Bruce@XYZZY.COM 
/c=US/a=att/p=Microsoft/o=Finance/ou=Purchasing/s=Furthur/g=Joe 
 
```

## <a name="related-resources"></a><span data-ttu-id="6ab61-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6ab61-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ab61-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6ab61-121">Protocol specifications</span></span>

<span data-ttu-id="6ab61-122">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ab61-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ab61-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6ab61-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6ab61-124">[[MS OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ab61-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ab61-125">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ab61-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="6ab61-126">[[MS OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ab61-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ab61-127">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="6ab61-127">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6ab61-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6ab61-128">Header files</span></span>

<span data-ttu-id="6ab61-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ab61-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ab61-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6ab61-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="6ab61-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6ab61-131">Mapitags.h</span></span>
  
> <span data-ttu-id="6ab61-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6ab61-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ab61-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="6ab61-133">See also</span></span>



[<span data-ttu-id="6ab61-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6ab61-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ab61-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6ab61-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ab61-136">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6ab61-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ab61-137">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6ab61-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

