---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f7339588bcc6815545e7341eafffe9cf001c1d76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408524"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="6cdc8-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="6cdc8-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="6cdc8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cdc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cdc8-105">MAPI DLL のインスタンスごとのグローバルデータを、参照カウント、クリーンアップ、削除します。</span><span class="sxs-lookup"><span data-stu-id="6cdc8-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6cdc8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6cdc8-106">Header file:</span></span>  <br/> |<span data-ttu-id="6cdc8-107">mapix</span><span class="sxs-lookup"><span data-stu-id="6cdc8-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="6cdc8-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="6cdc8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6cdc8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6cdc8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6cdc8-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="6cdc8-110">Called by:</span></span>  <br/> |<span data-ttu-id="6cdc8-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6cdc8-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="6cdc8-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6cdc8-112">Parameters</span></span>

<span data-ttu-id="6cdc8-113">なし</span><span class="sxs-lookup"><span data-stu-id="6cdc8-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="6cdc8-114">Return value</span><span class="sxs-lookup"><span data-stu-id="6cdc8-114">Return value</span></span>

<span data-ttu-id="6cdc8-115">なし。</span><span class="sxs-lookup"><span data-stu-id="6cdc8-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6cdc8-116">注釈</span><span class="sxs-lookup"><span data-stu-id="6cdc8-116">Remarks</span></span>

<span data-ttu-id="6cdc8-117">クライアントアプリケーションは、 **MAPIUninitialize**関数を呼び出して MAPI との対話を終了させるため、 [MAPIInitialize](mapiinitialize.md)関数の呼び出しから開始されます。</span><span class="sxs-lookup"><span data-stu-id="6cdc8-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="6cdc8-118">**MAPIUninitialize**を呼び出した後、クライアントは他の MAPI 呼び出しを行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="6cdc8-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="6cdc8-119">**MAPIUninitialize**は参照カウントをデクリメントし、対応する**MAPIInitialize**関数が参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="6cdc8-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="6cdc8-120">そのため、1つの関数への呼び出しの数は、もう一方への呼び出しの数と等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6cdc8-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6cdc8-121">**MAPIInitialize**または**MAPIUninitialize**は、Win32 **DllMain**関数から、またはスレッドを作成または終了する他の関数内から呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="6cdc8-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="6cdc8-122">詳細については、「[スレッドセーフオブジェクトの使用](using-thread-safe-objects.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cdc8-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

