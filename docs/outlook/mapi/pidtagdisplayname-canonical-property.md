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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 834141fe3e57fde5e6404776e0ad5ce3b438450e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360803"
---
# <a name="pidtagdisplayname-canonical-property"></a><span data-ttu-id="0bbeb-103">PidTagDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0bbeb-103">PidTagDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="0bbeb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0bbeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0bbeb-105">特定の MAPI オブジェクトの表示名を格納します。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-105">Contains the display name for a given MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0bbeb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0bbeb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0bbeb-107">PR_DISPLAY_NAME、PR_DISPLAY_NAME_A、PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="0bbeb-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="0bbeb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0bbeb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0bbeb-109">0x3001</span><span class="sxs-lookup"><span data-stu-id="0bbeb-109">0x3001</span></span>  <br/> |
|<span data-ttu-id="0bbeb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0bbeb-110">Data type:</span></span>  <br/> |<span data-ttu-id="0bbeb-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0bbeb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0bbeb-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="0bbeb-112">Area:</span></span>  <br/> |<span data-ttu-id="0bbeb-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="0bbeb-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bbeb-114">注釈</span><span class="sxs-lookup"><span data-stu-id="0bbeb-114">Remarks</span></span>

<span data-ttu-id="0bbeb-115">フォルダーには、一意の表示名を持つ兄弟サブフォルダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-115">Folders require sibling subfolders to have unique display names.</span></span> <span data-ttu-id="0bbeb-116">たとえば、フォルダーに 2 つのサブフォルダーが含まれている場合、2 つのサブフォルダーでは、このプロパティに同じ値を使用できません。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-116">For example, if a folder contains two subfolders, the two subfolders cannot use the same value for this property.</span></span> <span data-ttu-id="0bbeb-117">この制限は、アドレス帳や配布リストなどの他のコンテナーには適用されません。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-117">This restriction does not apply to other containers, such as address books and distribution lists.</span></span> 
  
<span data-ttu-id="0bbeb-118">サービス プロバイダーは、プロバイダーの種類と構成情報の両方を含むこのプロパティの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-118">Service providers should set the value of this property so that it contains both the provider type and configuration information.</span></span> <span data-ttu-id="0bbeb-119">追加情報は、同じ種類のプロバイダーのインスタンスを区別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-119">The additional information helps to distinguish between instances of providers of the same type.</span></span> <span data-ttu-id="0bbeb-120">構成されていないプロバイダーは、プロバイダーの名前を示す文字列を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-120">Unconfigured providers should use a string that names the provider.</span></span> <span data-ttu-id="0bbeb-121">構成済みのプロバイダーは、同じ文字列を使用し、その後にかっこで囲まれた識別文字列を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-121">Configured providers should use the same string followed by a distinguishing string in parentheses.</span></span> <span data-ttu-id="0bbeb-122">たとえば、構成されていないメッセージ ストア プロバイダーは、次のプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-122">For example, an unconfigured message store provider might set these properties to:</span></span> 
  
<span data-ttu-id="0bbeb-123">個人情報ストア</span><span class="sxs-lookup"><span data-stu-id="0bbeb-123">Personal Information Store</span></span>
  
<span data-ttu-id="0bbeb-124">構成済みのバージョンでは、次のプロパティを次のように設定できます。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-124">The configured version could then set these properties to:</span></span> 
  
<span data-ttu-id="0bbeb-125">個人情報ストア (1998 年 2 月 6 日)</span><span class="sxs-lookup"><span data-stu-id="0bbeb-125">Personal Information Store (February 6, 1998)</span></span>
  
<span data-ttu-id="0bbeb-126">状態オブジェクトの場合、これらのプロパティには、ユーザー インターフェイスで表示できるコンポーネントの名前が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-126">For status objects, these properties contain the name of the component that can be displayed by the user interface.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0bbeb-127">MAPI メッセージングでは、受信者名内でセミコロンを使用できません。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-127">Semicolons cannot be used within recipient names in MAPI messaging.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0bbeb-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0bbeb-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0bbeb-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0bbeb-129">Protocol specifications</span></span>

<span data-ttu-id="0bbeb-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bbeb-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bbeb-131">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0bbeb-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bbeb-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bbeb-133">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="0bbeb-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bbeb-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bbeb-135">フォルダー操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-135">Handles folder operations.</span></span>
    
<span data-ttu-id="0bbeb-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bbeb-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bbeb-137">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="0bbeb-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bbeb-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bbeb-139">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="0bbeb-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bbeb-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bbeb-141">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-141">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="0bbeb-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bbeb-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bbeb-143">WebDAV メソッドを使用してセキュリティ記述子を要求および設定する方法Exchange WebDAV プロトコルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-143">Extends the WebDAV protocol that specifies how to request and set the Exchange security descriptor via WebDAV methods.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0bbeb-144">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0bbeb-144">Header files</span></span>

<span data-ttu-id="0bbeb-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0bbeb-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="0bbeb-146">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="0bbeb-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0bbeb-147">Mapitags.h</span></span>
  
> <span data-ttu-id="0bbeb-148">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="0bbeb-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0bbeb-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="0bbeb-149">See also</span></span>



[<span data-ttu-id="0bbeb-150">PidTagTransmittableDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0bbeb-150">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="0bbeb-151">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0bbeb-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0bbeb-152">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0bbeb-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0bbeb-153">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="0bbeb-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0bbeb-154">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="0bbeb-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

