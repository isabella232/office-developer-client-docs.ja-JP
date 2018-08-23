---
title: サーバー フォルダーのサイズ プロパティを表示する
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
ms.openlocfilehash: f1ec10bde39f853a80540b48216478edc4e41f12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584311"
---
# <a name="display-server-folder-sizes-property"></a><span data-ttu-id="65ce0-103">サーバー フォルダーのサイズ プロパティを表示する</span><span class="sxs-lookup"><span data-stu-id="65ce0-103">Display Server Folder Sizes Property</span></span>

  
  
<span data-ttu-id="65ce0-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65ce0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65ce0-105">Outlook の **[フォルダー サイズ**] ダイアログ ボックスでサーバー上の指定したフォルダーのサイズを表示します。</span><span class="sxs-lookup"><span data-stu-id="65ce0-105">Displays the sizes of specified folders on the server in the Outlook **Folder Size** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="65ce0-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="65ce0-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65ce0-107">公開されます。</span><span class="sxs-lookup"><span data-stu-id="65ce0-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="65ce0-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)オブジェクト</span><span class="sxs-lookup"><span data-stu-id="65ce0-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="65ce0-109">によって作成されます。</span><span class="sxs-lookup"><span data-stu-id="65ce0-109">Created by:</span></span>  <br/> |<span data-ttu-id="65ce0-110">ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="65ce0-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="65ce0-111">によってアクセスします。</span><span class="sxs-lookup"><span data-stu-id="65ce0-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="65ce0-112">Outlook およびその他のクライアント</span><span class="sxs-lookup"><span data-stu-id="65ce0-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="65ce0-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="65ce0-113">Property type:</span></span>  <br/> |<span data-ttu-id="65ce0-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="65ce0-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="65ce0-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="65ce0-115">Access type:</span></span>  <br/> |<span data-ttu-id="65ce0-116">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="65ce0-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65ce0-117">注釈</span><span class="sxs-lookup"><span data-stu-id="65ce0-117">Remarks</span></span>

<span data-ttu-id="65ce0-118">ストア機能を提供するストア プロバイダーを実装する必要があります[IMAPIProp: IUnknown](imapipropiunknown.md) 、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)の呼び出しに渡されたこれらのプロパティのいずれかのプロパティの有効なタグを返すとします。</span><span class="sxs-lookup"><span data-stu-id="65ce0-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="65ce0-119">これらのプロパティのいずれかのプロパティ タグが[IMAPIProp::GetProps](imapiprop-getprops.md)に渡されると、ストア プロバイダーを使用、正しいプロパティ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="65ce0-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="65ce0-120">ストア プロバイダーには、取得、またはこれらのプロパティを設定するには、 [HrGetOneProp](hrgetoneprop.md)と[HrSetOneProp](hrsetoneprop.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="65ce0-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="65ce0-121">このプロパティの値を取得するには、クライアントはまず[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用して、プロパティ タグを取得して、値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)でこのプロパティのタグを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65ce0-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="65ce0-122">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出すときは、 _lppPropNames_の入力パラメーターで示される[MAPINAMEID](mapinameid.md)構造体の次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="65ce0-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65ce0-123">lpGuid。</span><span class="sxs-lookup"><span data-stu-id="65ce0-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="65ce0-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="65ce0-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="65ce0-125">ulKind。</span><span class="sxs-lookup"><span data-stu-id="65ce0-125">ulKind:</span></span>  <br/> |<span data-ttu-id="65ce0-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="65ce0-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="65ce0-127">Kind.lpwstrName。</span><span class="sxs-lookup"><span data-stu-id="65ce0-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="65ce0-128">L"urn: スキーマ-マイクロソフト-com:office:outlook #serverfoldersizes」</span><span class="sxs-lookup"><span data-stu-id="65ce0-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span></span>  <br/> |
   
<span data-ttu-id="65ce0-129">Microsoft Outlook 2003 Service Pack (SP) 1年では、このプロパティがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="65ce0-129">This property is supported in Microsoft Outlook 2003 Service Pack (SP) 1.</span></span> <span data-ttu-id="65ce0-130">Outlook のバージョンが Outlook 2003 SP 1 より前の場合、またはその値が**false**の場合は、ローカル ストアにフォルダーのサイズのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="65ce0-130">If the version of Outlook is earlier than Outlook 2003 SP 1, or if its value is **false**, Outlook will display only the sizes of folders on the local store.</span></span> <span data-ttu-id="65ce0-131">このプロパティは、Outlook 2003 SP 1 を使用するストアに設定されている場合、Outlook は、サーバーとローカル ドライブに指定した各フォルダーのサイズを照会します。</span><span class="sxs-lookup"><span data-stu-id="65ce0-131">If this property is set on a store that uses Outlook 2003 SP 1, Outlook will query for the size of each specified folder on the server and the local drive.</span></span> 
  
<span data-ttu-id="65ce0-132">クエリを実行するサーバー上のフォルダーのサイズの Outlook フォルダーを開くと、ストアで[IMsgStore::OpenEntry](imsgstore-openentry.md)、 **MAPI_NO_CACHE**、このフラグを渡すと、 **PR_MESSAGE_SIZE_EXTENDED**を照会し、.</span><span class="sxs-lookup"><span data-stu-id="65ce0-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then it queries for **PR_MESSAGE_SIZE_EXTENDED**.</span></span> <span data-ttu-id="65ce0-133">ストア プロバイダーは、サーバー上でフォルダーのサイズを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="65ce0-133">The store provider should then return the folder size on the server.</span></span>
  
<span data-ttu-id="65ce0-134">クエリを実行するローカル ドライブ上のフォルダーのサイズは、Outlook は、 **MAPI_NO_CACHE**フラグを設定しない] フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="65ce0-134">To query for the size of a folder on the local drive, Outlook opens the folder without the **MAPI_NO_CACHE** flag.</span></span> <span data-ttu-id="65ce0-135">それに基づいて、クエリの**PR_MESSAGE_SIZE_EXTENDED**です。ストア プロバイダーは、ローカル ドライブ上の指定したフォルダーのサイズを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="65ce0-135">It then queries for **PR_MESSAGE_SIZE_EXTENDED**; the store provider should return the size of the specified folder on the local drive.</span></span>
  
<span data-ttu-id="65ce0-136">このプロパティを設定するストア プロバイダーをサーバーにストアの内容を同期は、Outlook の **[フォルダー サイズ**] ダイアログ ボックスでサーバーにフォルダーのサイズのデータを表示できます。</span><span class="sxs-lookup"><span data-stu-id="65ce0-136">With this property set, store providers that synchronize store contents to a server can display folder size data on the server in the Outlook **Folder Size** dialog box.</span></span> <span data-ttu-id="65ce0-137">ユーザーは、現在のサーバー ストレージ使用状況とサーバーのクォータを比較し、ことができます。</span><span class="sxs-lookup"><span data-stu-id="65ce0-137">Users can then compare their current server storage usage with server quotas.</span></span> 
  

