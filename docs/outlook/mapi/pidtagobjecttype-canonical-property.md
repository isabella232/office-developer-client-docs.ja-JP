---
title: PidTagObjectType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObjectType
api_type:
- HeaderDef
ms.assetid: 37da4ff5-300d-479f-a8b4-6fc36df997d9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b433db7cb157afbf8c3b506f2ed95b04b7b88564
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329226"
---
# <a name="pidtagobjecttype-canonical-property"></a><span data-ttu-id="6b3c8-103">PidTagObjectType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b3c8-103">PidTagObjectType Canonical Property</span></span>

  
  
<span data-ttu-id="6b3c8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b3c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b3c8-105">オブジェクトの種類を格納します。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-105">Contains the type of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b3c8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6b3c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6b3c8-107">PR_OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="6b3c8-107">PR_OBJECT_TYPE</span></span>  <br/> |
|<span data-ttu-id="6b3c8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6b3c8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6b3c8-109">0x0ffe</span><span class="sxs-lookup"><span data-stu-id="6b3c8-109">0x0FFE</span></span>  <br/> |
|<span data-ttu-id="6b3c8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6b3c8-110">Data type:</span></span>  <br/> |<span data-ttu-id="6b3c8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6b3c8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6b3c8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="6b3c8-112">Area:</span></span>  <br/> |<span data-ttu-id="6b3c8-113">共通</span><span class="sxs-lookup"><span data-stu-id="6b3c8-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b3c8-114">解説</span><span class="sxs-lookup"><span data-stu-id="6b3c8-114">Remarks</span></span>

<span data-ttu-id="6b3c8-115">このプロパティに含まれているオブジェクトの種類は、 **openentry**インターフェイスを介してアクセスできるオブジェクトで利用できるプライマリインターフェイスに対応しています。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-115">The object type contained in this property corresponds to the primary interface available for an object accessible through the **OpenEntry** interface.</span></span> <span data-ttu-id="6b3c8-116">通常は、適切な**openentry**メソッドによって返される_lpulobjtype_パラメーターを調べて取得します。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-116">It is usually obtained by consulting the  _lpulObjType_ parameter returned by the appropriate **OpenEntry** method.</span></span> <span data-ttu-id="6b3c8-117">インターフェイスが他の方法で取得された場合は、 [imapiprop:: GetProps](imapiprop-getprops.md)を呼び出してこのプロパティの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-117">When the interface is obtained in other ways, call [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the value for this property.</span></span> 
  
<span data-ttu-id="6b3c8-118">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-118">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="6b3c8-119">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="6b3c8-119">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="6b3c8-120">アドレス帳のコンテナーオブジェクト</span><span class="sxs-lookup"><span data-stu-id="6b3c8-120">Address book container object</span></span> 
    
<span data-ttu-id="6b3c8-121">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="6b3c8-121">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="6b3c8-122">アドレス帳オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6b3c8-122">Address book object</span></span> 
    
<span data-ttu-id="6b3c8-123">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="6b3c8-123">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="6b3c8-124">メッセージ添付オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6b3c8-124">Message attachment object</span></span> 
    
<span data-ttu-id="6b3c8-125">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="6b3c8-125">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="6b3c8-126">配布リストオブジェクト</span><span class="sxs-lookup"><span data-stu-id="6b3c8-126">Distribution list object</span></span> 
    
<span data-ttu-id="6b3c8-127">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="6b3c8-127">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="6b3c8-128">フォルダー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6b3c8-128">Folder object</span></span> 
    
<span data-ttu-id="6b3c8-129">MAPI_FORMINFO</span><span class="sxs-lookup"><span data-stu-id="6b3c8-129">MAPI_FORMINFO</span></span> 
  
> <span data-ttu-id="6b3c8-130">Form オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6b3c8-130">Form object</span></span> 
    
<span data-ttu-id="6b3c8-131">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="6b3c8-131">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="6b3c8-132">メッセージングユーザーオブジェクト</span><span class="sxs-lookup"><span data-stu-id="6b3c8-132">Messaging user object</span></span> 
    
<span data-ttu-id="6b3c8-133">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="6b3c8-133">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="6b3c8-134">Message オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6b3c8-134">Message object</span></span> 
    
<span data-ttu-id="6b3c8-135">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="6b3c8-135">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="6b3c8-136">Profile section オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6b3c8-136">Profile section object</span></span> 
    
<span data-ttu-id="6b3c8-137">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="6b3c8-137">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="6b3c8-138">Session オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6b3c8-138">Session object</span></span> 
    
<span data-ttu-id="6b3c8-139">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="6b3c8-139">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="6b3c8-140">Status オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6b3c8-140">Status object</span></span> 
    
<span data-ttu-id="6b3c8-141">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="6b3c8-141">MAPI_STORE</span></span> 
  
> <span data-ttu-id="6b3c8-142">メッセージストアオブジェクト</span><span class="sxs-lookup"><span data-stu-id="6b3c8-142">Message store object</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="6b3c8-143">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6b3c8-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6b3c8-144">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6b3c8-144">Protocol specifications</span></span>

<span data-ttu-id="6b3c8-145">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b3c8-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b3c8-146">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6b3c8-147">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b3c8-147">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b3c8-148">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-148">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="6b3c8-149">[[MS-CHAP]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b3c8-149">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b3c8-150">ネームサービスプロバイダインターフェイス (NSPI) サーバーとのクライアントの通信を処理します。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-150">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="6b3c8-151">[[OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b3c8-151">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b3c8-152">フォルダー操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-152">Handles folder operations.</span></span>
    
<span data-ttu-id="6b3c8-153">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b3c8-153">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b3c8-154">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-154">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="6b3c8-155">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b3c8-155">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b3c8-156">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-156">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="6b3c8-157">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b3c8-157">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b3c8-158">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-158">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6b3c8-159">[[OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b3c8-159">[[MS-OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b3c8-160">ローカルアドレス帳のオブジェクトキャッシュのオフラインアドレス帳 (OAB) ファイル形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-160">Specifies the offline address book (OAB) file formats for the local address book objects cache.</span></span>
    
<span data-ttu-id="6b3c8-161">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b3c8-161">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b3c8-162">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-162">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="6b3c8-163">[[OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b3c8-163">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b3c8-164">検索フォルダーリストの構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-164">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6b3c8-165">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="6b3c8-165">Header files</span></span>

<span data-ttu-id="6b3c8-166">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b3c8-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="6b3c8-167">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-167">Provides data type definitions.</span></span>
    
<span data-ttu-id="6b3c8-168">Mapitags</span><span class="sxs-lookup"><span data-stu-id="6b3c8-168">Mapitags.h</span></span>
  
> <span data-ttu-id="6b3c8-169">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6b3c8-169">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6b3c8-170">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b3c8-170">See also</span></span>



[<span data-ttu-id="6b3c8-171">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="6b3c8-171">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6b3c8-172">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b3c8-172">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6b3c8-173">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6b3c8-173">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6b3c8-174">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6b3c8-174">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

