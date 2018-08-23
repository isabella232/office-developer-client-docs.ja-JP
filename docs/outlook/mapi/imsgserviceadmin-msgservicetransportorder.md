---
title: IMsgServiceAdminMsgServiceTransportOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.MsgServiceTransportOrder
api_type:
- COM
ms.assetid: c57ada0e-b9a1-496b-8548-75686d8cba4e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5b96a45bab4cd00d23604d0b0b25f3e772277395
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800995"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="35206-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="35206-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="35206-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35206-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35206-105">どのトランスポートにメッセージを配信するプロバイダーの呼び出し順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="35206-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="35206-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35206-106">Parameters</span></span>

 <span data-ttu-id="35206-107">_cUID_</span><span class="sxs-lookup"><span data-stu-id="35206-107">_cUID_</span></span>
  
> <span data-ttu-id="35206-108">[in]_LpUIDList_パラメーターに一意の識別子の数。</span><span class="sxs-lookup"><span data-stu-id="35206-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="35206-109">_lpUIDList_</span><span class="sxs-lookup"><span data-stu-id="35206-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="35206-110">[in]トランスポート プロバイダーを表す一意の識別子の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="35206-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="35206-111">配列には、現在のプロファイルで構成されているトランスポート プロバイダーごとに 1 つの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="35206-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="35206-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="35206-112">_ulFlags_</span></span>
  
> <span data-ttu-id="35206-113">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="35206-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="35206-114">�߂�l</span><span class="sxs-lookup"><span data-stu-id="35206-114">Return value</span></span>

<span data-ttu-id="35206-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="35206-115">S_OK</span></span> 
  
> <span data-ttu-id="35206-116">輸送注文が正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="35206-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="35206-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="35206-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="35206-118">_CUID_パラメーターの値は、プロファイルの中に、トランスポート プロバイダーの数によって異なります。</span><span class="sxs-lookup"><span data-stu-id="35206-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="35206-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="35206-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="35206-120">_LpUIDList_パラメーターで渡された[MAPIUID](mapiuid.md)の構造体の 1 つ以上は、プロファイルの現在のトランスポート プロバイダーを参照しません。</span><span class="sxs-lookup"><span data-stu-id="35206-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="35206-121">注釈</span><span class="sxs-lookup"><span data-stu-id="35206-121">Remarks</span></span>

<span data-ttu-id="35206-122">**IMsgServiceAdmin::MsgServiceTransportOrder**メソッドは、プロファイルに、トランスポート プロバイダーの配信順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="35206-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="35206-123">_LpUIDList_パラメーターには、 [IMsgServiceAdmin から返されるテーブルの**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) のプロパティから取得したトランスポート プロバイダーのエントリの識別子の一覧が含まれている必要があります。GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="35206-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="35206-124">クライアント アプリケーションは、 _lpUIDList_の完全なリストを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="35206-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="35206-125">**SetTransportOrder**のオーバーライドは、STATUS_XP_PREFER_LAST フラグを**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) のプロパティの設定などのプロバイダーの設定を転送します。</span><span class="sxs-lookup"><span data-stu-id="35206-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="35206-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="35206-126">See also</span></span>



[<span data-ttu-id="35206-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="35206-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="35206-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35206-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

