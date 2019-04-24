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
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342548"
---
# <a name="pidtagmappingsignature-canonical-property"></a><span data-ttu-id="de797-103">PidTagMappingSignature 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="de797-103">PidTagMappingSignature Canonical Property</span></span>

  
  
<span data-ttu-id="de797-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de797-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de797-105">特定の MAPI オブジェクトの名前付きプロパティのマッピングシグネチャが含まれています。</span><span class="sxs-lookup"><span data-stu-id="de797-105">Contains the mapping signature for named properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de797-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="de797-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de797-107">PR_MAPPING_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="de797-107">PR_MAPPING_SIGNATURE</span></span>  <br/> |
|<span data-ttu-id="de797-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="de797-108">Identifier:</span></span>  <br/> |<span data-ttu-id="de797-109">0x0ff8</span><span class="sxs-lookup"><span data-stu-id="de797-109">0x0FF8</span></span>  <br/> |
|<span data-ttu-id="de797-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="de797-110">Data type:</span></span>  <br/> |<span data-ttu-id="de797-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="de797-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="de797-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="de797-112">Area:</span></span>  <br/> |<span data-ttu-id="de797-113">その他</span><span class="sxs-lookup"><span data-stu-id="de797-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de797-114">解説</span><span class="sxs-lookup"><span data-stu-id="de797-114">Remarks</span></span>

<span data-ttu-id="de797-115">名前付きプロパティを持つオブジェクトは、このプロパティを公開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="de797-115">It is recommended that objects having named properties expose this property.</span></span> <span data-ttu-id="de797-116">クライアントアプリケーションは、あるオブジェクトから別のオブジェクトに名前付きプロパティをコピーするときに、両方のオブジェクトの**PR_MAPPING_SIGNATURE**プロパティをチェックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="de797-116">A client application should check the **PR_MAPPING_SIGNATURE** property of both objects when copying named properties from one object to another.</span></span> <span data-ttu-id="de797-117">このプロパティを使用すると、コピーされたプロパティの名前と識別子の間の変換を最小限に抑えることができます。</span><span class="sxs-lookup"><span data-stu-id="de797-117">Use of this property can minimize translating between copied properties' names and identifiers.</span></span> 
  
<span data-ttu-id="de797-118">指定した MAPI オブジェクトに対してこのプロパティが存在しない場合、オブジェクトには名前と識別子の固有のマッピングがあります。</span><span class="sxs-lookup"><span data-stu-id="de797-118">If this property does not exist for a given MAPI object, then the object has its own unique mapping of names and identifiers.</span></span> <span data-ttu-id="de797-119">この場合、クライアントは、ソースオブジェクトに対して[imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドを呼び出してから、宛先オブジェクトの[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="de797-119">In this case the client must call the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method on the source object and then the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method on the destination object.</span></span> 
  
<span data-ttu-id="de797-120">2つのオブジェクトの**PR_MAPPING_SIGNATURE**値が同じである場合、クライアントは名前を識別子と識別子に変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="de797-120">When two objects have the same **PR_MAPPING_SIGNATURE** value, the client does not need to translate name to identifier and identifier to name.</span></span> <span data-ttu-id="de797-121">クライアントは単に、ソースで[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出すことができます。その後、宛先の[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="de797-121">The client can simply call the [IMAPIProp::GetProps](imapiprop-getprops.md) method on the source and then the [IMAPIProp::SetProps](imapiprop-setprops.md) method on the destination.</span></span> <span data-ttu-id="de797-122">これは、名前付きプロパティのカスタムコピーを実行するクライアント、および[imapiprop:: CopyTo](imapiprop-copyto.md)および[imapiprop:: copyprops](imapiprop-copyprops.md)メソッドを実装しているプロバイダーにとって便利です。</span><span class="sxs-lookup"><span data-stu-id="de797-122">This is convenient for clients that perform custom copying of named properties, and for providers implementing the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) methods.</span></span> 
  
<span data-ttu-id="de797-123">名前付きプロパティと名前と識別子のマッピングの詳細については、「 [MAPI の名前付きプロパティ](mapi-named-properties.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de797-123">For more information on named properties and mapping of names and identifiers, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="de797-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="de797-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de797-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="de797-125">Protocol specifications</span></span>

<span data-ttu-id="de797-126">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de797-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de797-127">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="de797-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="de797-128">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de797-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de797-129">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="de797-129">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="de797-130">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="de797-130">Header files</span></span>

<span data-ttu-id="de797-131">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de797-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="de797-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="de797-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="de797-133">Mapitags</span><span class="sxs-lookup"><span data-stu-id="de797-133">Mapitags.h</span></span>
  
> <span data-ttu-id="de797-134">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="de797-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de797-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="de797-135">See also</span></span>



[<span data-ttu-id="de797-136">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="de797-136">MAPINAMEID</span></span>](mapinameid.md)


[<span data-ttu-id="de797-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="de797-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de797-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="de797-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de797-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="de797-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de797-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="de797-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

