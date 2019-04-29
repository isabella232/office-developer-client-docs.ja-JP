---
title: IMAPIViewAdviseSinkOnShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnShutdown
api_type:
- COM
ms.assetid: c9c3aecf-5e4b-407a-8ea1-6211b4c6e0a5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b43c1b96130052a05ac390f10f545a66fe72b7fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428523"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="4d566-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="4d566-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="4d566-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d566-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d566-105">フォームが閉じられていることをフォームビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="4d566-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="4d566-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4d566-106">Parameters</span></span>

<span data-ttu-id="4d566-107">なし</span><span class="sxs-lookup"><span data-stu-id="4d566-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="4d566-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="4d566-108">Return value</span></span>

<span data-ttu-id="4d566-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d566-109">S_OK</span></span> 
  
> <span data-ttu-id="4d566-110">通知に成功しました。</span><span class="sxs-lookup"><span data-stu-id="4d566-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4d566-111">注釈</span><span class="sxs-lookup"><span data-stu-id="4d566-111">Remarks</span></span>

<span data-ttu-id="4d566-112">フォーム通知の詳細については、「[フォーム通知の送信と受信](sending-and-receiving-form-notifications.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d566-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4d566-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="4d566-113">See also</span></span>



[<span data-ttu-id="4d566-114">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d566-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

