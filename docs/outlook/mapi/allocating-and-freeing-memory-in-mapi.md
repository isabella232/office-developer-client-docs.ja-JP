---
title: 割り当てと、MAPI でのメモリの解放
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e238f6bc-e9f6-4ea4-a2e4-ff5da2a04bd5
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: dc97abcb4b316b696032f2788f4e653717e1396b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799664"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a><span data-ttu-id="8a8ac-103">割り当てと、MAPI でのメモリの解放</span><span class="sxs-lookup"><span data-stu-id="8a8ac-103">Allocating and Freeing Memory in MAPI</span></span>

  
  
<span data-ttu-id="8a8ac-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8a8ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a8ac-105">ほかの割り当てし、メモリを解放する方法を指定するは、MAPI は、パブリック インターフェイスのメソッドと API 関数の呼び出しを解放する必要がありますとの間にメモリが渡された場合を把握するためのモデルを定義します。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-105">In addition to specifying how to allocate and free memory, MAPI defines a model for knowing when memory passed between public interface method and API function calls should be freed.</span></span> <span data-ttu-id="8a8ac-106">モデルは、文字列、構造体へのポインターなどのインターフェイスへのポインターではないパラメーターに割り当てられたメモリにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-106">The model applies only to memory allocated for parameters that are not pointers to interfaces, such as strings and pointers to structures.</span></span> <span data-ttu-id="8a8ac-107">インターフェイス ポインターは、参照カウント メカニズムを**IUnknown**を使用して実装を使用します。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-107">Interface pointers use the reference counting mechanism implemented through **IUnknown**.</span></span> <span data-ttu-id="8a8ac-108">割り当てと解放の非 MAPI クライアント アプリケーションまたはサービス プロバイダーの内部でメモリに関連する、意味をどのようなメカニズムを使用します。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-108">When allocating and freeing non-MAPI related memory internally within a client application or service provider, use whatever mechanism makes sense.</span></span> 
  
<span data-ttu-id="8a8ac-109">モデルでは、次の 3 種類の 1 つとしてパラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-109">The model defines parameters as one of three types.</span></span> <span data-ttu-id="8a8ac-110">それらを入力パラメーターは、呼び出された関数またはメソッドが使用する情報を使用して呼び出し元による設定は、出力パラメーターと、呼び出された関数またはメソッドによって設定には、呼び出し元、または入出力パラメーター、2 つの種類の組み合わせが返されます。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-110">They can be input parameters, set by the caller with information to be used by the called function or method, output parameters, set by the called function or method and returned to the caller, or input-output parameters, a combination of the two types.</span></span> <span data-ttu-id="8a8ac-111">出力パラメーターは、頻繁にデータへのポインターまたはデータへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-111">Output parameters are frequently pointers to data or pointers to pointers to data.</span></span> <span data-ttu-id="8a8ac-112">呼び出された関数は、出力パラメーターのデータの割り当てを担当するが、呼び出し元は、ポインターのメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-112">Although the called function is responsible for allocating the data for output parameters, the caller allocates the memory for the pointer.</span></span> 
  
<span data-ttu-id="8a8ac-113">割り当てと、これらのパラメーターの種類のメモリを解放するための規則は、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-113">The rules for allocating and releasing memory for these types of parameters are explained in the following table.</span></span>
  
|<span data-ttu-id="8a8ac-114">**型**</span><span class="sxs-lookup"><span data-stu-id="8a8ac-114">**Type**</span></span>|<span data-ttu-id="8a8ac-115">**メモリの割り当て**</span><span class="sxs-lookup"><span data-stu-id="8a8ac-115">**Memory allocation**</span></span>|<span data-ttu-id="8a8ac-116">**メモリのリリース**</span><span class="sxs-lookup"><span data-stu-id="8a8ac-116">**Memory release**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8a8ac-117">入力</span><span class="sxs-lookup"><span data-stu-id="8a8ac-117">Input</span></span>  <br/> |<span data-ttu-id="8a8ac-118">呼び出し元は、責任し、任意の機構を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-118">Caller is responsible and can use any mechanism.</span></span>  <br/> |<span data-ttu-id="8a8ac-119">呼び出し元は、責任し、任意の機構を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-119">Caller is responsible and can use any mechanism.</span></span>  <br/> |
|<span data-ttu-id="8a8ac-120">出力</span><span class="sxs-lookup"><span data-stu-id="8a8ac-120">Output</span></span>  <br/> |<span data-ttu-id="8a8ac-121">呼び出された関数は、担当する**MAPIAllocateBuffer**を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-121">Called function is responsible and must use **MAPIAllocateBuffer**.</span></span> <span data-ttu-id="8a8ac-122">詳細については、 [MAPIAllocateBuffer](mapiallocatebuffer.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-122">For more information, see [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>  <br/> |<span data-ttu-id="8a8ac-123">呼び出し元し、 **MAPIFreeBuffer**を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-123">Caller is responsible and must use **MAPIFreeBuffer**.</span></span> <span data-ttu-id="8a8ac-124">詳細については、 [MAPIFreeBuffer](mapifreebuffer.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-124">For more information, see [MAPIFreeBuffer](mapifreebuffer.md).</span></span>  <br/> |
|<span data-ttu-id="8a8ac-125">入力出力</span><span class="sxs-lookup"><span data-stu-id="8a8ac-125">Input-output</span></span>  <br/> |<span data-ttu-id="8a8ac-126">呼び出し元が呼び出された関数の初期の割り当てと割り当てを変更できます必要な場合の**MAPIAllocateBuffer**を使用します。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-126">Caller is responsible for the initial allocation and called function can reallocate if necessary using **MAPIAllocateBuffer**.</span></span>  <br/> |<span data-ttu-id="8a8ac-127">呼び出された関数は、再割り当てが必要な場合に、初期の解放をします。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-127">Called function is responsible for initial freeing if reallocation is necessary.</span></span> <span data-ttu-id="8a8ac-128">呼び出し元は、最終的な戻り値を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-128">Caller must free the final return value.</span></span>  <br/> |
   
<span data-ttu-id="8a8ac-129">障害条件は、時にインターフェイス メソッドの実装を呼び出し元はそれらをクリーンアップする方法があるない一般にために、出力パラメーターと入出力パラメーターに注意を払う必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-129">During failure conditions, implementers of interface methods need to pay attention to output and input-output parameters because the caller generally has no way to clean them up.</span></span> <span data-ttu-id="8a8ac-130">エラーが返された場合、各出力または入出力パラメーターする必要がありますかのままにして値は呼び出し元が初期化または呼び出し側の操作をしなくてもクリーンアップすることができる値に設定します。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-130">If an error is returned, then each output or input-output parameter must either be left at the value initialized by the caller or set to a value that can be cleaned up without any action on the part of the caller.</span></span> <span data-ttu-id="8a8ac-131">たとえば、出力ポインターのパラメーターの`void ** ppv`は NULL に設定することができます、または入力されて、ままにする必要があります ( `*ppv = NULL`)。</span><span class="sxs-lookup"><span data-stu-id="8a8ac-131">For example, an output pointer-parameter of  `void ** ppv` must be left as it was on input or can be set to NULL (  `*ppv = NULL`).</span></span>
  

