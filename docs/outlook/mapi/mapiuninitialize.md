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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c1a78889ea98133af46089fdc93b0c1c4bb24226
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801546"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="39cdc-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="39cdc-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="39cdc-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="39cdc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="39cdc-105">、参照カウントのクリーンアップ処理をデクリメントし、削除インスタンスごとのグローバルなデータの MAPI DLL です。</span><span class="sxs-lookup"><span data-stu-id="39cdc-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39cdc-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="39cdc-106">Header file:</span></span>  <br/> |<span data-ttu-id="39cdc-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="39cdc-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="39cdc-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="39cdc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="39cdc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="39cdc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="39cdc-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="39cdc-110">Called by:</span></span>  <br/> |<span data-ttu-id="39cdc-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="39cdc-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="39cdc-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="39cdc-112">Parameters</span></span>

<span data-ttu-id="39cdc-113">なし</span><span class="sxs-lookup"><span data-stu-id="39cdc-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="39cdc-114">Return value</span><span class="sxs-lookup"><span data-stu-id="39cdc-114">Return value</span></span>

<span data-ttu-id="39cdc-115">なし。</span><span class="sxs-lookup"><span data-stu-id="39cdc-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="39cdc-116">備考</span><span class="sxs-lookup"><span data-stu-id="39cdc-116">Remarks</span></span>

<span data-ttu-id="39cdc-117">クライアント アプリケーションでは、[生じます](mapiinitialize.md)関数の呼び出しによって開始されている MAPI との対話を終了する**MAPIUninitialize**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="39cdc-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="39cdc-118">**MAPIUninitialize**が呼び出されると、その他の MAPI 呼び出し可能ないクライアントです。</span><span class="sxs-lookup"><span data-stu-id="39cdc-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="39cdc-119">**MAPIUninitialize**参照をデクリメント、および対応する**生じます**関数は、参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="39cdc-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="39cdc-120">したがって、1 つの関数への呼び出しの数は、他の呼び出しの数に等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="39cdc-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="39cdc-121">Win32 **DllMain**関数またはその他の機能を作成するか、スレッドを終了するのには**生じます**かから**MAPIUninitialize**を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="39cdc-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="39cdc-122">詳細については、[スレッド セーフであるオブジェクトを使用する](using-thread-safe-objects.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39cdc-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

