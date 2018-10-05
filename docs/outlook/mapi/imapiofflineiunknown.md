---
title: IMAPIOffline IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline
api_type:
- COM
ms.assetid: 211281ff-3c22-1b51-4b72-ca1e313c7202
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 20d8c39765b0dbbfdde530361894d0a27876010a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401280"
---
# <a name="imapioffline--iunknown"></a><span data-ttu-id="cd330-103">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cd330-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="cd330-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd330-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd330-105">オフライン オブジェクトの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="cd330-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cd330-106">提供元:</span><span class="sxs-lookup"><span data-stu-id="cd330-106">Provided by:</span></span>  <br/> |<span data-ttu-id="cd330-107">[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)に対してクエリを実行</span><span class="sxs-lookup"><span data-stu-id="cd330-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="cd330-108">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="cd330-108">Called by:</span></span>  <br/> |<span data-ttu-id="cd330-109">クライアント</span><span class="sxs-lookup"><span data-stu-id="cd330-109">Client</span></span>  <br/> |
|<span data-ttu-id="cd330-110">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="cd330-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cd330-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="cd330-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cd330-112">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="cd330-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd330-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="cd330-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="cd330-114">オフライン オブジェクトをオンラインまたはオフラインの現在の状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="cd330-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="cd330-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="cd330-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="cd330-116">コールバックは、オフラインのオブジェクトによってサポートされている条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="cd330-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="cd330-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="cd330-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="cd330-118">オフライン オブジェクトの現在のオンラインまたはオフラインの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="cd330-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="cd330-119">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="cd330-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="cd330-120">このメンバーは、プレース ホルダーではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="cd330-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd330-121">備考</span><span class="sxs-lookup"><span data-stu-id="cd330-121">Remarks</span></span>

<span data-ttu-id="cd330-122">クライアントでは、 **[HrOpenOfflineObj](hropenofflineobj.md)** を使用して、開き、 **IMAPIOfflineMgr**をサポートしているオフラインのオブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="cd330-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="cd330-123">( [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を使用) して、クライアントがこのインターフェイスを問い合わせることができます**IMAPIOfflineMgr**は、 [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)から継承しているため**IMAPIOffline**のオフラインのオブジェクトのインターフェイス ポインターへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="cd330-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="cd330-124">クライアントを取得または、オブジェクトの現在の状態を設定または ( **IMAPIOffline::GetCapabilities**の呼び出し) によって、オブジェクトのコールバック機能をお探しし、 **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)** を使用してコールバックを設定する」を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd330-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="cd330-125">このインターフェイスのメンバーは、Microsoft Outlook 2013 の内部使用に予約されているプレース ホルダーし、変更されることが。</span><span class="sxs-lookup"><span data-stu-id="cd330-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="cd330-126">このインターフェイスの他のメンバーは、記載されている場合のみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="cd330-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd330-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd330-127">See also</span></span>



[<span data-ttu-id="cd330-128">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="cd330-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="cd330-129">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="cd330-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="cd330-130">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="cd330-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="cd330-131">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="cd330-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

