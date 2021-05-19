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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420095"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="7804c-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="7804c-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="7804c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7804c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7804c-105">メッセージを配信するためにトランスポート プロバイダーが呼び出される順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="7804c-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="7804c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7804c-106">Parameters</span></span>

 <span data-ttu-id="7804c-107">_cUID_</span><span class="sxs-lookup"><span data-stu-id="7804c-107">_cUID_</span></span>
  
> <span data-ttu-id="7804c-108">[in]lpUIDList パラメーター内の一  _意の識別子の_ 数。</span><span class="sxs-lookup"><span data-stu-id="7804c-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="7804c-109">_lpUIDList_</span><span class="sxs-lookup"><span data-stu-id="7804c-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="7804c-110">[in]トランスポート プロバイダーを表す一意の識別子の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7804c-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="7804c-111">配列には、現在のプロファイルで構成されているトランスポート プロバイダーごとに 1 つの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7804c-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="7804c-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7804c-112">_ulFlags_</span></span>
  
> <span data-ttu-id="7804c-113">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="7804c-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7804c-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="7804c-114">Return value</span></span>

<span data-ttu-id="7804c-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="7804c-115">S_OK</span></span> 
  
> <span data-ttu-id="7804c-116">トランスポートの順序が正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="7804c-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="7804c-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="7804c-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="7804c-118">_cUID パラメーターの値_ は、プロファイル内の実際のトランスポート プロバイダーの数と異なります。</span><span class="sxs-lookup"><span data-stu-id="7804c-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="7804c-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7804c-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7804c-120">_lpUIDList_ パラメーターで渡される 1 つ以上の [MAPIUID](mapiuid.md)構造体は、プロファイル内の現在のトランスポート プロバイダーを参照していない。</span><span class="sxs-lookup"><span data-stu-id="7804c-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7804c-121">注釈</span><span class="sxs-lookup"><span data-stu-id="7804c-121">Remarks</span></span>

<span data-ttu-id="7804c-122">**IMsgServiceAdmin::MsgServiceTransportOrder** メソッドは、プロファイル内のトランスポート プロバイダーの配信順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="7804c-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="7804c-123">_lpUIDList_ パラメーターには [、IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドから返されるテーブルの **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) プロパティから取得したトランスポート プロバイダーエントリ識別子の並べ替えリストが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7804c-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="7804c-124">クライアント アプリケーションは、lpUIDList の完全なリスト  _を渡す必要があります_。</span><span class="sxs-lookup"><span data-stu-id="7804c-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="7804c-125">**SetTransportOrder** は、STATUS_XP_PREFER_LAST **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティで設定された PR_RESOURCE_FLAGS フラグなどのトランスポート プロバイダーの基本設定を上書きします。</span><span class="sxs-lookup"><span data-stu-id="7804c-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7804c-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="7804c-126">See also</span></span>



[<span data-ttu-id="7804c-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="7804c-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="7804c-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7804c-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

