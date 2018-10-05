---
title: PidTagDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayName
api_type:
- HeaderDef
ms.assetid: bd094e00-5c60-4bb3-9a45-b943fab52876
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 834141fe3e57fde5e6404776e0ad5ce3b438450e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386419"
---
# <a name="pidtagdisplayname-canonical-property"></a><span data-ttu-id="a2ec3-103">PidTagDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a2ec3-103">PidTagDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="a2ec3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2ec3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2ec3-105">特定の MAPI オブジェクトの表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-105">Contains the display name for a given MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2ec3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a2ec3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a2ec3-107">PR_DISPLAY_NAME、PR_DISPLAY_NAME_A、PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="a2ec3-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="a2ec3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a2ec3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a2ec3-109">0x3001</span><span class="sxs-lookup"><span data-stu-id="a2ec3-109">0x3001</span></span>  <br/> |
|<span data-ttu-id="a2ec3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a2ec3-110">Data type:</span></span>  <br/> |<span data-ttu-id="a2ec3-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a2ec3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a2ec3-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a2ec3-112">Area:</span></span>  <br/> |<span data-ttu-id="a2ec3-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="a2ec3-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2ec3-114">備考</span><span class="sxs-lookup"><span data-stu-id="a2ec3-114">Remarks</span></span>

<span data-ttu-id="a2ec3-115">フォルダーには、一意の表示名を持つ兄弟のサブフォルダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-115">Folders require sibling subfolders to have unique display names.</span></span> <span data-ttu-id="a2ec3-116">などのフォルダーに 2 つのサブフォルダーが含まれている場合 2 つのサブフォルダーが同じ値をこのプロパティに使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-116">For example, if a folder contains two subfolders, the two subfolders cannot use the same value for this property.</span></span> <span data-ttu-id="a2ec3-117">この制限は、アドレス帳および配布リストなど、他のコンテナーには適用されません。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-117">This restriction does not apply to other containers, such as address books and distribution lists.</span></span> 
  
<span data-ttu-id="a2ec3-118">サービス プロバイダーは、プロバイダーの種類と構成の情報が含まれるように、このプロパティの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-118">Service providers should set the value of this property so that it contains both the provider type and configuration information.</span></span> <span data-ttu-id="a2ec3-119">その他の情報は、同じ種類のプロバイダーのインスタンスを区別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-119">The additional information helps to distinguish between instances of providers of the same type.</span></span> <span data-ttu-id="a2ec3-120">未構成のプロバイダーは、プロバイダーの名前を示す文字列を使用してください。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-120">Unconfigured providers should use a string that names the provider.</span></span> <span data-ttu-id="a2ec3-121">構成済みのプロバイダーでは、かっこで囲まれた識別用の文字列の後に同じ文字列を使用してください。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-121">Configured providers should use the same string followed by a distinguishing string in parentheses.</span></span> <span data-ttu-id="a2ec3-122">などの構成解除状態のメッセージ ストア プロバイダーはこれらのプロパティを設定可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-122">For example, an unconfigured message store provider might set these properties to:</span></span> 
  
<span data-ttu-id="a2ec3-123">個人用インフォメーション ストア</span><span class="sxs-lookup"><span data-stu-id="a2ec3-123">Personal Information Store</span></span>
  
<span data-ttu-id="a2ec3-124">構成済みのバージョンこれらのプロパティを設定し、でした。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-124">The configured version could then set these properties to:</span></span> 
  
<span data-ttu-id="a2ec3-125">個人用インフォメーション ストア (1998 年 2 月 6 日)</span><span class="sxs-lookup"><span data-stu-id="a2ec3-125">Personal Information Store (February 6, 1998)</span></span>
  
<span data-ttu-id="a2ec3-126">状態のオブジェクトに対してこれらのプロパティには、ユーザー インターフェイスで表示可能なコンポーネントの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-126">For status objects, these properties contain the name of the component that can be displayed by the user interface.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a2ec3-127">MAPI メッセージの受信者の名前には、セミコロンを使用できません。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-127">Semicolons cannot be used within recipient names in MAPI messaging.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a2ec3-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a2ec3-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a2ec3-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a2ec3-129">Protocol specifications</span></span>

<span data-ttu-id="a2ec3-130">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2ec3-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2ec3-131">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a2ec3-132">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2ec3-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2ec3-133">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="a2ec3-134">[[MS OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2ec3-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2ec3-135">フォルダーの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-135">Handles folder operations.</span></span>
    
<span data-ttu-id="a2ec3-136">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2ec3-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2ec3-137">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="a2ec3-138">[[MS OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2ec3-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2ec3-139">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="a2ec3-140">[[MS OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2ec3-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2ec3-141">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-141">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="a2ec3-142">[[MS XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2ec3-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2ec3-143">要求し、WebDAV メソッドを使用して Exchange のセキュリティ記述子を設定する方法を指定する WebDAV プロトコルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-143">Extends the WebDAV protocol that specifies how to request and set the Exchange security descriptor via WebDAV methods.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a2ec3-144">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a2ec3-144">Header files</span></span>

<span data-ttu-id="a2ec3-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a2ec3-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="a2ec3-146">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="a2ec3-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a2ec3-147">Mapitags.h</span></span>
  
> <span data-ttu-id="a2ec3-148">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a2ec3-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2ec3-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="a2ec3-149">See also</span></span>



[<span data-ttu-id="a2ec3-150">PidTagTransmittableDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a2ec3-150">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="a2ec3-151">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a2ec3-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a2ec3-152">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a2ec3-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a2ec3-153">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a2ec3-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a2ec3-154">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a2ec3-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

