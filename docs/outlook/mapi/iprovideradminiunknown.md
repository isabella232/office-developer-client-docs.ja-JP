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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 41195a49d1bf3566c81fe6e97697012209cbc5ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801153"
---
# <a name="iprovideradmin--iunknown"></a><span data-ttu-id="5d311-103">IProviderAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5d311-103">IProviderAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="5d311-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d311-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d311-105">メッセージ サービスのサービス プロバイダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="5d311-105">Works with service providers in a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d311-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5d311-106">Header file:</span></span>  <br/> |<span data-ttu-id="5d311-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d311-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5d311-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="5d311-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="5d311-109">プロバイダー管理オブジェクト</span><span class="sxs-lookup"><span data-stu-id="5d311-109">Provider administration objects</span></span>  <br/> |
|<span data-ttu-id="5d311-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="5d311-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="5d311-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="5d311-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="5d311-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5d311-112">Called by:</span></span>  <br/> |<span data-ttu-id="5d311-113">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="5d311-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="5d311-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="5d311-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5d311-115">IID_IProviderAdmin</span><span class="sxs-lookup"><span data-stu-id="5d311-115">IID_IProviderAdmin</span></span>  <br/> |
|<span data-ttu-id="5d311-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="5d311-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="5d311-117">LPPROVIDERADMIN</span><span class="sxs-lookup"><span data-stu-id="5d311-117">LPPROVIDERADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5d311-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="5d311-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5d311-119">発生しました</span><span class="sxs-lookup"><span data-stu-id="5d311-119">GetLastError</span></span>](iprovideradmin-getlasterror.md) <br/> |<span data-ttu-id="5d311-120">プロバイダーの管理オブジェクトに発生した前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="5d311-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span>  <br/> |
|[<span data-ttu-id="5d311-121">GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="5d311-121">GetProviderTable</span></span>](iprovideradmin-getprovidertable.md) <br/> |<span data-ttu-id="5d311-122">メッセージ サービスのプロバイダーのテーブル、メッセージ サービスのサービス プロバイダーの一覧へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="5d311-122">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>  <br/> |
|[<span data-ttu-id="5d311-123">CreateProvider</span><span class="sxs-lookup"><span data-stu-id="5d311-123">CreateProvider</span></span>](iprovideradmin-createprovider.md) <br/> |<span data-ttu-id="5d311-124">メッセージ サービスにサービス プロバイダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="5d311-124">Adds a service provider to the message service.</span></span>  <br/> |
|[<span data-ttu-id="5d311-125">DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="5d311-125">DeleteProvider</span></span>](iprovideradmin-deleteprovider.md) <br/> |<span data-ttu-id="5d311-126">メッセージ サービスからサービス プロバイダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="5d311-126">Deletes a service provider from the message service.</span></span>  <br/> |
|[<span data-ttu-id="5d311-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="5d311-127">OpenProfileSection</span></span>](iprovideradmin-openprofilesection.md) <br/> |<span data-ttu-id="5d311-128">現在のプロファイルからプロファイルのセクションを開き、さらにアクセスするための[IProfSect](iprofsectimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="5d311-128">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d311-129">備考</span><span class="sxs-lookup"><span data-stu-id="5d311-129">Remarks</span></span>

<span data-ttu-id="5d311-130">クライアントは、 [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)メソッドを呼び出すことによって**IProviderAdmin**インターフェイスにポインターを取得することができます。メッセージ サービスのエントリ ポイント関数が呼び出されたときに、サービス プロバイダーは、 **IProviderAdmin**ポインターに渡されます。</span><span class="sxs-lookup"><span data-stu-id="5d311-130">Clients can get a pointer to an **IProviderAdmin** interface by calling the [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) method; service providers are passed an **IProviderAdmin** pointer when their message service's entry point function is called.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5d311-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d311-131">See also</span></span>



[<span data-ttu-id="5d311-132">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5d311-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

