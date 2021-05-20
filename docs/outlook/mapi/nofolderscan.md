---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fc5f5a42e2b1e57374ff80a9333b927cc8dba120
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436812"
---
# <a name="nofolderscan"></a><span data-ttu-id="40e06-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="40e06-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="40e06-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40e06-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40e06-105">ストアの連絡先Microsoft Office Outlookスキャンするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="40e06-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="40e06-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="40e06-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40e06-107">次の場合に公開されます。</span><span class="sxs-lookup"><span data-stu-id="40e06-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="40e06-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) オブジェクト</span><span class="sxs-lookup"><span data-stu-id="40e06-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="40e06-109">作成者:</span><span class="sxs-lookup"><span data-stu-id="40e06-109">Created by:</span></span>  <br/> |<span data-ttu-id="40e06-110">ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="40e06-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="40e06-111">アクセス者:</span><span class="sxs-lookup"><span data-stu-id="40e06-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="40e06-112">Outlookクライアント</span><span class="sxs-lookup"><span data-stu-id="40e06-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="40e06-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="40e06-113">Property type:</span></span>  <br/> |<span data-ttu-id="40e06-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="40e06-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="40e06-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="40e06-115">Access type:</span></span>  <br/> |<span data-ttu-id="40e06-116">ストア プロバイダーに応じて読み取り専用または読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="40e06-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40e06-117">注釈</span><span class="sxs-lookup"><span data-stu-id="40e06-117">Remarks</span></span>

<span data-ttu-id="40e06-118">ストア機能を提供するには、ストア プロバイダーが [IMAPIProp : IUnknown](imapipropiunknown.md) を実装し [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) 呼び出しに渡されるこれらのプロパティの有効なプロパティ タグを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="40e06-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="40e06-119">これらのプロパティのプロパティ タグが [IMAPIProp::GetProps](imapiprop-getprops.md)に渡される場合、ストア プロバイダーは正しいプロパティ値も返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="40e06-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="40e06-120">ストア プロバイダーは [、HrGetOneProp](hrgetoneprop.md) と [HrSetOneProp](hrsetoneprop.md) を呼び出して、これらのプロパティを取得または設定できます。</span><span class="sxs-lookup"><span data-stu-id="40e06-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="40e06-121">このプロパティの値を取得するには、まず [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) を使用してプロパティ タグを取得し [、IMAPIProp::GetProps](imapiprop-getprops.md) でこのプロパティ タグを指定して値を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40e06-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="40e06-122">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lppPropNames_ が指す [MAPINAMEID](mapinameid.md)構造体に次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="40e06-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40e06-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="40e06-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="40e06-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="40e06-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="40e06-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="40e06-125">ulKind:</span></span>  <br/> |<span data-ttu-id="40e06-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="40e06-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="40e06-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="40e06-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="40e06-128">L"NoFolderScan"</span><span class="sxs-lookup"><span data-stu-id="40e06-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="40e06-129">このプロパティを使用すると、ストア プロバイダーは、パフォーマンスの低下を避けるために、Outlook連絡先フォルダーをスキャンしないように指定できます。</span><span class="sxs-lookup"><span data-stu-id="40e06-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="40e06-130">これは、スキャンを開始する前に、Outlookプロパティの存在と値をチェックする差し込み印刷操作で使用されます。</span><span class="sxs-lookup"><span data-stu-id="40e06-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="40e06-131">既定では、このプロパティはストアで公開されません。つまり、Outlook連絡先フォルダーをスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="40e06-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="40e06-132">プロパティが公開されている場合は、次の値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="40e06-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="40e06-133">ゼロ (0): Outlookを実行できます。</span><span class="sxs-lookup"><span data-stu-id="40e06-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="40e06-134">ゼロ以外の値: ストアOutlook連絡先フォルダーをスキャンしない必要があります。</span><span class="sxs-lookup"><span data-stu-id="40e06-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    

