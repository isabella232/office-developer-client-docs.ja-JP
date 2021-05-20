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
# <a name="iprovideradmin--iunknown"></a><span data-ttu-id="b057d-103">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b057d-103">IProviderAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="b057d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b057d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b057d-105">メッセージ サービスのサービス プロバイダーと動作します。</span><span class="sxs-lookup"><span data-stu-id="b057d-105">Works with service providers in a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b057d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b057d-106">Header file:</span></span>  <br/> |<span data-ttu-id="b057d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b057d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b057d-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="b057d-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b057d-109">プロバイダー管理オブジェクト</span><span class="sxs-lookup"><span data-stu-id="b057d-109">Provider administration objects</span></span>  <br/> |
|<span data-ttu-id="b057d-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="b057d-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b057d-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="b057d-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="b057d-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="b057d-112">Called by:</span></span>  <br/> |<span data-ttu-id="b057d-113">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="b057d-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="b057d-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="b057d-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b057d-115">IID_IProviderAdmin</span><span class="sxs-lookup"><span data-stu-id="b057d-115">IID_IProviderAdmin</span></span>  <br/> |
|<span data-ttu-id="b057d-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="b057d-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b057d-117">LPPROVIDERADMIN</span><span class="sxs-lookup"><span data-stu-id="b057d-117">LPPROVIDERADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b057d-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="b057d-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b057d-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="b057d-119">GetLastError</span></span>](iprovideradmin-getlasterror.md) <br/> |<span data-ttu-id="b057d-120">プロバイダー管理オブジェクト [に発生](mapierror.md) した以前のエラーに関する情報を含む MAPIERROR 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="b057d-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span>  <br/> |
|[<span data-ttu-id="b057d-121">GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="b057d-121">GetProviderTable</span></span>](iprovideradmin-getprovidertable.md) <br/> |<span data-ttu-id="b057d-122">メッセージ サービスのプロバイダー テーブル 、メッセージ サービス内のサービス プロバイダーの一覧へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b057d-122">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>  <br/> |
|[<span data-ttu-id="b057d-123">CreateProvider</span><span class="sxs-lookup"><span data-stu-id="b057d-123">CreateProvider</span></span>](iprovideradmin-createprovider.md) <br/> |<span data-ttu-id="b057d-124">サービス プロバイダーをメッセージ サービスに追加します。</span><span class="sxs-lookup"><span data-stu-id="b057d-124">Adds a service provider to the message service.</span></span>  <br/> |
|[<span data-ttu-id="b057d-125">DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="b057d-125">DeleteProvider</span></span>](iprovideradmin-deleteprovider.md) <br/> |<span data-ttu-id="b057d-126">メッセージ サービスからサービス プロバイダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="b057d-126">Deletes a service provider from the message service.</span></span>  <br/> |
|[<span data-ttu-id="b057d-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="b057d-127">OpenProfileSection</span></span>](iprovideradmin-openprofilesection.md) <br/> |<span data-ttu-id="b057d-128">現在のプロファイルからプロファイル セクションを開き、さらにアクセスする [IProfSect](iprofsectimapiprop.md) ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="b057d-128">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b057d-129">注釈</span><span class="sxs-lookup"><span data-stu-id="b057d-129">Remarks</span></span>

<span data-ttu-id="b057d-130">クライアントは [、IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)メソッドを呼び出すことによって **、IProviderAdmin** インターフェイスへのポインターを取得できます。メッセージ サービスのエントリ ポイント関数が呼び出された場合、サービス プロバイダーは **IProviderAdmin** ポインターを渡されます。</span><span class="sxs-lookup"><span data-stu-id="b057d-130">Clients can get a pointer to an **IProviderAdmin** interface by calling the [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) method; service providers are passed an **IProviderAdmin** pointer when their message service's entry point function is called.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b057d-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="b057d-131">See also</span></span>



[<span data-ttu-id="b057d-132">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="b057d-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

