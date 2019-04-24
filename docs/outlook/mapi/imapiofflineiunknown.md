---
title: imapioffline IUnknown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321267"
---
# <a name="imapioffline--iunknown"></a><span data-ttu-id="d4cea-103">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d4cea-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="d4cea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4cea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4cea-105">オフラインオブジェクトに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d4cea-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d4cea-106">提供元:</span><span class="sxs-lookup"><span data-stu-id="d4cea-106">Provided by:</span></span>  <br/> |<span data-ttu-id="d4cea-107">[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)のクエリ</span><span class="sxs-lookup"><span data-stu-id="d4cea-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="d4cea-108">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="d4cea-108">Called by:</span></span>  <br/> |<span data-ttu-id="d4cea-109">クライアント</span><span class="sxs-lookup"><span data-stu-id="d4cea-109">Client</span></span>  <br/> |
|<span data-ttu-id="d4cea-110">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="d4cea-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d4cea-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="d4cea-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d4cea-112">v の順序</span><span class="sxs-lookup"><span data-stu-id="d4cea-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4cea-113">**[setlevel](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="d4cea-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="d4cea-114">オフラインオブジェクトの現在の状態をオンラインまたはオフラインに設定します。</span><span class="sxs-lookup"><span data-stu-id="d4cea-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="d4cea-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="d4cea-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="d4cea-116">オフラインオブジェクトでサポートされているコールバックの条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="d4cea-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="d4cea-117">**[getselected](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="d4cea-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="d4cea-118">オフラインオブジェクトの現在のオンライン状態またはオフライン状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="d4cea-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="d4cea-119">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="d4cea-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="d4cea-120">このメンバーはプレースホルダーで、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d4cea-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4cea-121">解説</span><span class="sxs-lookup"><span data-stu-id="d4cea-121">Remarks</span></span>

<span data-ttu-id="d4cea-122">クライアントは**[hropenofflineobj](hropenofflineobj.md)** を使用して、 **IMAPIOfflineMgr**をサポートするオフラインオブジェクトを開いて取得します。</span><span class="sxs-lookup"><span data-stu-id="d4cea-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="d4cea-123">**IMAPIOfflineMgr**は[iunknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)から継承するため、クライアントはこのインターフェイスを ( [iunknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を使用して) 照会し、オフラインオブジェクトの**imapioffline**のインターフェイスポインターへのポインターを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="d4cea-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="d4cea-124">クライアントは、オブジェクトの現在の状態を取得または設定したり、オブジェクトのコールバック機能 ( **imapioffline:: getcapabilities**を呼び出すことによって) を調べたり、 **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)** を使用してコールバックを設定したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="d4cea-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="d4cea-125">このインターフェイスのメンバーは、Microsoft Outlook 2013 の内部使用のために予約されているプレースホルダーであり、変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d4cea-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="d4cea-126">このインターフェイスの他のメンバーは、ドキュメント化されている場合にのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4cea-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4cea-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="d4cea-127">See also</span></span>



[<span data-ttu-id="d4cea-128">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="d4cea-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="d4cea-129">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="d4cea-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="d4cea-130">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="d4cea-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="d4cea-131">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="d4cea-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

