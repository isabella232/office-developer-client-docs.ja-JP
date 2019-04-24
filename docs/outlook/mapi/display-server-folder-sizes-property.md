---
title: サーバーフォルダーのサイズプロパティを表示する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337080"
---
# <a name="display-server-folder-sizes-property"></a><span data-ttu-id="b1e51-103">サーバーフォルダーのサイズプロパティを表示する</span><span class="sxs-lookup"><span data-stu-id="b1e51-103">Display Server Folder Sizes Property</span></span>

  
  
<span data-ttu-id="b1e51-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1e51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1e51-105">サーバー上の指定されたフォルダーのサイズが [Outlook**フォルダーサイズ**] ダイアログボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b1e51-105">Displays the sizes of specified folders on the server in the Outlook **Folder Size** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b1e51-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b1e51-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1e51-107">公開:</span><span class="sxs-lookup"><span data-stu-id="b1e51-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="b1e51-108">[IMsgStore: imapiprop](imsgstoreimapiprop.md)オブジェクト</span><span class="sxs-lookup"><span data-stu-id="b1e51-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="b1e51-109">作成者:</span><span class="sxs-lookup"><span data-stu-id="b1e51-109">Created by:</span></span>  <br/> |<span data-ttu-id="b1e51-110">ストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="b1e51-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="b1e51-111">アクセス先:</span><span class="sxs-lookup"><span data-stu-id="b1e51-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="b1e51-112">Outlook およびその他のクライアント</span><span class="sxs-lookup"><span data-stu-id="b1e51-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="b1e51-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="b1e51-113">Property type:</span></span>  <br/> |<span data-ttu-id="b1e51-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b1e51-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b1e51-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="b1e51-115">Access type:</span></span>  <br/> |<span data-ttu-id="b1e51-116">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="b1e51-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1e51-117">解説</span><span class="sxs-lookup"><span data-stu-id="b1e51-117">Remarks</span></span>

<span data-ttu-id="b1e51-118">ストアの機能を提供するには、ストアプロバイダーが[imapiprop: IUnknown](imapipropiunknown.md)を実装し、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)呼び出しに渡されるこれらのプロパティに対して有効なプロパティタグを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1e51-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="b1e51-119">これらのプロパティのいずれかのプロパティタグが[imapiprop:: GetProps](imapiprop-getprops.md)に渡されると、ストアプロバイダーは、適切なプロパティ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1e51-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="b1e51-120">ストアプロバイダーは、 [hrgetoneprop](hrgetoneprop.md)および[hrgetoneprop](hrsetoneprop.md)を呼び出して、これらのプロパティを取得または設定できます。</span><span class="sxs-lookup"><span data-stu-id="b1e51-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="b1e51-121">このプロパティの値を取得するには、クライアントはまず[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を使用してプロパティタグを取得し、次に[imapiprop:: GetProps](imapiprop-getprops.md)でこのプロパティタグを指定して値を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1e51-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="b1e51-122">[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lpppropnames_でポイントされている[mapinameid](mapinameid.md)構造に次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1e51-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1e51-123">lpguid:</span><span class="sxs-lookup"><span data-stu-id="b1e51-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="b1e51-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="b1e51-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="b1e51-125">ulkind:</span><span class="sxs-lookup"><span data-stu-id="b1e51-125">ulKind:</span></span>  <br/> |<span data-ttu-id="b1e51-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="b1e51-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="b1e51-127">種類が lpwstrname:</span><span class="sxs-lookup"><span data-stu-id="b1e51-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="b1e51-128">L "urn: スキーマ-microsoft-com: office: outlook # serverfoldersizes"</span><span class="sxs-lookup"><span data-stu-id="b1e51-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span></span>  <br/> |
   
<span data-ttu-id="b1e51-129">このプロパティは、Microsoft Outlook 2003 Service Pack (SP) 1 でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b1e51-129">This property is supported in Microsoft Outlook 2003 Service Pack (SP) 1.</span></span> <span data-ttu-id="b1e51-130">outlook のバージョンが outlook 2003 SP 1 より前の場合、またはその値が**false**の場合、outlook はローカルストア上のフォルダーのサイズのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="b1e51-130">If the version of Outlook is earlier than Outlook 2003 SP 1, or if its value is **false**, Outlook will display only the sizes of folders on the local store.</span></span> <span data-ttu-id="b1e51-131">outlook 2003 SP 1 を使用するストアにこのプロパティが設定されている場合、outlook はサーバー上の指定された各フォルダーとローカルドライブのサイズを照会します。</span><span class="sxs-lookup"><span data-stu-id="b1e51-131">If this property is set on a store that uses Outlook 2003 SP 1, Outlook will query for the size of each specified folder on the server and the local drive.</span></span> 
  
<span data-ttu-id="b1e51-132">サーバー上のフォルダーサイズを照会するには、Outlook は[IMsgStore:: openentry](imsgstore-openentry.md)を使用してストアのフォルダーを開き、フラグ**MAPI_NO_CACHE**を渡してから、 **PR_MESSAGE_SIZE_EXTENDED**に対するクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="b1e51-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then it queries for **PR_MESSAGE_SIZE_EXTENDED**.</span></span> <span data-ttu-id="b1e51-133">その後、ストアプロバイダーは、サーバー上のフォルダーサイズを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1e51-133">The store provider should then return the folder size on the server.</span></span>
  
<span data-ttu-id="b1e51-134">ローカルドライブのフォルダーのサイズを照会するには、 **MAPI_NO_CACHE**フラグを指定せずにフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="b1e51-134">To query for the size of a folder on the local drive, Outlook opens the folder without the **MAPI_NO_CACHE** flag.</span></span> <span data-ttu-id="b1e51-135">その後、 **PR_MESSAGE_SIZE_EXTENDED**に対するクエリを行います。ストアプロバイダーは、ローカルドライブ上の指定されたフォルダーのサイズを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1e51-135">It then queries for **PR_MESSAGE_SIZE_EXTENDED**; the store provider should return the size of the specified folder on the local drive.</span></span>
  
<span data-ttu-id="b1e51-136">このプロパティセットを使用すると、ストアのコンテンツをサーバーに同期するストアプロバイダーは、Outlook の [**フォルダーサイズ**] ダイアログボックスで、サーバー上のフォルダーサイズデータを表示できます。</span><span class="sxs-lookup"><span data-stu-id="b1e51-136">With this property set, store providers that synchronize store contents to a server can display folder size data on the server in the Outlook **Folder Size** dialog box.</span></span> <span data-ttu-id="b1e51-137">その後、ユーザーは現在のサーバー記憶域の使用状況をサーバークォータと比較できます。</span><span class="sxs-lookup"><span data-stu-id="b1e51-137">Users can then compare their current server storage usage with server quotas.</span></span> 
  

