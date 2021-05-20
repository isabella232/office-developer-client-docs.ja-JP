---
title: imapiinitmonitor-isinitialized
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.IsInitialized
api_type:
- COM
ms.assetid: 1af0bf93-6bcb-4235-ac30-0d00245ec636
description: IMAPIInitMonitor::IsInitialized
Last modified: April 26, 2021
ms.openlocfilehash: 6870c8fa0de51b626662c58b2c8c300c3a4d806e
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062026"
---
# <a name="imapiinitmonitorisinitialized"></a><span data-ttu-id="d51ca-103">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="d51ca-103">IMAPIInitMonitor::IsInitialized</span></span>
  
<span data-ttu-id="d51ca-104">**適用対象 :** Outlook 2013 |Outlook 2016 |2019</span><span class="sxs-lookup"><span data-stu-id="d51ca-104">**Applies to**: Outlook 2013 | Outlook 2016 | 2019</span></span>
  
<span data-ttu-id="d51ca-105">MAPI を照会して、呼び出し元プロセスで現在初期化されているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="d51ca-105">Queries MAPI to determine if it currently initialized in the calling process.</span></span>

```cpp
BOOL IMAPIInitMonitor::IsInitialized()  
```

## <a name="parameters"></a><span data-ttu-id="d51ca-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d51ca-106">Parameters</span></span>
<span data-ttu-id="d51ca-107">なし</span><span class="sxs-lookup"><span data-stu-id="d51ca-107">None</span></span>

## <a name="return-value"></a><span data-ttu-id="d51ca-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="d51ca-108">Return value</span></span>
<span data-ttu-id="d51ca-109">MAPI 初期化の現在の状態を示す BOOL は、値 TRUE は MAPI が初期化され、使用できる状態であることを意味し、FALSE の値は MAPI が現在初期化されていない状態で使用できる状態であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="d51ca-109">A BOOL indicating the current state of MAPI initialization, a value of TRUE means MAPI has been initialized and is available for use, while a value of FALSE means MAPI is currenty uninitialized and is not ready be consumed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d51ca-110">注釈</span><span class="sxs-lookup"><span data-stu-id="d51ca-110">Remarks</span></span>
<span data-ttu-id="d51ca-111">これは、MAPI を使用する準備ができているかどうかを判断するために使用できます。たとえば、MAPI が既に初期化されている場合にのみアプリケーションが何かを実行する場合は、オプションの作業のために MAPI をスピンアップするコストを防ぐため、バックグラウンド タスクのチェックに役立つ可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d51ca-111">This can be used to determine if MAPI is ready to be used, for example, if your application wanted to do something only if MAPI has already be initialized, this could be a useful check in a background task to prevent the cost of spinning up MAPI for optional work.</span></span>

## <a name="see-also"></a><span data-ttu-id="d51ca-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="d51ca-112">See also</span></span>

[<span data-ttu-id="d51ca-113">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="d51ca-113">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md)

[<span data-ttu-id="d51ca-114">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="d51ca-114">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)
