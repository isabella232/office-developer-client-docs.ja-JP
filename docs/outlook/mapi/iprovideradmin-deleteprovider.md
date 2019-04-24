---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 28dbbb98c9810bb688b9ecdd730ef6c4ada5f60b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279550"
---
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="ebc03-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="ebc03-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="ebc03-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebc03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebc03-105">メッセージサービスからサービスプロバイダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="ebc03-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="ebc03-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ebc03-106">Parameters</span></span>

 <span data-ttu-id="ebc03-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="ebc03-107">_lpUID_</span></span>
  
> <span data-ttu-id="ebc03-108">[入力]削除するプロバイダーを表す一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ebc03-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ebc03-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="ebc03-109">Return value</span></span>

<span data-ttu-id="ebc03-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ebc03-110">S_OK</span></span> 
  
> <span data-ttu-id="ebc03-111">プロバイダーがメッセージサービスから正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="ebc03-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="ebc03-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ebc03-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ebc03-113">_lpuid_パラメーターが指す**MAPIUID**が認識されませんでした。</span><span class="sxs-lookup"><span data-stu-id="ebc03-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ebc03-114">解説</span><span class="sxs-lookup"><span data-stu-id="ebc03-114">Remarks</span></span>

<span data-ttu-id="ebc03-115">**IProviderAdmin::D eleteprovider**メソッドは、メッセージサービスからサービスプロバイダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="ebc03-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="ebc03-116">**deleteprovider**は、アクティブなサービスプロバイダによって登録された一連の識別子を使用して、 _lpuid_が指す**MAPIUID**構造を照合することによって、削除するサービスプロバイダーを決定します。</span><span class="sxs-lookup"><span data-stu-id="ebc03-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="ebc03-117">ほとんどのメッセージサービスでは、プロファイルが使用されている間、プロバイダーを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="ebc03-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="ebc03-118">削除するプロバイダーが使用されている場合、 **deleteprovider**はすぐに削除するのではなく、削除対象としてマークし、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="ebc03-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="ebc03-119">プロバイダーが使用されなくなると、そのプロバイダーは削除されます。</span><span class="sxs-lookup"><span data-stu-id="ebc03-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="ebc03-120">**deleteprovider**は、プロバイダーがサービスから削除される前に、メッセージサービスのエントリポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebc03-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="ebc03-121">_ulcontext_パラメーターは MSG_SERVICE_PROVIDER_DELETE に設定されています。</span><span class="sxs-lookup"><span data-stu-id="ebc03-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="ebc03-122">メッセージサービスエントリポイント関数は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="ebc03-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="ebc03-123">サービスプロバイダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="ebc03-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="ebc03-124">サービスプロバイダーのプロファイルセクションを削除します。</span><span class="sxs-lookup"><span data-stu-id="ebc03-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="ebc03-125">プロバイダーが削除された後、メッセージサービスエントリポイント関数が再度呼び出されることはありません。</span><span class="sxs-lookup"><span data-stu-id="ebc03-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ebc03-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="ebc03-126">See also</span></span>



[<span data-ttu-id="ebc03-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ebc03-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ebc03-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="ebc03-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="ebc03-129">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ebc03-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

