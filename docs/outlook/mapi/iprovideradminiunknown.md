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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 559680b9ca4ea5be85718d8f9692df93f77b0edf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585753"
---
# <a name="iprovideradmin--iunknown"></a><span data-ttu-id="ee984-103">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee984-103">IProviderAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="ee984-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee984-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee984-105">メッセージ サービスのサービス プロバイダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="ee984-105">Works with service providers in a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee984-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ee984-106">Header file:</span></span>  <br/> |<span data-ttu-id="ee984-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee984-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ee984-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="ee984-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ee984-109">プロバイダー管理オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ee984-109">Provider administration objects</span></span>  <br/> |
|<span data-ttu-id="ee984-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="ee984-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ee984-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="ee984-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="ee984-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee984-112">Called by:</span></span>  <br/> |<span data-ttu-id="ee984-113">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="ee984-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="ee984-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="ee984-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ee984-115">IID_IProviderAdmin</span><span class="sxs-lookup"><span data-stu-id="ee984-115">IID_IProviderAdmin</span></span>  <br/> |
|<span data-ttu-id="ee984-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="ee984-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ee984-117">LPPROVIDERADMIN</span><span class="sxs-lookup"><span data-stu-id="ee984-117">LPPROVIDERADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ee984-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="ee984-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ee984-119">発生しました</span><span class="sxs-lookup"><span data-stu-id="ee984-119">GetLastError</span></span>](iprovideradmin-getlasterror.md) <br/> |<span data-ttu-id="ee984-120">プロバイダーの管理オブジェクトに発生した前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="ee984-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span>  <br/> |
|[<span data-ttu-id="ee984-121">GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="ee984-121">GetProviderTable</span></span>](iprovideradmin-getprovidertable.md) <br/> |<span data-ttu-id="ee984-122">メッセージ サービスのプロバイダーのテーブル、メッセージ サービスのサービス プロバイダーの一覧へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="ee984-122">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>  <br/> |
|[<span data-ttu-id="ee984-123">CreateProvider</span><span class="sxs-lookup"><span data-stu-id="ee984-123">CreateProvider</span></span>](iprovideradmin-createprovider.md) <br/> |<span data-ttu-id="ee984-124">メッセージ サービスにサービス プロバイダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="ee984-124">Adds a service provider to the message service.</span></span>  <br/> |
|[<span data-ttu-id="ee984-125">DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="ee984-125">DeleteProvider</span></span>](iprovideradmin-deleteprovider.md) <br/> |<span data-ttu-id="ee984-126">メッセージ サービスからサービス プロバイダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="ee984-126">Deletes a service provider from the message service.</span></span>  <br/> |
|[<span data-ttu-id="ee984-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="ee984-127">OpenProfileSection</span></span>](iprovideradmin-openprofilesection.md) <br/> |<span data-ttu-id="ee984-128">現在のプロファイルからプロファイルのセクションを開き、さらにアクセスするための[IProfSect](iprofsectimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="ee984-128">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee984-129">注釈</span><span class="sxs-lookup"><span data-stu-id="ee984-129">Remarks</span></span>

<span data-ttu-id="ee984-130">クライアントは、 [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)メソッドを呼び出すことによって**IProviderAdmin**インターフェイスにポインターを取得することができます。メッセージ サービスのエントリ ポイント関数が呼び出されたときに、サービス プロバイダーは、 **IProviderAdmin**ポインターに渡されます。</span><span class="sxs-lookup"><span data-stu-id="ee984-130">Clients can get a pointer to an **IProviderAdmin** interface by calling the [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) method; service providers are passed an **IProviderAdmin** pointer when their message service's entry point function is called.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee984-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee984-131">See also</span></span>



[<span data-ttu-id="ee984-132">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ee984-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

