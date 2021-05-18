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
# <a name="mapiuninitialize"></a><span data-ttu-id="ffa25-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="ffa25-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="ffa25-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffa25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffa25-105">MAPI DLL の参照カウントをデクレメントし、クリーンアップし、インスタンスごとのグローバル データを削除します。</span><span class="sxs-lookup"><span data-stu-id="ffa25-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ffa25-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ffa25-106">Header file:</span></span>  <br/> |<span data-ttu-id="ffa25-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="ffa25-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="ffa25-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="ffa25-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ffa25-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ffa25-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ffa25-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ffa25-110">Called by:</span></span>  <br/> |<span data-ttu-id="ffa25-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="ffa25-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="ffa25-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ffa25-112">Parameters</span></span>

<span data-ttu-id="ffa25-113">なし</span><span class="sxs-lookup"><span data-stu-id="ffa25-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="ffa25-114">Return value</span><span class="sxs-lookup"><span data-stu-id="ffa25-114">Return value</span></span>

<span data-ttu-id="ffa25-115">なし。</span><span class="sxs-lookup"><span data-stu-id="ffa25-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ffa25-116">注釈</span><span class="sxs-lookup"><span data-stu-id="ffa25-116">Remarks</span></span>

<span data-ttu-id="ffa25-117">クライアント アプリケーションは **、MAPIUninitialize** 関数を呼び出して MAPI との対話を終了します [。MAPIInitialize](mapiinitialize.md) 関数の呼び出しで開始します。</span><span class="sxs-lookup"><span data-stu-id="ffa25-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="ffa25-118">**MAPIUninitialize が呼** び出された後、クライアントによって他の MAPI 呼び出しを行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ffa25-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="ffa25-119">**MAPIUninitialize** デクリメントは参照カウントを、対応する **MAPIInitialize** 関数は参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="ffa25-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="ffa25-120">したがって、1 つの関数に対する呼び出しの数は、もう一方の関数への呼び出しの数と等しくする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffa25-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ffa25-121">Win32 **DllMain** 関数またはスレッドを作成または終了するその他の関数内から **MAPIInitialize** または **MAPIUninitialize** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffa25-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="ffa25-122">詳細については、「Using [Thread-Safe オブジェクト」を参照してください](using-thread-safe-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="ffa25-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

