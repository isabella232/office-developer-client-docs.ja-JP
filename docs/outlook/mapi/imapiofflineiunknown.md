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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 20d8c39765b0dbbfdde530361894d0a27876010a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321267"
---
# <a name="imapioffline--iunknown"></a><span data-ttu-id="40a23-103">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="40a23-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="40a23-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40a23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40a23-105">オフライン オブジェクトの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="40a23-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40a23-106">提供元:</span><span class="sxs-lookup"><span data-stu-id="40a23-106">Provided by:</span></span>  <br/> |<span data-ttu-id="40a23-107">[IMAPIOfflineMgr のクエリ](imapiofflinemgrimapioffline.md)</span><span class="sxs-lookup"><span data-stu-id="40a23-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="40a23-108">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="40a23-108">Called by:</span></span>  <br/> |<span data-ttu-id="40a23-109">クライアント</span><span class="sxs-lookup"><span data-stu-id="40a23-109">Client</span></span>  <br/> |
|<span data-ttu-id="40a23-110">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="40a23-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="40a23-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="40a23-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="40a23-112">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="40a23-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40a23-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="40a23-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="40a23-114">オフライン オブジェクトの現在の状態をオンラインまたはオフラインに設定します。</span><span class="sxs-lookup"><span data-stu-id="40a23-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="40a23-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="40a23-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="40a23-116">オフライン オブジェクトでコールバックがサポートされる条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="40a23-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="40a23-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="40a23-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="40a23-118">オフライン オブジェクトの現在のオンライン状態またはオフライン状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="40a23-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="40a23-119">*プレースホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="40a23-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="40a23-120">このメンバーはプレースホルダーであり、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="40a23-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40a23-121">注釈</span><span class="sxs-lookup"><span data-stu-id="40a23-121">Remarks</span></span>

<span data-ttu-id="40a23-122">クライアントは **[、HrOpenOfflineObj](hropenofflineobj.md)** を使用して **、IMAPIOfflineMgr** をサポートするオフライン オブジェクトを開いて取得します。</span><span class="sxs-lookup"><span data-stu-id="40a23-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="40a23-123">**IMAPIOfflineMgr** は [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)から継承しますので、クライアントは [(IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を使用して) このインターフェイスをクエリして、オフライン オブジェクトの **IMAPIOffline** のインターフェイス ポインターへのポインターを取得できます。</span><span class="sxs-lookup"><span data-stu-id="40a23-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="40a23-124">その後、クライアントはオブジェクトの現在の状態を取得または設定するか、オブジェクトのコールバック機能 **(IMAPIOffline::GetCapabilities** を呼び出して) を確認し **[、IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)** を使用してコールバックを設定できます。</span><span class="sxs-lookup"><span data-stu-id="40a23-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="40a23-125">このインターフェイスのメンバーは、内部で使用するために予約されたプレースホルダーであり、Microsoft Outlook 2013変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="40a23-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="40a23-126">このインターフェイスの他のメンバーは、ドキュメントとしてのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40a23-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40a23-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="40a23-127">See also</span></span>



[<span data-ttu-id="40a23-128">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="40a23-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="40a23-129">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="40a23-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="40a23-130">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="40a23-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="40a23-131">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="40a23-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

