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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c9c446097213e5b743a47ec32db17ec0afe63b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357548"
---
# <a name="pidtagcontainerflags-canonical-property"></a><span data-ttu-id="194e9-103">PidTagContainerFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="194e9-103">PidTagContainerFlags Canonical Property</span></span>

  
  
<span data-ttu-id="194e9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="194e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="194e9-105">アドレス帳コンテナーの機能を説明するフラグのビットマスクが含まれる。</span><span class="sxs-lookup"><span data-stu-id="194e9-105">Contains a bitmask of flags describing capabilities of an address book container.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="194e9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="194e9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="194e9-107">PR_CONTAINER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="194e9-107">PR_CONTAINER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="194e9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="194e9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="194e9-109">0x3600</span><span class="sxs-lookup"><span data-stu-id="194e9-109">0x3600</span></span>  <br/> |
|<span data-ttu-id="194e9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="194e9-110">Data type:</span></span>  <br/> |<span data-ttu-id="194e9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="194e9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="194e9-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="194e9-112">Area:</span></span>  <br/> |<span data-ttu-id="194e9-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="194e9-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="194e9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="194e9-114">Remarks</span></span>

<span data-ttu-id="194e9-115">ビットマスクには、次のフラグを 1 つ以上設定できます。</span><span class="sxs-lookup"><span data-stu-id="194e9-115">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="194e9-116">AB_FIND_ON_OPEN</span><span class="sxs-lookup"><span data-stu-id="194e9-116">AB_FIND_ON_OPEN</span></span> 
  
> <span data-ttu-id="194e9-117">コンテナーの内容を表示する前に、制限を要求するダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="194e9-117">Displays a dialog box to request a restriction before displaying any contents of the container.</span></span> 
    
<span data-ttu-id="194e9-118">AB_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="194e9-118">AB_MODIFIABLE</span></span> 
  
> <span data-ttu-id="194e9-119">エントリはコンテナーに追加および削除できます。</span><span class="sxs-lookup"><span data-stu-id="194e9-119">Entries can be added to and removed from the container.</span></span> <span data-ttu-id="194e9-120">このフラグは、コンテナー内のエントリを変更できるかどうかを示す値ではありません。</span><span class="sxs-lookup"><span data-stu-id="194e9-120">This flag does not indicate whether any entries in the container can be modified.</span></span>
    
<span data-ttu-id="194e9-121">AB_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="194e9-121">AB_RECIPIENTS</span></span> 
  
> <span data-ttu-id="194e9-122">コンテナーは受信者を保持できます。</span><span class="sxs-lookup"><span data-stu-id="194e9-122">The container can hold recipients.</span></span> <span data-ttu-id="194e9-123">このフラグは、コンテナー内に受信者が実際に存在するかどうか、または受信者を追加または削除できるかどうかを示すのではありません。</span><span class="sxs-lookup"><span data-stu-id="194e9-123">This flag does not indicate whether any recipients are actually present in the container, or whether they can be added or removed.</span></span> 
    
<span data-ttu-id="194e9-124">AB_SUBCONTAINERS</span><span class="sxs-lookup"><span data-stu-id="194e9-124">AB_SUBCONTAINERS</span></span> 
  
> <span data-ttu-id="194e9-125">コンテナーは子コンテナーを保持できます。</span><span class="sxs-lookup"><span data-stu-id="194e9-125">The container can hold child containers.</span></span> <span data-ttu-id="194e9-126">このフラグは、どのサブコンテナーが実際にコンテナーに存在するか、追加または削除できるかどうかを示すのではありません。</span><span class="sxs-lookup"><span data-stu-id="194e9-126">This flag does not indicate whether any subcontainers are actually present in the container, nor whether they can be added or removed.</span></span> <span data-ttu-id="194e9-127">AB_SUBCONTAINERS [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)をサポートするには、コンテナーに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="194e9-127">AB_SUBCONTAINERS must be set for the container to support [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span></span> 
    
<span data-ttu-id="194e9-128">AB_UNMODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="194e9-128">AB_UNMODIFIABLE</span></span> 
  
> <span data-ttu-id="194e9-129">コンテナーにエントリを追加したり、コンテナーから削除したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="194e9-129">Entries cannot be added to or removed from the container.</span></span> <span data-ttu-id="194e9-130">このフラグは、コンテナー内のエントリを変更できるかどうかを示す値ではありません。</span><span class="sxs-lookup"><span data-stu-id="194e9-130">This flag does not indicate whether any entries in the container can be modified.</span></span> 
    
<span data-ttu-id="194e9-131">オンライン サービスAB_FIND_ON_OPENサーバーへの低速接続で使用されるコンテナーには、このフラグを使用することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="194e9-131">The AB_FIND_ON_OPEN flag is highly recommended for containers used with online services or with slow connections to servers.</span></span> <span data-ttu-id="194e9-132">設定されているコンテナーを開AB_FIND_ON_OPEN、表示されるメッセージング ユーザーを制限する[検索] ダイアログ ボックスがユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="194e9-132">When a container is opened that has AB_FIND_ON_OPEN set, a **Find** dialog box is presented to the user to restrict the displayed messaging users.</span></span> <span data-ttu-id="194e9-133">メッセージング ユーザーを制限する部分的な仕様でも、コンテンツの表示を大幅に高速化できます。</span><span class="sxs-lookup"><span data-stu-id="194e9-133">Even a partial specification limiting the messaging users can dramatically speed up a display of the contents.</span></span> 
  
<span data-ttu-id="194e9-134">AB_MODIFIABLEまたはAB_UNMODIFIABLEフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="194e9-134">Either the AB_MODIFIABLE or AB_UNMODIFIABLE flag must be set.</span></span> <span data-ttu-id="194e9-135">両方のフラグを設定すると、変更がユーザーのアクセス権に依存する場合など、コンテナーが変更できるかどうかがわかりません。</span><span class="sxs-lookup"><span data-stu-id="194e9-135">Both flags can be set to indicate that the container does not know whether it can be modified or not, for example if modification depends on the user's access rights.</span></span> <span data-ttu-id="194e9-136">この場合、クライアント アプリケーションは呼び出しを試み、戻りコードを調べてコンテナーの機能を判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="194e9-136">In this case, a client application must attempt a call and examine the return code to determine the container's capabilities.</span></span> <span data-ttu-id="194e9-137">通常、クライアントは、クライアントの検証からAB_MODIFIABLE。</span><span class="sxs-lookup"><span data-stu-id="194e9-137">A client typically starts by examining AB_MODIFIABLE.</span></span> <span data-ttu-id="194e9-138">設定されている場合、クライアントはコンテナーの変更を試み、戻り値を確認する呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="194e9-138">If it is set, the client makes a call that attempts to modify the container and checks the return value.</span></span> 
  
<span data-ttu-id="194e9-139">このAB_MODIFIABLEは、コンテナーに追加できるエントリの種類を示す値ではありません。</span><span class="sxs-lookup"><span data-stu-id="194e9-139">The AB_MODIFIABLE flag does not indicate what types of entries can be added to the container.</span></span> <span data-ttu-id="194e9-140">これを確認するには、クライアントは適切な [OpenProperty](imapiprop-openproperty.md)メソッドを使用してコンテナーのプロパティ [(PidTagCreateTemplates)](pidtagcreatetemplates-canonical-property.md)**プロパティを開** PR_CREATE_TEMPLATESする必要があります。</span><span class="sxs-lookup"><span data-stu-id="194e9-140">To determine this, the client should use the appropriate [OpenProperty](imapiprop-openproperty.md) method to open the container's **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="194e9-141">この **PR_CREATE_TEMPLATES** すると、コンテナーの 1 回のテーブルが返され、コンテナーに作成できるエントリの種類が一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="194e9-141">Opening **PR_CREATE_TEMPLATES** causes the container's one-off table to be returned, listing the kinds of entries that can be created in the container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="194e9-142">関連リソース</span><span class="sxs-lookup"><span data-stu-id="194e9-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="194e9-143">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="194e9-143">Protocol specifications</span></span>

<span data-ttu-id="194e9-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="194e9-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="194e9-145">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="194e9-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="194e9-146">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="194e9-146">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="194e9-147">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="194e9-147">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="194e9-148">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="194e9-148">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="194e9-149">ネーム サービス プロバイダー インターフェイス (NSPI) サーバーとのクライアントの通信を処理します。</span><span class="sxs-lookup"><span data-stu-id="194e9-149">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="194e9-150">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="194e9-150">Header files</span></span>

<span data-ttu-id="194e9-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="194e9-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="194e9-152">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="194e9-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="194e9-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="194e9-153">Mapitags.h</span></span>
  
> <span data-ttu-id="194e9-154">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="194e9-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="194e9-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="194e9-155">See also</span></span>



[<span data-ttu-id="194e9-156">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="194e9-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="194e9-157">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="194e9-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="194e9-158">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="194e9-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="194e9-159">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="194e9-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

