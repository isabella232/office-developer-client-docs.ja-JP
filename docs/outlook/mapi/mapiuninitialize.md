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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f95c86a137e7253f3445123c23f2dc0d76b6d87a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567392"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="a4e75-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="a4e75-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="a4e75-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4e75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4e75-105">、参照カウントのクリーンアップ処理をデクリメントし、削除インスタンスごとのグローバルなデータの MAPI DLL です。</span><span class="sxs-lookup"><span data-stu-id="a4e75-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4e75-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a4e75-106">Header file:</span></span>  <br/> |<span data-ttu-id="a4e75-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="a4e75-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="a4e75-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="a4e75-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a4e75-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a4e75-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a4e75-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a4e75-110">Called by:</span></span>  <br/> |<span data-ttu-id="a4e75-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="a4e75-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="a4e75-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a4e75-112">Parameters</span></span>

<span data-ttu-id="a4e75-113">なし</span><span class="sxs-lookup"><span data-stu-id="a4e75-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="a4e75-114">Return value</span><span class="sxs-lookup"><span data-stu-id="a4e75-114">Return value</span></span>

<span data-ttu-id="a4e75-115">なし。</span><span class="sxs-lookup"><span data-stu-id="a4e75-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4e75-116">注釈</span><span class="sxs-lookup"><span data-stu-id="a4e75-116">Remarks</span></span>

<span data-ttu-id="a4e75-117">クライアント アプリケーションでは、[生じます](mapiinitialize.md)関数の呼び出しによって開始されている MAPI との対話を終了する**MAPIUninitialize**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a4e75-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="a4e75-118">**MAPIUninitialize**が呼び出されると、その他の MAPI 呼び出し可能ないクライアントです。</span><span class="sxs-lookup"><span data-stu-id="a4e75-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="a4e75-119">**MAPIUninitialize**参照をデクリメント、および対応する**生じます**関数は、参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="a4e75-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="a4e75-120">したがって、1 つの関数への呼び出しの数は、他の呼び出しの数に等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a4e75-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a4e75-121">Win32 **DllMain**関数またはその他の機能を作成するか、スレッドを終了するのには**生じます**かから**MAPIUninitialize**を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="a4e75-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="a4e75-122">詳細については、[スレッド セーフであるオブジェクトを使用する](using-thread-safe-objects.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4e75-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

