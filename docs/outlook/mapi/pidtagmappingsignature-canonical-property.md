---
title: PidTagMappingSignature 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6017871b9567406af0898eede0d5659b468b3343
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581035"
---
# <a name="pidtagmappingsignature-canonical-property"></a><span data-ttu-id="119a5-103">PidTagMappingSignature 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="119a5-103">PidTagMappingSignature Canonical Property</span></span>

  
  
<span data-ttu-id="119a5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="119a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="119a5-105">特定の MAPI オブジェクトの名前付きプロパティのマッピングの署名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="119a5-105">Contains the mapping signature for named properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="119a5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="119a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="119a5-107">PR_MAPPING_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="119a5-107">PR_MAPPING_SIGNATURE</span></span>  <br/> |
|<span data-ttu-id="119a5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="119a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="119a5-109">0x0FF8</span><span class="sxs-lookup"><span data-stu-id="119a5-109">0x0FF8</span></span>  <br/> |
|<span data-ttu-id="119a5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="119a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="119a5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="119a5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="119a5-112">領域:</span><span class="sxs-lookup"><span data-stu-id="119a5-112">Area:</span></span>  <br/> |<span data-ttu-id="119a5-113">その他</span><span class="sxs-lookup"><span data-stu-id="119a5-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="119a5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="119a5-114">Remarks</span></span>

<span data-ttu-id="119a5-115">名前付きプロパティを持つオブジェクトがこのプロパティを公開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="119a5-115">It is recommended that objects having named properties expose this property.</span></span> <span data-ttu-id="119a5-116">という名前の別の 1 つのオブジェクトからプロパティをコピーするとき、クライアント アプリケーションは両方のオブジェクトの**PR_MAPPING_SIGNATURE**プロパティを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="119a5-116">A client application should check the **PR_MAPPING_SIGNATURE** property of both objects when copying named properties from one object to another.</span></span> <span data-ttu-id="119a5-117">このプロパティの使用方法は、コピーされたプロパティの名前と id の間の変換を最小限にできます。</span><span class="sxs-lookup"><span data-stu-id="119a5-117">Use of this property can minimize translating between copied properties' names and identifiers.</span></span> 
  
<span data-ttu-id="119a5-118">特定の MAPI オブジェクトのこのプロパティが存在しない場合、オブジェクトは、固有のマッピングが、独自の名前と識別子があります。</span><span class="sxs-lookup"><span data-stu-id="119a5-118">If this property does not exist for a given MAPI object, then the object has its own unique mapping of names and identifiers.</span></span> <span data-ttu-id="119a5-119">ここで、クライアントは、ソース オブジェクトとし、目的のオブジェクトの[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドで[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="119a5-119">In this case the client must call the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method on the source object and then the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method on the destination object.</span></span> 
  
<span data-ttu-id="119a5-120">2 つのオブジェクトは、同じ**PR_MAPPING_SIGNATURE**値を持つ、クライアントでは、識別子を名前に識別子の名前を変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="119a5-120">When two objects have the same **PR_MAPPING_SIGNATURE** value, the client does not need to translate name to identifier and identifier to name.</span></span> <span data-ttu-id="119a5-121">クライアントがメソッドを呼び出して[IMAPIProp::GetProps](imapiprop-getprops.md)ソースとし、 [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドで先にします。</span><span class="sxs-lookup"><span data-stu-id="119a5-121">The client can simply call the [IMAPIProp::GetProps](imapiprop-getprops.md) method on the source and then the [IMAPIProp::SetProps](imapiprop-setprops.md) method on the destination.</span></span> <span data-ttu-id="119a5-122">これは、名前付きプロパティは、ユーザー設定のコピーを実行するクライアント、およびプロバイダーは、 [IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドと[IMAPIProp::CopyProps](imapiprop-copyprops.md)メソッドを実装するには便利です。</span><span class="sxs-lookup"><span data-stu-id="119a5-122">This is convenient for clients that perform custom copying of named properties, and for providers implementing the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) methods.</span></span> 
  
<span data-ttu-id="119a5-123">名前付きプロパティとの名前と識別子のマッピングの詳細については、 [MAPI 名前付きプロパティ](mapi-named-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="119a5-123">For more information on named properties and mapping of names and identifiers, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="119a5-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="119a5-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="119a5-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="119a5-125">Protocol specifications</span></span>

<span data-ttu-id="119a5-126">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="119a5-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="119a5-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="119a5-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="119a5-128">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="119a5-128">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="119a5-129">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="119a5-129">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="119a5-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="119a5-130">Header files</span></span>

<span data-ttu-id="119a5-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="119a5-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="119a5-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="119a5-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="119a5-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="119a5-133">Mapitags.h</span></span>
  
> <span data-ttu-id="119a5-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="119a5-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="119a5-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="119a5-135">See also</span></span>



[<span data-ttu-id="119a5-136">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="119a5-136">MAPINAMEID</span></span>](mapinameid.md)


[<span data-ttu-id="119a5-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="119a5-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="119a5-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="119a5-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="119a5-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="119a5-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="119a5-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="119a5-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

