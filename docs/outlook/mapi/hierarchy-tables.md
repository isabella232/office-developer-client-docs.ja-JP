---
title: 階層テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8aa6b36-d6e5-4e1f-8ac5-5d6a78a70bf8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2a1461f0c7196cd425d9736f5837b742bedd4fb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428369"
---
# <a name="hierarchy-tables"></a><span data-ttu-id="22f9d-103">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="22f9d-103">Hierarchy Tables</span></span>

  
  
<span data-ttu-id="22f9d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22f9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22f9d-105">階層テーブルには、メッセージ ストア内のフォルダー、またはアドレス帳コンテナー内のコンテナーに関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="22f9d-105">A hierarchy table contains information about the folders in a message store or the containers in an address book container.</span></span> <span data-ttu-id="22f9d-106">階層テーブルの各行には、1 つのフォルダーまたはアドレス帳コンテナーに関する情報を含む列のセットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="22f9d-106">Each row of a hierarchy table contains a set of columns with information about one folder or address book container.</span></span> <span data-ttu-id="22f9d-107">階層テーブルは主にクライアントによって使用され、メッセージ ストア プロバイダーによってフォルダーとサブフォルダーのツリーを表示するために実装され、アドレス帳プロバイダーによって実装され、アドレス帳にコンテナーのツリーを表示します。</span><span class="sxs-lookup"><span data-stu-id="22f9d-107">Hierarchy tables are primarily used by clients and implemented by message store providers to show a tree of folders and subfolders and implemented by address book providers to show a tree of containers in the address book.</span></span> <span data-ttu-id="22f9d-108">PR_CONTAINER_FLAGS ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティに **AB_SUBCONTAINERS** フラグがない場合に示されるサブコンテナーを保持できないコンテナーは、階層テーブルを実装できません。</span><span class="sxs-lookup"><span data-stu-id="22f9d-108">Containers that cannot hold subcontainers, as indicated by the absence of the AB_SUBCONTAINERS flag in their **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property, do not implement a hierarchy table.</span></span>
  
<span data-ttu-id="22f9d-109">階層テーブルには、次の呼び出しでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="22f9d-109">A hierarchy table can be accessed by calling:</span></span>
  
- <span data-ttu-id="22f9d-110">[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span><span class="sxs-lookup"><span data-stu-id="22f9d-110">[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span></span>
    
    - <span data-ttu-id="22f9d-111">Or -</span><span class="sxs-lookup"><span data-stu-id="22f9d-111">Or -</span></span>
    
- <span data-ttu-id="22f9d-112">[IMAPIProp::OpenProperty](imapiprop-openproperty.md) は、PR_CONTAINER_HIERARCHY **(** [PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) をプロパティ タグとして渡し、IID_IMAPITableをインターフェイス識別子として渡します。</span><span class="sxs-lookup"><span data-stu-id="22f9d-112">[IMAPIProp::OpenProperty](imapiprop-openproperty.md) passing **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) as the property tag and IID_IMAPITable as the interface identifier.</span></span>
    
<span data-ttu-id="22f9d-113">コンテナーとフォルダーは、テーブル のプロパティを取得するための両方の手法をサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="22f9d-113">Containers and folders must support both techniques for retrieving table properties.</span></span> <span data-ttu-id="22f9d-114">サービス プロバイダーがこれらのテーブルにアクセスする 1 つの方法のみをサポートできるのは、クライアントが選択肢を持つ必要があるため、受け入れられません。</span><span class="sxs-lookup"><span data-stu-id="22f9d-114">It is unacceptable for service providers to support only one way to access these tables because clients expect to have the choice.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="22f9d-115">ストア プロバイダーは、階層テーブルに指定された並べ替え順序セットを尊重する保証はありません。</span><span class="sxs-lookup"><span data-stu-id="22f9d-115">Store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="22f9d-116">**IMAPIProp::OpenProperty** の呼び出しでは、対応するプロパティを開いて階層 **テーブル** にアクセスPR_CONTAINER_HIERARCHY。</span><span class="sxs-lookup"><span data-stu-id="22f9d-116">The call to **IMAPIProp::OpenProperty** involves accessing the hierarchy table by opening its corresponding property, **PR_CONTAINER_HIERARCHY**.</span></span> <span data-ttu-id="22f9d-117">フォルダー **PR_CONTAINER_HIERARCHY** コンテナーの [IMAPIProp::GetProps メソッドでは取得できませんが、IMAPIProp::GetPropList](imapiprop-getprops.md)メソッドによって返されるプロパティ タグ配列に含 [](imapiprop-getproplist.md)まれます。</span><span class="sxs-lookup"><span data-stu-id="22f9d-117">Although **PR_CONTAINER_HIERARCHY** cannot be retrieved through a folder or container's [IMAPIProp::GetProps](imapiprop-getprops.md) method, it is included in the property tag array that is returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
  
 <span data-ttu-id="22f9d-118">**PR_CONTAINER_HIERARCHY** を使用して、階層テーブルをコピー操作から含めるか除外することもできます。</span><span class="sxs-lookup"><span data-stu-id="22f9d-118">**PR_CONTAINER_HIERARCHY** can also be used to include or exclude a hierarchy table from a copy operation.</span></span> <span data-ttu-id="22f9d-119">クライアントがコピー **操作で** [IMAPIProp::CopyTo](imapiprop-copyto.md)の *lpExcludeProps* パラメーターに PR_CONTAINER_HIERARCHY を指定した場合、新しいフォルダーまたはコンテナーは元のフォルダーまたはコンテナーの階層テーブルをサポートしない。</span><span class="sxs-lookup"><span data-stu-id="22f9d-119">If a client specifies **PR_CONTAINER_HIERARCHY** in the  *lpExcludeProps*  parameter for [IMAPIProp::CopyTo](imapiprop-copyto.md) in a copy operation, the new folder or container will not support the hierarchy table of the original folder or container.</span></span> 
  
<span data-ttu-id="22f9d-120">次のプロパティは、階層テーブルで必要な列セットを構成します。</span><span class="sxs-lookup"><span data-stu-id="22f9d-120">The following properties make up the required column set in a hierarchy table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22f9d-121">**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22f9d-121">**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="22f9d-122">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22f9d-122">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="22f9d-123">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22f9d-123">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="22f9d-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22f9d-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="22f9d-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22f9d-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="22f9d-126">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22f9d-126">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="22f9d-127">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22f9d-127">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="22f9d-128">**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22f9d-128">**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="22f9d-129">**PR_DISPLAY_NAME** には、階層の表示に表示するコンテナーまたはフォルダーの名前が含まれます。</span><span class="sxs-lookup"><span data-stu-id="22f9d-129">**PR_DISPLAY_NAME** contains the name for the container or folder that should appear in the display of the hierarchy.</span></span> 
  
 <span data-ttu-id="22f9d-130">**PR_ENTRYID** は、このコンテナーまたはフォルダーに関連付けられているエントリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="22f9d-130">**PR_ENTRYID** is the entry identifier associated with this container or folder.</span></span> <span data-ttu-id="22f9d-131">これは、長期的なエントリ識別子である必要があります。</span><span class="sxs-lookup"><span data-stu-id="22f9d-131">It is expected to be a long-term entry identifier.</span></span> <span data-ttu-id="22f9d-132">クライアントと MAPI は、このエントリ識別子を **OpenEntry** に渡してコンテナーまたはフォルダーを開き [、IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)を呼び出すことによってその内容を表示できます。</span><span class="sxs-lookup"><span data-stu-id="22f9d-132">Clients and MAPI can pass this entry identifier to **OpenEntry** to open the container or folder and view its contents by calling [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span> 
  
 <span data-ttu-id="22f9d-133">**PR_DEPTH** は、このコンテナーまたはフォルダーのインデントのレベルを表す数値で、0 がトップ レベルです。</span><span class="sxs-lookup"><span data-stu-id="22f9d-133">**PR_DEPTH** is a numeric value that indicates the level of indentation for this container or folder with zero being the top level.</span></span> <span data-ttu-id="22f9d-134">コンテナーまたはフォルダーが存在する階層が深いほど、コンテナーまたはフォルダーのプロパティの値 **PR_DEPTH** します。</span><span class="sxs-lookup"><span data-stu-id="22f9d-134">The deeper in the hierarchy a container or folder resides, the higher the value for its **PR_DEPTH** property.</span></span> <span data-ttu-id="22f9d-135">クライアントは **、PR_DEPTH** プロパティを使用して階層テーブルを適切に表示し、ユーザーが親と子の関係を明確に確認できます。</span><span class="sxs-lookup"><span data-stu-id="22f9d-135">Clients use the **PR_DEPTH** property to display a hierarchy table appropriately so that users can clearly see parent and child relationships.</span></span> <span data-ttu-id="22f9d-136">コンテナーまたはフォルダーの深度は、階層テーブルを実装するコンテナーまたはフォルダーに対して常に相対的です。</span><span class="sxs-lookup"><span data-stu-id="22f9d-136">Container or folder depth is always relative to the container or folder implementing the hierarchy table.</span></span> 
  
 <span data-ttu-id="22f9d-137">**PR_OBJECT_TYPE** は、常にアドレス帳MAPI_ABCONTテーブルとフォルダー階層テーブルのMAPI_FOLDERに設定されます。</span><span class="sxs-lookup"><span data-stu-id="22f9d-137">**PR_OBJECT_TYPE** is always set to MAPI_ABCONT for address book hierarchy tables and MAPI_FOLDER for folder hierarchy tables.</span></span> 
  
 <span data-ttu-id="22f9d-138">**PR_DISPLAY_TYPE** は、コンテナーまたはフォルダーを階層テーブルに表示する方法に関連する数値です。</span><span class="sxs-lookup"><span data-stu-id="22f9d-138">**PR_DISPLAY_TYPE** is a numeric value that relates to how a container or folder is displayed in the hierarchy table.</span></span> <span data-ttu-id="22f9d-139">これは主に、コンテナーまたはフォルダーの種類を視覚的に区別するために、表示目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="22f9d-139">It is mainly used for display purposes, to differentiate visually between types of containers or folders.</span></span> <span data-ttu-id="22f9d-140">多くのメッセージ ストアプロバイダーとアドレス帳プロバイダーは、さまざまな種類の表示にアイコンを使用します。</span><span class="sxs-lookup"><span data-stu-id="22f9d-140">Many message store and address book providers use icons for the different display types.</span></span> <span data-ttu-id="22f9d-141">これらのアイコンはプロバイダーが提供する必要があります。MAPI では、既定値は指定されません。</span><span class="sxs-lookup"><span data-stu-id="22f9d-141">It is up to the provider to supply these icons; MAPI does not supply defaults.</span></span> 
  
<span data-ttu-id="22f9d-142">MAPI では、アドレス帳コンテナー PR_DISPLAY_TYPE階層テーブルで使用されるフォルダーや他のフォルダーに有効な値を多数定義します。</span><span class="sxs-lookup"><span data-stu-id="22f9d-142">MAPI defines many values for **PR_DISPLAY_TYPE**, some that are valid for folders and others that are used with the hierarchy tables of address book containers.</span></span> <span data-ttu-id="22f9d-143">通常、フォルダーの **PR_DISPLAY_TYPE** は DT_FOLDER に設定して既定のフォルダー アイコンを示し、DT_FOLDER_LINK は別のフォルダーへのリンクを表すアイコンを示し、DT_FOLDER_SPECIAL はアプリケーション固有のアイコンを示します。</span><span class="sxs-lookup"><span data-stu-id="22f9d-143">Typically, a folder's **PR_DISPLAY_TYPE** is set to DT_FOLDER to indicate a default folder icon, DT_FOLDER_LINK to indicate an icon that represents a link to another folder, or DT_FOLDER_SPECIAL to indicate an icon that is application-specific.</span></span> <span data-ttu-id="22f9d-144">DT_FOLDER_LINKは、検索結果フォルダーと一緒に使用されます。</span><span class="sxs-lookup"><span data-stu-id="22f9d-144">DT_FOLDER_LINK is used with search-results folders.</span></span> 
  
<span data-ttu-id="22f9d-145">これらの必須の列に加えて、アドレス帳階層テーブルに PR_CONTAINER_FLAGSする **必要** があります。</span><span class="sxs-lookup"><span data-stu-id="22f9d-145">In addition to these required columns, address book hierarchy tables must include the **PR_CONTAINER_FLAGS** property.</span></span> <span data-ttu-id="22f9d-146">**PR_CONTAINER_FLAGS** は、階層内のコンテナーに関するさまざまな属性を示し、あるコンテナーを別のコンテナーと区別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="22f9d-146">**PR_CONTAINER_FLAGS** indicates various attributes about a container in the hierarchy and is used to distinguish one container from another.</span></span> 
  
<span data-ttu-id="22f9d-147">アドレス帳階層テーブルの省略可能なプロパティは、PR_AB_PROVIDER_ID **(** [PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="22f9d-147">An optional property for address book hierarchy tables is the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="22f9d-148">メッセージ ストア階層テーブルには、必要な列セットに次のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="22f9d-148">Message-store hierarchy tables include these properties in their required column set:</span></span>
  
- <span data-ttu-id="22f9d-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22f9d-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="22f9d-150">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22f9d-150">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
- <span data-ttu-id="22f9d-151">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22f9d-151">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="22f9d-152">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22f9d-152">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
<span data-ttu-id="22f9d-153">アドレス帳プロバイダーは、MAPI 統合アドレス帳で必要なので、階層テーブルの実装で次の **IMAPITable** メソッドをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="22f9d-153">Address book providers must support the following **IMAPITable** methods in their hierarchy table implementations because they are required by the MAPI integrated address book:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="22f9d-154">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="22f9d-154">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |[<span data-ttu-id="22f9d-155">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="22f9d-155">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md) <br/> |
|[<span data-ttu-id="22f9d-156">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="22f9d-156">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md) <br/> |[<span data-ttu-id="22f9d-157">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="22f9d-157">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |
|[<span data-ttu-id="22f9d-158">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="22f9d-158">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |[<span data-ttu-id="22f9d-159">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="22f9d-159">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |
|[<span data-ttu-id="22f9d-160">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="22f9d-160">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |[<span data-ttu-id="22f9d-161">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="22f9d-161">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |
|[<span data-ttu-id="22f9d-162">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="22f9d-162">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22f9d-163">関連項目</span><span class="sxs-lookup"><span data-stu-id="22f9d-163">See also</span></span>



[<span data-ttu-id="22f9d-164">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="22f9d-164">MAPI Tables</span></span>](mapi-tables.md)

