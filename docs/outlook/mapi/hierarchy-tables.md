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
ms.openlocfilehash: d135e0c224866cd2a675df2ef9ec1b206f3169ab
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580755"
---
# <a name="hierarchy-tables"></a><span data-ttu-id="51900-103">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="51900-103">Hierarchy Tables</span></span>

  
  
<span data-ttu-id="51900-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51900-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51900-105">階層テーブルには、メッセージ ・ ストア内のフォルダーまたはアドレス帳コンテナーにコンテナーに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="51900-105">A hierarchy table contains information about the folders in a message store or the containers in an address book container.</span></span> <span data-ttu-id="51900-106">階層テーブルの各行には、1 つのフォルダーまたはアドレス帳コンテナーに関する情報を持つ列のセットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="51900-106">Each row of a hierarchy table contains a set of columns with information about one folder or address book container.</span></span> <span data-ttu-id="51900-107">階層テーブルは、主にクライアントによって使用されるフォルダーとサブフォルダーのツリーを表示するのには、メッセージ ストア プロバイダーによって実装され、アドレス帳コンテナーのツリーを表示するアドレス帳のプロバイダーによって実装されています。</span><span class="sxs-lookup"><span data-stu-id="51900-107">Hierarchy tables are primarily used by clients and implemented by message store providers to show a tree of folders and subfolders and implemented by address book providers to show a tree of containers in the address book.</span></span> <span data-ttu-id="51900-108">コンテナーのサブコンテナーを保持することはできませんが、 **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) のプロパティに AB_SUBCONTAINERS フラグがない場合で示されるように実装しない階層テーブルです。</span><span class="sxs-lookup"><span data-stu-id="51900-108">Containers that cannot hold subcontainers, as indicated by the absence of the AB_SUBCONTAINERS flag in their **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property, do not implement a hierarchy table.</span></span>
  
<span data-ttu-id="51900-109">階層テーブルを呼び出すことによってアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="51900-109">A hierarchy table can be accessed by calling:</span></span>
  
- <span data-ttu-id="51900-110">[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)。</span><span class="sxs-lookup"><span data-stu-id="51900-110">[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span></span>
    
    - <span data-ttu-id="51900-111">または、</span><span class="sxs-lookup"><span data-stu-id="51900-111">Or -</span></span>
    
- <span data-ttu-id="51900-112">[IMAPIProp::OpenProperty](imapiprop-openproperty.md)は、プロパティ タグとインターフェイス識別子として IID_IMAPITable として**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) を渡すことです。</span><span class="sxs-lookup"><span data-stu-id="51900-112">[IMAPIProp::OpenProperty](imapiprop-openproperty.md) passing **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) as the property tag and IID_IMAPITable as the interface identifier.</span></span>
    
<span data-ttu-id="51900-113">コンテナー、フォルダーは、[表のプロパティを取得するための両方の方法をサポートしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="51900-113">Containers and folders must support both techniques for retrieving table properties.</span></span> <span data-ttu-id="51900-114">どちらかを選択することがクライアントにこれらのテーブルをアクセスするための方法の 1 つのみをサポートするためにサービス ・ プロバイダーの許容可能なことはできません。</span><span class="sxs-lookup"><span data-stu-id="51900-114">It is unacceptable for service providers to support only one way to access these tables because clients expect to have the choice.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="51900-115">階層テーブルの指定した並べ替え順を優先するのには、ストア プロバイダーは保証されません。</span><span class="sxs-lookup"><span data-stu-id="51900-115">Store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="51900-116">**IMAPIProp::OpenProperty**への呼び出しでは、対応するプロパティ、 **PR_CONTAINER_HIERARCHY**を開いて、階層テーブルにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="51900-116">The call to **IMAPIProp::OpenProperty** involves accessing the hierarchy table by opening its corresponding property, **PR_CONTAINER_HIERARCHY**.</span></span> <span data-ttu-id="51900-117">フォルダーまたはコンテナーの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを**PR_CONTAINER_HIERARCHY**を取得することはできませんが、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドによって返されるプロパティ タグ配列に含まれます。</span><span class="sxs-lookup"><span data-stu-id="51900-117">Although **PR_CONTAINER_HIERARCHY** cannot be retrieved through a folder or container's [IMAPIProp::GetProps](imapiprop-getprops.md) method, it is included in the property tag array that is returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
  
 <span data-ttu-id="51900-118">**PR_CONTAINER_HIERARCHY**は、コピー操作の階層テーブルをエクスクルードまたはインクルードするにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="51900-118">**PR_CONTAINER_HIERARCHY** can also be used to include or exclude a hierarchy table from a copy operation.</span></span> <span data-ttu-id="51900-119">クライアントは、コピー操作で[IMAPIProp::CopyTo](imapiprop-copyto.md)の*lpExcludeProps*パラメーターでの**PR_CONTAINER_HIERARCHY**を指定した場合、新しいフォルダーまたはコンテナーはサポートされません、元のフォルダーまたはコンテナーの階層テーブル。</span><span class="sxs-lookup"><span data-stu-id="51900-119">If a client specifies **PR_CONTAINER_HIERARCHY** in the  *lpExcludeProps*  parameter for [IMAPIProp::CopyTo](imapiprop-copyto.md) in a copy operation, the new folder or container will not support the hierarchy table of the original folder or container.</span></span> 
  
<span data-ttu-id="51900-120">次のプロパティは、必要な列の階層テーブルの設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="51900-120">The following properties make up the required column set in a hierarchy table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51900-121">**PR_COMMENT**([PidTagComment](pidtagcomment-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51900-121">**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="51900-122">**PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51900-122">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="51900-123">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51900-123">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="51900-124">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51900-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="51900-125">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51900-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="51900-126">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51900-126">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="51900-127">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51900-127">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="51900-128">**PR_STATUS**([PidTagStatus](pidtagstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51900-128">**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="51900-129">**PR_DISPLAY_NAME**には、コンテナーまたは階層の表示に表示されるフォルダーの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="51900-129">**PR_DISPLAY_NAME** contains the name for the container or folder that should appear in the display of the hierarchy.</span></span> 
  
 <span data-ttu-id="51900-130">**PR_ENTRYID**は、このコンテナーまたはフォルダーに関連付けられているエントリの識別子です。</span><span class="sxs-lookup"><span data-stu-id="51900-130">**PR_ENTRYID** is the entry identifier associated with this container or folder.</span></span> <span data-ttu-id="51900-131">長期のエントリ id を使用する予定です。</span><span class="sxs-lookup"><span data-stu-id="51900-131">It is expected to be a long-term entry identifier.</span></span> <span data-ttu-id="51900-132">クライアントと、MAPI は、コンテナーまたはフォルダーを開き、 [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)を呼び出すことによってその内容を表示する**OpenEntry**にこのエントリの識別子を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="51900-132">Clients and MAPI can pass this entry identifier to **OpenEntry** to open the container or folder and view its contents by calling [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span> 
  
 <span data-ttu-id="51900-133">**PR_DEPTH**は、0 が最上位レベルでこのコンテナーまたはフォルダーのインデントのレベルを示す数値です。</span><span class="sxs-lookup"><span data-stu-id="51900-133">**PR_DEPTH** is a numeric value that indicates the level of indentation for this container or folder with zero being the top level.</span></span> <span data-ttu-id="51900-134">コンテナーまたはフォルダー階層のより深いレベルが存在する、 **PR_DEPTH**プロパティの値を大きくします。</span><span class="sxs-lookup"><span data-stu-id="51900-134">The deeper in the hierarchy a container or folder resides, the higher the value for its **PR_DEPTH** property.</span></span> <span data-ttu-id="51900-135">クライアントは、ユーザーが明確に親と子の関係を確認できるように、階層テーブルを適切に表示するのには、 **PR_DEPTH**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="51900-135">Clients use the **PR_DEPTH** property to display a hierarchy table appropriately so that users can clearly see parent and child relationships.</span></span> <span data-ttu-id="51900-136">コンテナーまたはフォルダーの深さは常にコンテナーまたはフォルダーの階層テーブルを実装します。</span><span class="sxs-lookup"><span data-stu-id="51900-136">Container or folder depth is always relative to the container or folder implementing the hierarchy table.</span></span> 
  
 <span data-ttu-id="51900-137">**PR_OBJECT_TYPE**は常に設定 MAPI_ABCONT にアドレス帳階層テーブルおよび MAPI_FOLDER フォルダーの階層テーブルにします。</span><span class="sxs-lookup"><span data-stu-id="51900-137">**PR_OBJECT_TYPE** is always set to MAPI_ABCONT for address book hierarchy tables and MAPI_FOLDER for folder hierarchy tables.</span></span> 
  
 <span data-ttu-id="51900-138">**PR_DISPLAY_TYPE**は、コンテナーまたはフォルダーの階層テーブルの表示方法に関連する数値値です。</span><span class="sxs-lookup"><span data-stu-id="51900-138">**PR_DISPLAY_TYPE** is a numeric value that relates to how a container or folder is displayed in the hierarchy table.</span></span> <span data-ttu-id="51900-139">表示用には、コンテナーまたはフォルダーの種類を視覚的に区別するために主に使用されます。</span><span class="sxs-lookup"><span data-stu-id="51900-139">It is mainly used for display purposes, to differentiate visually between types of containers or folders.</span></span> <span data-ttu-id="51900-140">多くのメッセージは、保存し、アドレス帳プロバイダーは、さまざまな表示の種類のアイコンを使用します。</span><span class="sxs-lookup"><span data-stu-id="51900-140">Many message store and address book providers use icons for the different display types.</span></span> <span data-ttu-id="51900-141">これらのアイコンを提供するプロバイダーMAPI では、既定値が用意されていません。</span><span class="sxs-lookup"><span data-stu-id="51900-141">It is up to the provider to supply these icons; MAPI does not supply defaults.</span></span> 
  
<span data-ttu-id="51900-142">MAPI では、 **PR_DISPLAY_TYPE**フォルダーとアドレス帳コンテナーの階層テーブルで使用される他のユーザーの有効なされているいくつかの多くの値を定義します。</span><span class="sxs-lookup"><span data-stu-id="51900-142">MAPI defines many values for **PR_DISPLAY_TYPE**, some that are valid for folders and others that are used with the hierarchy tables of address book containers.</span></span> <span data-ttu-id="51900-143">通常、フォルダーの**PR_DISPLAY_TYPE**は、別のフォルダーへのリンクを表すアイコンを示すために DT_FOLDER_LINK または DT_FOLDER_SPECIAL は、アプリケーション固有のアイコンを示すために、既定のフォルダー アイコンを示すために DT_FOLDER に設定されています。</span><span class="sxs-lookup"><span data-stu-id="51900-143">Typically, a folder's **PR_DISPLAY_TYPE** is set to DT_FOLDER to indicate a default folder icon, DT_FOLDER_LINK to indicate an icon that represents a link to another folder, or DT_FOLDER_SPECIAL to indicate an icon that is application-specific.</span></span> <span data-ttu-id="51900-144">DT_FOLDER_LINK は、検索結果のフォルダーで使用されます。</span><span class="sxs-lookup"><span data-stu-id="51900-144">DT_FOLDER_LINK is used with search-results folders.</span></span> 
  
<span data-ttu-id="51900-145">アドレス帳階層テーブルは、これらの必要な列だけでなく、 **PR_CONTAINER_FLAGS**プロパティを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="51900-145">In addition to these required columns, address book hierarchy tables must include the **PR_CONTAINER_FLAGS** property.</span></span> <span data-ttu-id="51900-146">**PR_CONTAINER_FLAGS**は、階層内のコンテナーのさまざまな属性を示し、1 つのコンテナーを区別するために使用します。</span><span class="sxs-lookup"><span data-stu-id="51900-146">**PR_CONTAINER_FLAGS** indicates various attributes about a container in the hierarchy and is used to distinguish one container from another.</span></span> 
  
<span data-ttu-id="51900-147">アドレス帳階層テーブルのオプションのプロパティは、 **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="51900-147">An optional property for address book hierarchy tables is the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="51900-148">メッセージ ストアの階層テーブルの必要な列のセットでこれらのプロパティのとおりです。</span><span class="sxs-lookup"><span data-stu-id="51900-148">Message-store hierarchy tables include these properties in their required column set:</span></span>
  
- <span data-ttu-id="51900-149">**PR_FOLDER_TYPE**([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51900-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="51900-150">**PR_SUBFOLDERS**([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51900-150">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
- <span data-ttu-id="51900-151">**PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51900-151">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="51900-152">**PR_CONTENT_UNREAD**([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51900-152">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
<span data-ttu-id="51900-153">アドレス帳プロバイダーは MAPI の統合のアドレス帳で必要とされるため、階層テーブルの実装で**IMAPITable**メソッドを次をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="51900-153">Address book providers must support the following **IMAPITable** methods in their hierarchy table implementations because they are required by the MAPI integrated address book:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="51900-154">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="51900-154">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |[<span data-ttu-id="51900-155">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="51900-155">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md) <br/> |
|[<span data-ttu-id="51900-156">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="51900-156">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md) <br/> |[<span data-ttu-id="51900-157">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="51900-157">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |
|[<span data-ttu-id="51900-158">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="51900-158">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |[<span data-ttu-id="51900-159">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="51900-159">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |
|[<span data-ttu-id="51900-160">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="51900-160">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |[<span data-ttu-id="51900-161">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="51900-161">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |
|[<span data-ttu-id="51900-162">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="51900-162">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51900-163">関連項目</span><span class="sxs-lookup"><span data-stu-id="51900-163">See also</span></span>



[<span data-ttu-id="51900-164">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="51900-164">MAPI Tables</span></span>](mapi-tables.md)

