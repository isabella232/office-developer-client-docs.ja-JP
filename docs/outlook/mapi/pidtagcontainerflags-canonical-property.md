---
title: PidTagContainerFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b62fc62bb9232b7106019fca82f502221e50bad0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583562"
---
# <a name="pidtagcontainerflags-canonical-property"></a><span data-ttu-id="77713-103">PidTagContainerFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="77713-103">PidTagContainerFlags Canonical Property</span></span>

  
  
<span data-ttu-id="77713-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77713-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77713-105">アドレス帳コンテナーの機能を記述するフラグのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="77713-105">Contains a bitmask of flags describing capabilities of an address book container.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77713-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="77713-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="77713-107">PR_CONTAINER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="77713-107">PR_CONTAINER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="77713-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="77713-108">Identifier:</span></span>  <br/> |<span data-ttu-id="77713-109">0x3600</span><span class="sxs-lookup"><span data-stu-id="77713-109">0x3600</span></span>  <br/> |
|<span data-ttu-id="77713-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="77713-110">Data type:</span></span>  <br/> |<span data-ttu-id="77713-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="77713-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="77713-112">領域:</span><span class="sxs-lookup"><span data-stu-id="77713-112">Area:</span></span>  <br/> |<span data-ttu-id="77713-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="77713-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77713-114">注釈</span><span class="sxs-lookup"><span data-stu-id="77713-114">Remarks</span></span>

<span data-ttu-id="77713-115">1 つ以上次のフラグのビットマスクを設定できます。</span><span class="sxs-lookup"><span data-stu-id="77713-115">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="77713-116">AB_FIND_ON_OPEN</span><span class="sxs-lookup"><span data-stu-id="77713-116">AB_FIND_ON_OPEN</span></span> 
  
> <span data-ttu-id="77713-117">コンテナーの内容を表示する前に制限を要求するダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="77713-117">Displays a dialog box to request a restriction before displaying any contents of the container.</span></span> 
    
<span data-ttu-id="77713-118">AB_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="77713-118">AB_MODIFIABLE</span></span> 
  
> <span data-ttu-id="77713-119">エントリに追加され、コンテナーから削除します。</span><span class="sxs-lookup"><span data-stu-id="77713-119">Entries can be added to and removed from the container.</span></span> <span data-ttu-id="77713-120">このフラグでは、コンテナー内のすべてのエントリを変更できるかどうかは示されません。</span><span class="sxs-lookup"><span data-stu-id="77713-120">This flag does not indicate whether any entries in the container can be modified.</span></span>
    
<span data-ttu-id="77713-121">AB_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="77713-121">AB_RECIPIENTS</span></span> 
  
> <span data-ttu-id="77713-122">コンテナーには、受信者を保持できます。</span><span class="sxs-lookup"><span data-stu-id="77713-122">The container can hold recipients.</span></span> <span data-ttu-id="77713-123">このフラグでは、いずれかの受信者は、コンテナーに実際に存在するかどうか、またはかどうか、追加または削除は表示されません。</span><span class="sxs-lookup"><span data-stu-id="77713-123">This flag does not indicate whether any recipients are actually present in the container, or whether they can be added or removed.</span></span> 
    
<span data-ttu-id="77713-124">AB_SUBCONTAINERS</span><span class="sxs-lookup"><span data-stu-id="77713-124">AB_SUBCONTAINERS</span></span> 
  
> <span data-ttu-id="77713-125">コンテナーは、コンテナーの子を保持できます。</span><span class="sxs-lookup"><span data-stu-id="77713-125">The container can hold child containers.</span></span> <span data-ttu-id="77713-126">このフラグは、すべてのサブコンテナーは、コンテナーに実際に存在するかどうかもあるかどうか、ことができますが追加または削除には表示されません。</span><span class="sxs-lookup"><span data-stu-id="77713-126">This flag does not indicate whether any subcontainers are actually present in the container, nor whether they can be added or removed.</span></span> <span data-ttu-id="77713-127">[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)をサポートするためにコンテナーの AB_SUBCONTAINERS を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77713-127">AB_SUBCONTAINERS must be set for the container to support [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span></span> 
    
<span data-ttu-id="77713-128">AB_UNMODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="77713-128">AB_UNMODIFIABLE</span></span> 
  
> <span data-ttu-id="77713-129">エントリを追加またはコンテナーから削除されることはできません。</span><span class="sxs-lookup"><span data-stu-id="77713-129">Entries cannot be added to or removed from the container.</span></span> <span data-ttu-id="77713-130">このフラグでは、コンテナー内のすべてのエントリを変更できるかどうかは示されません。</span><span class="sxs-lookup"><span data-stu-id="77713-130">This flag does not indicate whether any entries in the container can be modified.</span></span> 
    
<span data-ttu-id="77713-131">オンライン サービスまたはサーバーへの低速の接続に使用されるコンテナーの AB_FIND_ON_OPEN フラグを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="77713-131">The AB_FIND_ON_OPEN flag is highly recommended for containers used with online services or with slow connections to servers.</span></span> <span data-ttu-id="77713-132">AB_FIND_ON_OPEN の設定を持つコンテナーが開かれたときに表示されているメッセージング ユーザーを制限するユーザーに、[**検索**] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="77713-132">When a container is opened that has AB_FIND_ON_OPEN set, a **Find** dialog box is presented to the user to restrict the displayed messaging users.</span></span> <span data-ttu-id="77713-133">メッセージングのユーザーを制限する部分の仕様は、内容の表示を劇的に短縮できます。</span><span class="sxs-lookup"><span data-stu-id="77713-133">Even a partial specification limiting the messaging users can dramatically speed up a display of the contents.</span></span> 
  
<span data-ttu-id="77713-134">AB_MODIFIABLE または AB_UNMODIFIABLE のいずれかのフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77713-134">Either the AB_MODIFIABLE or AB_UNMODIFIABLE flag must be set.</span></span> <span data-ttu-id="77713-135">あるコンテナーがわからないかどうか変更するか、変更がユーザーのアクセス権に依存する場合の例を示すためには、両方のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="77713-135">Both flags can be set to indicate that the container does not know whether it can be modified or not, for example if modification depends on the user's access rights.</span></span> <span data-ttu-id="77713-136">この例では、クライアント アプリケーションは呼び出しを試みるし、コンテナーの機能を確認するのにはリターン コードを調査する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77713-136">In this case, a client application must attempt a call and examine the return code to determine the container's capabilities.</span></span> <span data-ttu-id="77713-137">クライアントは、通常、AB_MODIFIABLE を調べることによって開始します。</span><span class="sxs-lookup"><span data-stu-id="77713-137">A client typically starts by examining AB_MODIFIABLE.</span></span> <span data-ttu-id="77713-138">設定されている場合、クライアントは、コンテナーを変更しようとして、戻り値をチェックするための呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="77713-138">If it is set, the client makes a call that attempts to modify the container and checks the return value.</span></span> 
  
<span data-ttu-id="77713-139">AB_MODIFIABLE フラグはすることができますエントリの種類を示していないコンテナーに追加します。</span><span class="sxs-lookup"><span data-stu-id="77713-139">The AB_MODIFIABLE flag does not indicate what types of entries can be added to the container.</span></span> <span data-ttu-id="77713-140">これを確認するには、クライアントが、コンテナーの**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティを開くに適切な[OpenProperty](imapiprop-openproperty.md)メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77713-140">To determine this, the client should use the appropriate [OpenProperty](imapiprop-openproperty.md) method to open the container's **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="77713-141">開始**PR_CREATE_TEMPLATES**原因が返され、テーブルのコンテナーの one-off コンテナー内に作成できるエントリの種類を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="77713-141">Opening **PR_CREATE_TEMPLATES** causes the container's one-off table to be returned, listing the kinds of entries that can be created in the container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="77713-142">関連リソース</span><span class="sxs-lookup"><span data-stu-id="77713-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="77713-143">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="77713-143">Protocol specifications</span></span>

<span data-ttu-id="77713-144">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77713-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77713-145">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="77713-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="77713-146">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77713-146">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77713-147">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="77713-147">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="77713-148">[[MS NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77713-148">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77713-149">ネーム サービス プロバイダー インターフェイス (NSPI) サーバーとクライアントの通信を処理します。</span><span class="sxs-lookup"><span data-stu-id="77713-149">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="77713-150">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="77713-150">Header files</span></span>

<span data-ttu-id="77713-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="77713-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="77713-152">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="77713-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="77713-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="77713-153">Mapitags.h</span></span>
  
> <span data-ttu-id="77713-154">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="77713-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77713-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="77713-155">See also</span></span>



[<span data-ttu-id="77713-156">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="77713-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="77713-157">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="77713-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="77713-158">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="77713-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="77713-159">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="77713-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

