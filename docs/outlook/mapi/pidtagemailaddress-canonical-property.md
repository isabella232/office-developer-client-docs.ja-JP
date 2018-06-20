---
title: PidTagEmailAddress の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: cb8b7d0fca6b30f75bd35d1e4e48fa359100ad18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802716"
---
# <a name="pidtagemailaddress-canonical-property"></a><span data-ttu-id="8958c-103">PidTagEmailAddress の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="8958c-103">PidTagEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="8958c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8958c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8958c-105">メッセージング ユーザーの電子メール アドレスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8958c-105">Contains the messaging user's email address.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8958c-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="8958c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8958c-107">PR_EMAIL_ADDRESS、PR_EMAIL_ADDRESS_A、PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="8958c-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="8958c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8958c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8958c-109">0x3003</span><span class="sxs-lookup"><span data-stu-id="8958c-109">0x3003</span></span>  <br/> |
|<span data-ttu-id="8958c-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="8958c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8958c-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8958c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8958c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="8958c-112">Area:</span></span>  <br/> |<span data-ttu-id="8958c-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="8958c-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8958c-114">備考</span><span class="sxs-lookup"><span data-stu-id="8958c-114">Remarks</span></span>

<span data-ttu-id="8958c-115">これらのプロパティでは、すべてのメッセージング ユーザーのベース アドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="8958c-115">These properties are examples of the base address properties for all messaging users.</span></span> <span data-ttu-id="8958c-116">フォーマットが基になるメッセージング システムに対してのみ意味を持つ null で終わる文字列することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8958c-116">It is a null-terminated string whose format has meaning only for the underlying messaging system.</span></span> 
  
<span data-ttu-id="8958c-117">これらのプロパティは、 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) およびメッセージのアドレス指定で**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティと組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="8958c-117">These properties are used in conjunction with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) properties in addressing messages.</span></span> <span data-ttu-id="8958c-118">文字列の形式は、 **PR_ADDRTYPE**によって修飾されます。</span><span class="sxs-lookup"><span data-stu-id="8958c-118">The string format is qualified by **PR_ADDRTYPE**.</span></span> 
  
<span data-ttu-id="8958c-119">このプロパティの有効値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8958c-119">Valid values for this property include:</span></span> 
  
```cpp
network/postoffice/user 
Bruce@XYZZY.COM 
/c=US/a=att/p=Microsoft/o=Finance/ou=Purchasing/s=Furthur/g=Joe 
 
```

## <a name="related-resources"></a><span data-ttu-id="8958c-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8958c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8958c-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8958c-121">Protocol specifications</span></span>

<span data-ttu-id="8958c-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8958c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8958c-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8958c-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8958c-124">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8958c-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8958c-125">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8958c-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="8958c-126">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8958c-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8958c-127">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="8958c-127">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8958c-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8958c-128">Header files</span></span>

<span data-ttu-id="8958c-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8958c-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="8958c-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8958c-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="8958c-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8958c-131">Mapitags.h</span></span>
  
> <span data-ttu-id="8958c-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8958c-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8958c-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="8958c-133">See also</span></span>



[<span data-ttu-id="8958c-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8958c-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8958c-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8958c-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8958c-136">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="8958c-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8958c-137">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="8958c-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

