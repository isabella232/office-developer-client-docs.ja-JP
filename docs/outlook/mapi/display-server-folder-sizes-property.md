---
title: '[サーバー フォルダーサイズの表示] プロパティ'
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434551"
---
# <a name="display-server-folder-sizes-property"></a><span data-ttu-id="22836-103">[サーバー フォルダーサイズの表示] プロパティ</span><span class="sxs-lookup"><span data-stu-id="22836-103">Display Server Folder Sizes Property</span></span>

  
  
<span data-ttu-id="22836-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22836-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22836-105">サーバー上の指定したフォルダーのサイズを [フォルダー のサイズ] ダイアログ ボックスOutlook **表示** します。</span><span class="sxs-lookup"><span data-stu-id="22836-105">Displays the sizes of specified folders on the server in the Outlook **Folder Size** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="22836-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="22836-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22836-107">次の場合に公開されます。</span><span class="sxs-lookup"><span data-stu-id="22836-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="22836-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) オブジェクト</span><span class="sxs-lookup"><span data-stu-id="22836-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="22836-109">作成者:</span><span class="sxs-lookup"><span data-stu-id="22836-109">Created by:</span></span>  <br/> |<span data-ttu-id="22836-110">ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="22836-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="22836-111">アクセス者:</span><span class="sxs-lookup"><span data-stu-id="22836-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="22836-112">Outlookクライアント</span><span class="sxs-lookup"><span data-stu-id="22836-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="22836-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="22836-113">Property type:</span></span>  <br/> |<span data-ttu-id="22836-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="22836-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="22836-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="22836-115">Access type:</span></span>  <br/> |<span data-ttu-id="22836-116">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="22836-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22836-117">注釈</span><span class="sxs-lookup"><span data-stu-id="22836-117">Remarks</span></span>

<span data-ttu-id="22836-118">ストア機能を提供するには、ストア プロバイダーが [IMAPIProp : IUnknown](imapipropiunknown.md) を実装し [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) 呼び出しに渡されるこれらのプロパティの有効なプロパティ タグを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="22836-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="22836-119">これらのプロパティのプロパティ タグが [IMAPIProp::GetProps](imapiprop-getprops.md)に渡される場合、ストア プロバイダーは正しいプロパティ値も返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="22836-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="22836-120">ストア プロバイダーは [、HrGetOneProp](hrgetoneprop.md) と [HrSetOneProp](hrsetoneprop.md) を呼び出して、これらのプロパティを取得または設定できます。</span><span class="sxs-lookup"><span data-stu-id="22836-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="22836-121">このプロパティの値を取得するには、まず [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) を使用してプロパティ タグを取得し [、IMAPIProp::GetProps](imapiprop-getprops.md) でこのプロパティ タグを指定して値を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="22836-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="22836-122">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lppPropNames_ が指す [MAPINAMEID](mapinameid.md)構造体に次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="22836-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22836-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="22836-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="22836-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="22836-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="22836-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="22836-125">ulKind:</span></span>  <br/> |<span data-ttu-id="22836-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="22836-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="22836-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="22836-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="22836-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span><span class="sxs-lookup"><span data-stu-id="22836-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span></span>  <br/> |
   
<span data-ttu-id="22836-129">このプロパティは、Microsoft Outlook 2003 Service Pack (SP) 1 でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="22836-129">This property is supported in Microsoft Outlook 2003 Service Pack (SP) 1.</span></span> <span data-ttu-id="22836-130">Outlook のバージョンが Outlook 2003 SP 1 より前の場合、または値が **false** の場合、Outlook はローカル ストア上のフォルダーのサイズのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="22836-130">If the version of Outlook is earlier than Outlook 2003 SP 1, or if its value is **false**, Outlook will display only the sizes of folders on the local store.</span></span> <span data-ttu-id="22836-131">Outlook 2003 SP 1 を使用するストアでこのプロパティが設定されている場合、Outlook はサーバー上の指定された各フォルダーとローカル ドライブのサイズを照会します。</span><span class="sxs-lookup"><span data-stu-id="22836-131">If this property is set on a store that uses Outlook 2003 SP 1, Outlook will query for the size of each specified folder on the server and the local drive.</span></span> 
  
<span data-ttu-id="22836-132">サーバー上のフォルダー サイズを照会するために、Outlook は [IMsgStore::OpenEntry](imsgstore-openentry.md)を使用してストア上のフォルダーを開き、フラグ **MAPI_NO_CACHE** を渡し、PR_MESSAGE_SIZE_EXTENDED を **照会します**。</span><span class="sxs-lookup"><span data-stu-id="22836-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then it queries for **PR_MESSAGE_SIZE_EXTENDED**.</span></span> <span data-ttu-id="22836-133">ストア プロバイダーは、サーバー上のフォルダー サイズを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="22836-133">The store provider should then return the folder size on the server.</span></span>
  
<span data-ttu-id="22836-134">ローカル ドライブ上のフォルダーのサイズを照会するには、Outlookフラグなしでフォルダー **MAPI_NO_CACHE** します。</span><span class="sxs-lookup"><span data-stu-id="22836-134">To query for the size of a folder on the local drive, Outlook opens the folder without the **MAPI_NO_CACHE** flag.</span></span> <span data-ttu-id="22836-135">次に、クエリを実行 **PR_MESSAGE_SIZE_EXTENDED。** ストア プロバイダーは、ローカル ドライブ上の指定したフォルダーのサイズを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="22836-135">It then queries for **PR_MESSAGE_SIZE_EXTENDED**; the store provider should return the size of the specified folder on the local drive.</span></span>
  
<span data-ttu-id="22836-136">このプロパティセットを使用すると、ストアの内容をサーバーに同期するストア プロバイダーは、[フォルダー サイズ] ダイアログ ボックスの **[Outlook]** にフォルダー サイズデータを表示できます。</span><span class="sxs-lookup"><span data-stu-id="22836-136">With this property set, store providers that synchronize store contents to a server can display folder size data on the server in the Outlook **Folder Size** dialog box.</span></span> <span data-ttu-id="22836-137">その後、ユーザーは現在のサーバー ストレージ使用量とサーバー クォータを比較できます。</span><span class="sxs-lookup"><span data-stu-id="22836-137">Users can then compare their current server storage usage with server quotas.</span></span> 
  

