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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3d532e0eb46daa412711344421936a58da309b7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310004"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="cbd61-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="cbd61-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="cbd61-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbd61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbd61-105">メッセージを配信するためにトランスポートプロバイダーが呼び出される順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd61-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="cbd61-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cbd61-106">Parameters</span></span>

 <span data-ttu-id="cbd61-107">_cuid_</span><span class="sxs-lookup"><span data-stu-id="cbd61-107">_cUID_</span></span>
  
> <span data-ttu-id="cbd61-108">順番_lpuidlist_パラメーターの一意の識別子の数。</span><span class="sxs-lookup"><span data-stu-id="cbd61-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="cbd61-109">_lpuidlist_</span><span class="sxs-lookup"><span data-stu-id="cbd61-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="cbd61-110">順番トランスポートプロバイダーを表す一意の識別子の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cbd61-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="cbd61-111">配列には、現在のプロファイルで構成されている各トランスポートプロバイダーの識別子が1つ含まれています。</span><span class="sxs-lookup"><span data-stu-id="cbd61-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="cbd61-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cbd61-112">_ulFlags_</span></span>
  
> <span data-ttu-id="cbd61-113">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="cbd61-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cbd61-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="cbd61-114">Return value</span></span>

<span data-ttu-id="cbd61-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="cbd61-115">S_OK</span></span> 
  
> <span data-ttu-id="cbd61-116">トランスポートオーダーが正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="cbd61-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="cbd61-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="cbd61-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="cbd61-118">_cuid_パラメーターの値は、プロファイルに実際に含まれるトランスポートプロバイダーの数とは異なります。</span><span class="sxs-lookup"><span data-stu-id="cbd61-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="cbd61-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="cbd61-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="cbd61-120">_lpuidlist_パラメーターに渡された1つ以上の[MAPIUID](mapiuid.md)構造体が、プロファイルに現在含まれているトランスポートプロバイダーを参照していません。</span><span class="sxs-lookup"><span data-stu-id="cbd61-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cbd61-121">解説</span><span class="sxs-lookup"><span data-stu-id="cbd61-121">Remarks</span></span>

<span data-ttu-id="cbd61-122">**IMsgServiceAdmin:: msgservicetransportorder**メソッドは、プロファイル内のトランスポートプロバイダーの配信順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd61-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="cbd61-123">_lpuidlist_パラメーターには、IMsgServiceAdmin から返されるテーブルの**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) プロパティから取得した、トランスポートプロバイダーのエントリ識別子の並べ替えられたリストを含める必要があります[。getprovidertable](imsgserviceadmin-getprovidertable.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="cbd61-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="cbd61-124">クライアントアプリケーションは、完全なリストを_lpuidlist_に渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cbd61-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="cbd61-125">**settransportorder**は、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティで設定された STATUS_XP_PREFER_LAST フラグなど、トランスポートプロバイダーの設定より優先されます。</span><span class="sxs-lookup"><span data-stu-id="cbd61-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cbd61-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="cbd61-126">See also</span></span>



[<span data-ttu-id="cbd61-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="cbd61-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="cbd61-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbd61-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

