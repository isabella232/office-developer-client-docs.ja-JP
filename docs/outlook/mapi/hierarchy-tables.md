---
title: 階層テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8aa6b36-d6e5-4e1f-8ac5-5d6a78a70bf8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2a1461f0c7196cd425d9736f5837b742bedd4fb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344577"
---
# <a name="hierarchy-tables"></a><span data-ttu-id="df0c0-103">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="df0c0-103">Hierarchy Tables</span></span>

  
  
<span data-ttu-id="df0c0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df0c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df0c0-105">階層テーブルには、メッセージストア内のフォルダーまたはアドレス帳コンテナー内のコンテナーに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="df0c0-105">A hierarchy table contains information about the folders in a message store or the containers in an address book container.</span></span> <span data-ttu-id="df0c0-106">階層テーブルの各行には、1つのフォルダーまたはアドレス帳コンテナーに関する情報が記載された一連の列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="df0c0-106">Each row of a hierarchy table contains a set of columns with information about one folder or address book container.</span></span> <span data-ttu-id="df0c0-107">階層テーブルは、主にクライアントによって使用され、メッセージストアプロバイダーによって実装され、アドレス帳のツリーを表示するためにアドレス帳プロバイダーによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="df0c0-107">Hierarchy tables are primarily used by clients and implemented by message store providers to show a tree of folders and subfolders and implemented by address book providers to show a tree of containers in the address book.</span></span> <span data-ttu-id="df0c0-108">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティで AB_SUBCONTAINERS フラグが指定されていない場合、サブコンテナーを保持できないコンテナーは、階層テーブルを実装しません。</span><span class="sxs-lookup"><span data-stu-id="df0c0-108">Containers that cannot hold subcontainers, as indicated by the absence of the AB_SUBCONTAINERS flag in their **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property, do not implement a hierarchy table.</span></span>
  
<span data-ttu-id="df0c0-109">階層テーブルには、次の呼び出しを使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="df0c0-109">A hierarchy table can be accessed by calling:</span></span>
  
- <span data-ttu-id="df0c0-110">[IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md)。</span><span class="sxs-lookup"><span data-stu-id="df0c0-110">[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span></span>
    
    - <span data-ttu-id="df0c0-111">や</span><span class="sxs-lookup"><span data-stu-id="df0c0-111">Or -</span></span>
    
- <span data-ttu-id="df0c0-112">[imapiprop:: openproperty](imapiprop-openproperty.md)は、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) をプロパティタグおよび IID_IMAPITable としてインターフェイス識別子として渡します。</span><span class="sxs-lookup"><span data-stu-id="df0c0-112">[IMAPIProp::OpenProperty](imapiprop-openproperty.md) passing **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) as the property tag and IID_IMAPITable as the interface identifier.</span></span>
    
<span data-ttu-id="df0c0-113">コンテナーとフォルダーは、テーブルのプロパティを取得するための両方の手法をサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="df0c0-113">Containers and folders must support both techniques for retrieving table properties.</span></span> <span data-ttu-id="df0c0-114">クライアントが選択を必要とするため、サービスプロバイダーがこれらのテーブルにアクセスする方法を1つだけサポートすることは許容されません。</span><span class="sxs-lookup"><span data-stu-id="df0c0-114">It is unacceptable for service providers to support only one way to access these tables because clients expect to have the choice.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="df0c0-115">ストアプロバイダーは、階層テーブルに指定された並べ替え順序セットを優先することは保証されません。</span><span class="sxs-lookup"><span data-stu-id="df0c0-115">Store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="df0c0-116">**imapiprop:: openproperty**の呼び出しでは、対応するプロパティ**PR_CONTAINER_HIERARCHY**を開くことにより、階層テーブルにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="df0c0-116">The call to **IMAPIProp::OpenProperty** involves accessing the hierarchy table by opening its corresponding property, **PR_CONTAINER_HIERARCHY**.</span></span> <span data-ttu-id="df0c0-117">**PR_CONTAINER_HIERARCHY**は、フォルダーまたはコンテナーの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを使用して取得することはできませんが、 [imapiprop:: getproplist](imapiprop-getproplist.md)メソッドによって返される property tag 配列に含まれています。</span><span class="sxs-lookup"><span data-stu-id="df0c0-117">Although **PR_CONTAINER_HIERARCHY** cannot be retrieved through a folder or container's [IMAPIProp::GetProps](imapiprop-getprops.md) method, it is included in the property tag array that is returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
  
 <span data-ttu-id="df0c0-118">**PR_CONTAINER_HIERARCHY**を使用して、コピー操作から階層テーブルを含めたり除外したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="df0c0-118">**PR_CONTAINER_HIERARCHY** can also be used to include or exclude a hierarchy table from a copy operation.</span></span> <span data-ttu-id="df0c0-119">クライアントが[imapiprop:: CopyTo](imapiprop-copyto.md)の*lpexcludeprops*パラメーターで**PR_CONTAINER_HIERARCHY**を指定している場合、コピー操作では、新しいフォルダーまたはコンテナーは元のフォルダーまたはコンテナーの階層テーブルをサポートしません。</span><span class="sxs-lookup"><span data-stu-id="df0c0-119">If a client specifies **PR_CONTAINER_HIERARCHY** in the  *lpExcludeProps*  parameter for [IMAPIProp::CopyTo](imapiprop-copyto.md) in a copy operation, the new folder or container will not support the hierarchy table of the original folder or container.</span></span> 
  
<span data-ttu-id="df0c0-120">次のプロパティは、階層テーブルで必要な列セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="df0c0-120">The following properties make up the required column set in a hierarchy table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df0c0-121">**PR_COMMENT**([PidTagComment](pidtagcomment-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df0c0-121">**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="df0c0-122">**PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df0c0-122">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="df0c0-123">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df0c0-123">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="df0c0-124">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df0c0-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="df0c0-125">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df0c0-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="df0c0-126">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df0c0-126">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="df0c0-127">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df0c0-127">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="df0c0-128">**PR_STATUS**([PidTagStatus](pidtagstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df0c0-128">**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="df0c0-129">**PR_DISPLAY_NAME**には、階層の表示に表示されるコンテナーまたはフォルダーの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="df0c0-129">**PR_DISPLAY_NAME** contains the name for the container or folder that should appear in the display of the hierarchy.</span></span> 
  
 <span data-ttu-id="df0c0-130">**PR_ENTRYID**は、このコンテナーまたはフォルダーに関連付けられているエントリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="df0c0-130">**PR_ENTRYID** is the entry identifier associated with this container or folder.</span></span> <span data-ttu-id="df0c0-131">長期のエントリ識別子であることが想定されています。</span><span class="sxs-lookup"><span data-stu-id="df0c0-131">It is expected to be a long-term entry identifier.</span></span> <span data-ttu-id="df0c0-132">クライアントと MAPI は、このエントリ識別子を**openentry**に渡して、コンテナーまたはフォルダーを開いたり、 [IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)を呼び出して内容を表示したりできます。</span><span class="sxs-lookup"><span data-stu-id="df0c0-132">Clients and MAPI can pass this entry identifier to **OpenEntry** to open the container or folder and view its contents by calling [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span> 
  
 <span data-ttu-id="df0c0-133">**PR_DEPTH**は、最上位レベルが0のこのコンテナーまたはフォルダーのインデントレベルを示す数値です。</span><span class="sxs-lookup"><span data-stu-id="df0c0-133">**PR_DEPTH** is a numeric value that indicates the level of indentation for this container or folder with zero being the top level.</span></span> <span data-ttu-id="df0c0-134">コンテナーまたはフォルダーが存在する階層の深さが深いほど、 **PR_DEPTH**プロパティの値は高くなります。</span><span class="sxs-lookup"><span data-stu-id="df0c0-134">The deeper in the hierarchy a container or folder resides, the higher the value for its **PR_DEPTH** property.</span></span> <span data-ttu-id="df0c0-135">クライアントは、 **PR_DEPTH**プロパティを使用して階層テーブルを適切に表示するので、ユーザーは、親と子の関係をはっきりと確認できます。</span><span class="sxs-lookup"><span data-stu-id="df0c0-135">Clients use the **PR_DEPTH** property to display a hierarchy table appropriately so that users can clearly see parent and child relationships.</span></span> <span data-ttu-id="df0c0-136">コンテナーまたはフォルダーの深さは、常に、階層テーブルを実装するコンテナーまたはフォルダーを基準にしています。</span><span class="sxs-lookup"><span data-stu-id="df0c0-136">Container or folder depth is always relative to the container or folder implementing the hierarchy table.</span></span> 
  
 <span data-ttu-id="df0c0-137">**PR_OBJECT_TYPE**は常に MAPI_ABCONT に設定され、アドレス帳の階層テーブルとフォルダー階層テーブルの MAPI_FOLDER が設定されます。</span><span class="sxs-lookup"><span data-stu-id="df0c0-137">**PR_OBJECT_TYPE** is always set to MAPI_ABCONT for address book hierarchy tables and MAPI_FOLDER for folder hierarchy tables.</span></span> 
  
 <span data-ttu-id="df0c0-138">**PR_DISPLAY_TYPE**は、コンテナーまたはフォルダーが階層テーブル内でどのように表示されるかに関連する数値です。</span><span class="sxs-lookup"><span data-stu-id="df0c0-138">**PR_DISPLAY_TYPE** is a numeric value that relates to how a container or folder is displayed in the hierarchy table.</span></span> <span data-ttu-id="df0c0-139">主に、コンテナーまたはフォルダーの種類を視覚的に区別するために、表示目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="df0c0-139">It is mainly used for display purposes, to differentiate visually between types of containers or folders.</span></span> <span data-ttu-id="df0c0-140">多くのメッセージストアプロバイダーとアドレス帳プロバイダーでは、さまざまなディスプレイの種類にアイコンが使用されています。</span><span class="sxs-lookup"><span data-stu-id="df0c0-140">Many message store and address book providers use icons for the different display types.</span></span> <span data-ttu-id="df0c0-141">これらのアイコンは、プロバイダーが提供します。MAPI では既定値は提供されません。</span><span class="sxs-lookup"><span data-stu-id="df0c0-141">It is up to the provider to supply these icons; MAPI does not supply defaults.</span></span> 
  
<span data-ttu-id="df0c0-142">MAPI は、 **PR_DISPLAY_TYPE**に対して多数の値を定義します。一部の値はフォルダーに対しては有効であり、アドレス帳コンテナーの階層テーブルで使用されるものもあります。</span><span class="sxs-lookup"><span data-stu-id="df0c0-142">MAPI defines many values for **PR_DISPLAY_TYPE**, some that are valid for folders and others that are used with the hierarchy tables of address book containers.</span></span> <span data-ttu-id="df0c0-143">通常、フォルダーの**PR_DISPLAY_TYPE**は、既定のフォルダーアイコンを示すために DT_FOLDER に設定され、別のフォルダーへのリンクを表すアイコンを示すために DT_FOLDER_LINK、あるいはアプリケーション固有のアイコンを示すために DT_FOLDER_SPECIAL に設定されます。</span><span class="sxs-lookup"><span data-stu-id="df0c0-143">Typically, a folder's **PR_DISPLAY_TYPE** is set to DT_FOLDER to indicate a default folder icon, DT_FOLDER_LINK to indicate an icon that represents a link to another folder, or DT_FOLDER_SPECIAL to indicate an icon that is application-specific.</span></span> <span data-ttu-id="df0c0-144">DT_FOLDER_LINK は、検索結果フォルダーと共に使用されます。</span><span class="sxs-lookup"><span data-stu-id="df0c0-144">DT_FOLDER_LINK is used with search-results folders.</span></span> 
  
<span data-ttu-id="df0c0-145">これらの必須列に加えて、アドレス帳階層テーブルに**PR_CONTAINER_FLAGS**プロパティを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="df0c0-145">In addition to these required columns, address book hierarchy tables must include the **PR_CONTAINER_FLAGS** property.</span></span> <span data-ttu-id="df0c0-146">**PR_CONTAINER_FLAGS**は、階層内のコンテナーに関するさまざまな属性を示します。これは、コンテナーと別のコンテナーを区別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="df0c0-146">**PR_CONTAINER_FLAGS** indicates various attributes about a container in the hierarchy and is used to distinguish one container from another.</span></span> 
  
<span data-ttu-id="df0c0-147">アドレス帳階層テーブルのオプションのプロパティは、 **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="df0c0-147">An optional property for address book hierarchy tables is the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="df0c0-148">メッセージストア階層テーブルには、必要な列セットにこれらのプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="df0c0-148">Message-store hierarchy tables include these properties in their required column set:</span></span>
  
- <span data-ttu-id="df0c0-149">**PR_FOLDER_TYPE**([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df0c0-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="df0c0-150">**PR_SUBFOLDERS**([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df0c0-150">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
- <span data-ttu-id="df0c0-151">**PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df0c0-151">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="df0c0-152">**PR_CONTENT_UNREAD**([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df0c0-152">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
<span data-ttu-id="df0c0-153">アドレス帳プロバイダーは、MAPI 統合アドレス帳で必要とされるため、次の**IMAPITable**メソッドを階層テーブル実装でサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="df0c0-153">Address book providers must support the following **IMAPITable** methods in their hierarchy table implementations because they are required by the MAPI integrated address book:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="df0c0-154">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="df0c0-154">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |[<span data-ttu-id="df0c0-155">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="df0c0-155">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md) <br/> |
|[<span data-ttu-id="df0c0-156">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="df0c0-156">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md) <br/> |[<span data-ttu-id="df0c0-157">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="df0c0-157">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |
|[<span data-ttu-id="df0c0-158">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="df0c0-158">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |[<span data-ttu-id="df0c0-159">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="df0c0-159">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |
|[<span data-ttu-id="df0c0-160">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="df0c0-160">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |[<span data-ttu-id="df0c0-161">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="df0c0-161">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |
|[<span data-ttu-id="df0c0-162">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="df0c0-162">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df0c0-163">関連項目</span><span class="sxs-lookup"><span data-stu-id="df0c0-163">See also</span></span>



[<span data-ttu-id="df0c0-164">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="df0c0-164">MAPI Tables</span></span>](mapi-tables.md)

