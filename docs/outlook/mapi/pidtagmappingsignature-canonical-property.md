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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342548"
---
# <a name="pidtagmappingsignature-canonical-property"></a><span data-ttu-id="e9652-103">PidTagMappingSignature 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9652-103">PidTagMappingSignature Canonical Property</span></span>

  
  
<span data-ttu-id="e9652-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9652-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9652-105">特定の MAPI オブジェクトの名前付きプロパティのマッピング署名を格納します。</span><span class="sxs-lookup"><span data-stu-id="e9652-105">Contains the mapping signature for named properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9652-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e9652-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9652-107">PR_MAPPING_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="e9652-107">PR_MAPPING_SIGNATURE</span></span>  <br/> |
|<span data-ttu-id="e9652-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e9652-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9652-109">0x0FF8</span><span class="sxs-lookup"><span data-stu-id="e9652-109">0x0FF8</span></span>  <br/> |
|<span data-ttu-id="e9652-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e9652-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9652-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e9652-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e9652-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e9652-112">Area:</span></span>  <br/> |<span data-ttu-id="e9652-113">その他</span><span class="sxs-lookup"><span data-stu-id="e9652-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9652-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e9652-114">Remarks</span></span>

<span data-ttu-id="e9652-115">名前付きプロパティを持つオブジェクトは、このプロパティを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9652-115">It is recommended that objects having named properties expose this property.</span></span> <span data-ttu-id="e9652-116">クライアント アプリケーションは、1 つの **オブジェクトから別** PR_MAPPING_SIGNATUREに名前付きプロパティをコピーするときに、両方のオブジェクトのプロパティをチェックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9652-116">A client application should check the **PR_MAPPING_SIGNATURE** property of both objects when copying named properties from one object to another.</span></span> <span data-ttu-id="e9652-117">このプロパティを使用すると、コピーされたプロパティの名前と識別子の変換を最小限に抑える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e9652-117">Use of this property can minimize translating between copied properties' names and identifiers.</span></span> 
  
<span data-ttu-id="e9652-118">特定の MAPI オブジェクトに対してこのプロパティが存在しない場合、オブジェクトには、名前と識別子の独自のマッピングがあります。</span><span class="sxs-lookup"><span data-stu-id="e9652-118">If this property does not exist for a given MAPI object, then the object has its own unique mapping of names and identifiers.</span></span> <span data-ttu-id="e9652-119">この場合、クライアントはソース オブジェクトの [IMAPIProp:::GetNamesFromIDs](imapiprop-getnamesfromids.md) メソッドを呼び出し、次に移行先オブジェクトの [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9652-119">In this case the client must call the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method on the source object and then the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method on the destination object.</span></span> 
  
<span data-ttu-id="e9652-120">2 つのオブジェクトの値 **PR_MAPPING_SIGNATURE、クライアント** は名前を識別子と識別子に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9652-120">When two objects have the same **PR_MAPPING_SIGNATURE** value, the client does not need to translate name to identifier and identifier to name.</span></span> <span data-ttu-id="e9652-121">クライアントは、ソースで [IMAPIProp:::GetProps](imapiprop-getprops.md) メソッドを呼び出し、次に宛先の [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出すだけでできます。</span><span class="sxs-lookup"><span data-stu-id="e9652-121">The client can simply call the [IMAPIProp::GetProps](imapiprop-getprops.md) method on the source and then the [IMAPIProp::SetProps](imapiprop-setprops.md) method on the destination.</span></span> <span data-ttu-id="e9652-122">これは、名前付きプロパティのカスタム コピーを実行するクライアントや [、IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドと [IMAPIProp::CopyProps](imapiprop-copyprops.md) メソッドを実装するプロバイダーに便利です。</span><span class="sxs-lookup"><span data-stu-id="e9652-122">This is convenient for clients that perform custom copying of named properties, and for providers implementing the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) methods.</span></span> 
  
<span data-ttu-id="e9652-123">名前付きプロパティと名前と識別子のマッピングの詳細については、「MAPI 名前付きプロパティ [」を参照してください](mapi-named-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="e9652-123">For more information on named properties and mapping of names and identifiers, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e9652-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e9652-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9652-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e9652-125">Protocol specifications</span></span>

<span data-ttu-id="e9652-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9652-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9652-127">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="e9652-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e9652-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9652-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9652-129">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e9652-129">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9652-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e9652-130">Header files</span></span>

<span data-ttu-id="e9652-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9652-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9652-132">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e9652-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9652-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e9652-133">Mapitags.h</span></span>
  
> <span data-ttu-id="e9652-134">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="e9652-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9652-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9652-135">See also</span></span>



[<span data-ttu-id="e9652-136">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="e9652-136">MAPINAMEID</span></span>](mapinameid.md)


[<span data-ttu-id="e9652-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e9652-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9652-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9652-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9652-139">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e9652-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9652-140">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e9652-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

