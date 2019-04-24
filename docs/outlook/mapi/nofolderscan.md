---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fc5f5a42e2b1e57374ff80a9333b927cc8dba120
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326265"
---
# <a name="nofolderscan"></a><span data-ttu-id="dc5d8-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="dc5d8-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="dc5d8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc5d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc5d8-105">Microsoft Office Outlook がストアの連絡先フォルダーをスキャンする必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="dc5d8-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dc5d8-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="dc5d8-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc5d8-107">公開:</span><span class="sxs-lookup"><span data-stu-id="dc5d8-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="dc5d8-108">[IMsgStore: imapiprop](imsgstoreimapiprop.md)オブジェクト</span><span class="sxs-lookup"><span data-stu-id="dc5d8-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="dc5d8-109">作成者:</span><span class="sxs-lookup"><span data-stu-id="dc5d8-109">Created by:</span></span>  <br/> |<span data-ttu-id="dc5d8-110">ストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="dc5d8-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="dc5d8-111">アクセス先:</span><span class="sxs-lookup"><span data-stu-id="dc5d8-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="dc5d8-112">Outlook およびその他のクライアント</span><span class="sxs-lookup"><span data-stu-id="dc5d8-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="dc5d8-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="dc5d8-113">Property type:</span></span>  <br/> |<span data-ttu-id="dc5d8-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dc5d8-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dc5d8-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="dc5d8-115">Access type:</span></span>  <br/> |<span data-ttu-id="dc5d8-116">ストアプロバイダーに応じて読み取り専用または読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="dc5d8-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc5d8-117">解説</span><span class="sxs-lookup"><span data-stu-id="dc5d8-117">Remarks</span></span>

<span data-ttu-id="dc5d8-118">ストアの機能を提供するには、ストアプロバイダーが[imapiprop: IUnknown](imapipropiunknown.md)を実装し、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)呼び出しに渡されるこれらのプロパティに対して有効なプロパティタグを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc5d8-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="dc5d8-119">これらのプロパティのいずれかのプロパティタグが[imapiprop:: GetProps](imapiprop-getprops.md)に渡されると、ストアプロバイダーは、適切なプロパティ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc5d8-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="dc5d8-120">ストアプロバイダーは、 [hrgetoneprop](hrgetoneprop.md)および[hrgetoneprop](hrsetoneprop.md)を呼び出して、これらのプロパティを取得または設定できます。</span><span class="sxs-lookup"><span data-stu-id="dc5d8-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="dc5d8-121">このプロパティの値を取得するには、クライアントはまず[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を使用してプロパティタグを取得し、次に[imapiprop:: GetProps](imapiprop-getprops.md)でこのプロパティタグを指定して値を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc5d8-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="dc5d8-122">[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lpppropnames_でポイントされている[mapinameid](mapinameid.md)構造に次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="dc5d8-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc5d8-123">lpguid:</span><span class="sxs-lookup"><span data-stu-id="dc5d8-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="dc5d8-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="dc5d8-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="dc5d8-125">ulkind:</span><span class="sxs-lookup"><span data-stu-id="dc5d8-125">ulKind:</span></span>  <br/> |<span data-ttu-id="dc5d8-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="dc5d8-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="dc5d8-127">種類が lpwstrname:</span><span class="sxs-lookup"><span data-stu-id="dc5d8-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="dc5d8-128">L "nofolderscan"</span><span class="sxs-lookup"><span data-stu-id="dc5d8-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="dc5d8-129">このプロパティは、ストアプロバイダーが、パフォーマンスの低下を回避するためにストア内の連絡先フォルダーをスキャンしないように指定する方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="dc5d8-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="dc5d8-130">これは、Outlook がスキャンを開始する前に、このプロパティのプレゼンスと値をチェックする差し込み印刷操作で使用されます。</span><span class="sxs-lookup"><span data-stu-id="dc5d8-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="dc5d8-131">既定では、このプロパティはストアに公開されていないため、Outlook はストアの連絡先フォルダーをスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="dc5d8-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="dc5d8-132">プロパティが公開されている場合は、次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="dc5d8-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="dc5d8-133">ゼロ (0): Outlook はスキャンを実行できます。</span><span class="sxs-lookup"><span data-stu-id="dc5d8-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="dc5d8-134">0以外の値: Outlook は、ストア上の連絡先フォルダーをスキャンしません。</span><span class="sxs-lookup"><span data-stu-id="dc5d8-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    

