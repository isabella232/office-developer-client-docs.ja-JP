---
title: IProviderAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bedec72e8371d0e8aa69415d2f0dc77b4c62ff76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437533"
---
# <a name="iprovideradmin--iunknown"></a><span data-ttu-id="defa5-103">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="defa5-103">IProviderAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="defa5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="defa5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="defa5-105">メッセージサービスのサービスプロバイダーと連携します。</span><span class="sxs-lookup"><span data-stu-id="defa5-105">Works with service providers in a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="defa5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="defa5-106">Header file:</span></span>  <br/> |<span data-ttu-id="defa5-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="defa5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="defa5-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="defa5-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="defa5-109">プロバイダー管理オブジェクト</span><span class="sxs-lookup"><span data-stu-id="defa5-109">Provider administration objects</span></span>  <br/> |
|<span data-ttu-id="defa5-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="defa5-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="defa5-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="defa5-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="defa5-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="defa5-112">Called by:</span></span>  <br/> |<span data-ttu-id="defa5-113">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="defa5-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="defa5-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="defa5-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="defa5-115">IID_IProviderAdmin</span><span class="sxs-lookup"><span data-stu-id="defa5-115">IID_IProviderAdmin</span></span>  <br/> |
|<span data-ttu-id="defa5-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="defa5-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="defa5-117">lpprovideradmin</span><span class="sxs-lookup"><span data-stu-id="defa5-117">LPPROVIDERADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="defa5-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="defa5-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="defa5-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="defa5-119">GetLastError</span></span>](iprovideradmin-getlasterror.md) <br/> |<span data-ttu-id="defa5-120">プロバイダー管理オブジェクトに発生した前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="defa5-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span>  <br/> |
|[<span data-ttu-id="defa5-121">getprovidertable</span><span class="sxs-lookup"><span data-stu-id="defa5-121">GetProviderTable</span></span>](iprovideradmin-getprovidertable.md) <br/> |<span data-ttu-id="defa5-122">メッセージサービスのプロバイダーテーブルへのアクセスを提供します。これには、メッセージサービスのサービスプロバイダーの一覧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="defa5-122">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>  <br/> |
|[<span data-ttu-id="defa5-123">createprovider</span><span class="sxs-lookup"><span data-stu-id="defa5-123">CreateProvider</span></span>](iprovideradmin-createprovider.md) <br/> |<span data-ttu-id="defa5-124">メッセージサービスにサービスプロバイダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="defa5-124">Adds a service provider to the message service.</span></span>  <br/> |
|[<span data-ttu-id="defa5-125">deleteprovider</span><span class="sxs-lookup"><span data-stu-id="defa5-125">DeleteProvider</span></span>](iprovideradmin-deleteprovider.md) <br/> |<span data-ttu-id="defa5-126">メッセージサービスからサービスプロバイダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="defa5-126">Deletes a service provider from the message service.</span></span>  <br/> |
|[<span data-ttu-id="defa5-127">openプロファイル '</span><span class="sxs-lookup"><span data-stu-id="defa5-127">OpenProfileSection</span></span>](iprovideradmin-openprofilesection.md) <br/> |<span data-ttu-id="defa5-128">現在のプロファイルからプロファイルセクションを開き、さらにアクセスできるように[IProfSect](iprofsectimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="defa5-128">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="defa5-129">注釈</span><span class="sxs-lookup"><span data-stu-id="defa5-129">Remarks</span></span>

<span data-ttu-id="defa5-130">クライアントは、 [IMsgServiceAdmin:: adminproviders](imsgserviceadmin-adminproviders.md)メソッドを呼び出して、 **IProviderAdmin**インターフェイスへのポインターを取得できます。サービスプロバイダーのメッセージサービスのエントリポイント関数が呼び出されると、 **IProviderAdmin**ポインターが渡されます。</span><span class="sxs-lookup"><span data-stu-id="defa5-130">Clients can get a pointer to an **IProviderAdmin** interface by calling the [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) method; service providers are passed an **IProviderAdmin** pointer when their message service's entry point function is called.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="defa5-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="defa5-131">See also</span></span>



[<span data-ttu-id="defa5-132">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="defa5-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

