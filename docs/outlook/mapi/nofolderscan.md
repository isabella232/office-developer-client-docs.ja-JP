---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3477104cc254ea5f22158b9791d7fd3bd776d819
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801660"
---
# <a name="nofolderscan"></a><span data-ttu-id="89e6b-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="89e6b-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="89e6b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="89e6b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="89e6b-105">Microsoft Office Outlook がストアの連絡先フォルダーをスキャンするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="89e6b-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="89e6b-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="89e6b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89e6b-107">公開されます。</span><span class="sxs-lookup"><span data-stu-id="89e6b-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="89e6b-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)オブジェクト</span><span class="sxs-lookup"><span data-stu-id="89e6b-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="89e6b-109">によって作成されます。</span><span class="sxs-lookup"><span data-stu-id="89e6b-109">Created by:</span></span>  <br/> |<span data-ttu-id="89e6b-110">ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="89e6b-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="89e6b-111">によってアクセスします。</span><span class="sxs-lookup"><span data-stu-id="89e6b-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="89e6b-112">Outlook およびその他のクライアント</span><span class="sxs-lookup"><span data-stu-id="89e6b-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="89e6b-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="89e6b-113">Property type:</span></span>  <br/> |<span data-ttu-id="89e6b-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="89e6b-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="89e6b-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="89e6b-115">Access type:</span></span>  <br/> |<span data-ttu-id="89e6b-116">読み取り専用または読み取り/書き込みによってストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="89e6b-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89e6b-117">備考</span><span class="sxs-lookup"><span data-stu-id="89e6b-117">Remarks</span></span>

<span data-ttu-id="89e6b-118">ストア機能を提供するストア プロバイダーを実装する必要があります[IMAPIProp: IUnknown](imapipropiunknown.md) 、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)の呼び出しに渡されたこれらのプロパティのいずれかのプロパティの有効なタグを返すとします。</span><span class="sxs-lookup"><span data-stu-id="89e6b-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="89e6b-119">これらのプロパティのいずれかのプロパティ タグが[IMAPIProp::GetProps](imapiprop-getprops.md)に渡されると、ストア プロバイダーを使用、正しいプロパティ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="89e6b-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="89e6b-120">ストア プロバイダーには、取得、またはこれらのプロパティを設定するには、 [HrGetOneProp](hrgetoneprop.md)と[HrSetOneProp](hrsetoneprop.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="89e6b-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="89e6b-121">このプロパティの値を取得するには、クライアントはまず[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用して、プロパティ タグを取得して、値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)でこのプロパティのタグを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89e6b-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="89e6b-122">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出すときは、 _lppPropNames_の入力パラメーターで示される[MAPINAMEID](mapinameid.md)構造体の次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="89e6b-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89e6b-123">lpGuid。</span><span class="sxs-lookup"><span data-stu-id="89e6b-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="89e6b-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="89e6b-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="89e6b-125">ulKind。</span><span class="sxs-lookup"><span data-stu-id="89e6b-125">ulKind:</span></span>  <br/> |<span data-ttu-id="89e6b-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="89e6b-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="89e6b-127">Kind.lpwstrName。</span><span class="sxs-lookup"><span data-stu-id="89e6b-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="89e6b-128">L"NoFolderScan"</span><span class="sxs-lookup"><span data-stu-id="89e6b-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="89e6b-129">このプロパティは、Outlook を指定するのには、ストア プロバイダーのパフォーマンスの低下を防ぐためにストア内の連絡先フォルダーをスキャンする方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="89e6b-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="89e6b-130">スキャンを開始する前に存在し、このプロパティの値を調べ、差し込み印刷操作で使用されます。</span><span class="sxs-lookup"><span data-stu-id="89e6b-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="89e6b-131">既定では、このプロパティは、ストアは、Outlook は、ストアの連絡先フォルダーをスキャンできることを意味では公開されません。</span><span class="sxs-lookup"><span data-stu-id="89e6b-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="89e6b-132">プロパティが公開されている場合、値は次のことです。</span><span class="sxs-lookup"><span data-stu-id="89e6b-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="89e6b-133">ゼロ (0): Outlook は、スキャンを実行できます。</span><span class="sxs-lookup"><span data-stu-id="89e6b-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="89e6b-134">ゼロ以外の値: Outlook では、ストアの連絡先フォルダーはスキャンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="89e6b-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    

