---
title: PidTagObjectType の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2830da6aad561045a7ecdd953286c90edea88ca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803030"
---
# <a name="pidtagobjecttype-canonical-property"></a><span data-ttu-id="15a17-103">PidTagObjectType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="15a17-103">PidTagObjectType Canonical Property</span></span>

  
  
<span data-ttu-id="15a17-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="15a17-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15a17-105">オブジェクトの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="15a17-105">Contains the type of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15a17-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="15a17-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15a17-107">PR_OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="15a17-107">PR_OBJECT_TYPE</span></span>  <br/> |
|<span data-ttu-id="15a17-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="15a17-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15a17-109">0x0FFE</span><span class="sxs-lookup"><span data-stu-id="15a17-109">0x0FFE</span></span>  <br/> |
|<span data-ttu-id="15a17-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="15a17-110">Data type:</span></span>  <br/> |<span data-ttu-id="15a17-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="15a17-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="15a17-112">領域:</span><span class="sxs-lookup"><span data-stu-id="15a17-112">Area:</span></span>  <br/> |<span data-ttu-id="15a17-113">Common</span><span class="sxs-lookup"><span data-stu-id="15a17-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15a17-114">備考</span><span class="sxs-lookup"><span data-stu-id="15a17-114">Remarks</span></span>

<span data-ttu-id="15a17-115">**OpenEntry**インタ フェースを介してアクセス可能なオブジェクトで使用できる主要なインターフェイスに、このプロパティに含まれているオブジェクトの種類に対応しています。</span><span class="sxs-lookup"><span data-stu-id="15a17-115">The object type contained in this property corresponds to the primary interface available for an object accessible through the **OpenEntry** interface.</span></span> <span data-ttu-id="15a17-116">通常は、適切な**OpenEntry**メソッドによって返される_lpulObjType_パラメーターを参照して取得されます。</span><span class="sxs-lookup"><span data-stu-id="15a17-116">It is usually obtained by consulting the  _lpulObjType_ parameter returned by the appropriate **OpenEntry** method.</span></span> <span data-ttu-id="15a17-117">インタ フェースの他の方法で取得するときは、このプロパティの値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="15a17-117">When the interface is obtained in other ways, call [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the value for this property.</span></span> 
  
<span data-ttu-id="15a17-118">このプロパティは、次の値の 1 つだけ持つことができます。</span><span class="sxs-lookup"><span data-stu-id="15a17-118">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="15a17-119">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="15a17-119">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="15a17-120">アドレス帳コンテナー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="15a17-120">Address book container object</span></span> 
    
<span data-ttu-id="15a17-121">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="15a17-121">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="15a17-122">アドレス帳オブジェクト</span><span class="sxs-lookup"><span data-stu-id="15a17-122">Address book object</span></span> 
    
<span data-ttu-id="15a17-123">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="15a17-123">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="15a17-124">メッセージの添付ファイルのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="15a17-124">Message attachment object</span></span> 
    
<span data-ttu-id="15a17-125">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="15a17-125">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="15a17-126">配布リスト オブジェクト</span><span class="sxs-lookup"><span data-stu-id="15a17-126">Distribution list object</span></span> 
    
<span data-ttu-id="15a17-127">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="15a17-127">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="15a17-128">フォルダー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="15a17-128">Folder object</span></span> 
    
<span data-ttu-id="15a17-129">MAPI_FORMINFO</span><span class="sxs-lookup"><span data-stu-id="15a17-129">MAPI_FORMINFO</span></span> 
  
> <span data-ttu-id="15a17-130">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="15a17-130">Form object</span></span> 
    
<span data-ttu-id="15a17-131">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="15a17-131">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="15a17-132">メッセージングのユーザー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="15a17-132">Messaging user object</span></span> 
    
<span data-ttu-id="15a17-133">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="15a17-133">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="15a17-134">Message オブジェクト</span><span class="sxs-lookup"><span data-stu-id="15a17-134">Message object</span></span> 
    
<span data-ttu-id="15a17-135">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="15a17-135">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="15a17-136">プロファイル セクションのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="15a17-136">Profile section object</span></span> 
    
<span data-ttu-id="15a17-137">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="15a17-137">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="15a17-138">セッション オブジェクト</span><span class="sxs-lookup"><span data-stu-id="15a17-138">Session object</span></span> 
    
<span data-ttu-id="15a17-139">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="15a17-139">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="15a17-140">ステータス オブジェクト</span><span class="sxs-lookup"><span data-stu-id="15a17-140">Status object</span></span> 
    
<span data-ttu-id="15a17-141">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="15a17-141">MAPI_STORE</span></span> 
  
> <span data-ttu-id="15a17-142">メッセージ ストアのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="15a17-142">Message store object</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="15a17-143">関連リソース</span><span class="sxs-lookup"><span data-stu-id="15a17-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15a17-144">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="15a17-144">Protocol specifications</span></span>

<span data-ttu-id="15a17-145">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15a17-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15a17-146">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="15a17-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="15a17-147">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15a17-147">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15a17-148">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="15a17-148">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="15a17-149">[[MS NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15a17-149">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15a17-150">ネーム サービス プロバイダー インターフェイス (NSPI) サーバーとクライアントの通信を処理します。</span><span class="sxs-lookup"><span data-stu-id="15a17-150">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="15a17-151">[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15a17-151">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15a17-152">フォルダーの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="15a17-152">Handles folder operations.</span></span>
    
<span data-ttu-id="15a17-153">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15a17-153">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15a17-154">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="15a17-154">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="15a17-155">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15a17-155">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15a17-156">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="15a17-156">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="15a17-157">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15a17-157">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15a17-158">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="15a17-158">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="15a17-159">[[MS OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15a17-159">[[MS-OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15a17-160">ローカル アドレス帳のオブジェクト キャッシュのオフライン アドレス帳 (OAB) ファイル形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="15a17-160">Specifies the offline address book (OAB) file formats for the local address book objects cache.</span></span>
    
<span data-ttu-id="15a17-161">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15a17-161">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15a17-162">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="15a17-162">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="15a17-163">[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15a17-163">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15a17-164">プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="15a17-164">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15a17-165">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="15a17-165">Header files</span></span>

<span data-ttu-id="15a17-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15a17-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="15a17-167">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="15a17-167">Provides data type definitions.</span></span>
    
<span data-ttu-id="15a17-168">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="15a17-168">Mapitags.h</span></span>
  
> <span data-ttu-id="15a17-169">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="15a17-169">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15a17-170">関連項目</span><span class="sxs-lookup"><span data-stu-id="15a17-170">See also</span></span>



[<span data-ttu-id="15a17-171">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="15a17-171">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15a17-172">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="15a17-172">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15a17-173">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="15a17-173">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15a17-174">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="15a17-174">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

