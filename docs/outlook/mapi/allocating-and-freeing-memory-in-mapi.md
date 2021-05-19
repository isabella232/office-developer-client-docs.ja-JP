---
title: MAPI でのメモリの割り当てと解放
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e238f6bc-e9f6-4ea4-a2e4-ff5da2a04bd5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 68250c5cbeaa366ed4555bb469c4e68d62302f28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419668"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a><span data-ttu-id="fa36c-103">MAPI でのメモリの割り当てと解放</span><span class="sxs-lookup"><span data-stu-id="fa36c-103">Allocating and Freeing Memory in MAPI</span></span>

  
  
<span data-ttu-id="fa36c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa36c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa36c-105">MAPI は、メモリの割り当ておよび解放方法を指定する以外に、パブリック インターフェイス メソッドと API 関数呼び出しの間で渡されるメモリを解放する必要がある場合を知るモデルを定義します。</span><span class="sxs-lookup"><span data-stu-id="fa36c-105">In addition to specifying how to allocate and free memory, MAPI defines a model for knowing when memory passed between public interface method and API function calls should be freed.</span></span> <span data-ttu-id="fa36c-106">このモデルは、文字列や構造体へのポインターなど、インターフェイスへのポインターではないパラメーターに割り当てられたメモリにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="fa36c-106">The model applies only to memory allocated for parameters that are not pointers to interfaces, such as strings and pointers to structures.</span></span> <span data-ttu-id="fa36c-107">インターフェイス ポインターは **、IUnknown** を介して実装された参照カウント メカニズムを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa36c-107">Interface pointers use the reference counting mechanism implemented through **IUnknown**.</span></span> <span data-ttu-id="fa36c-108">クライアント アプリケーションまたはサービス プロバイダー内で MAPI 以外の関連メモリを内部的に割り当て、解放する場合は、意味のあるメカニズムを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa36c-108">When allocating and freeing non-MAPI related memory internally within a client application or service provider, use whatever mechanism makes sense.</span></span> 
  
<span data-ttu-id="fa36c-109">モデルは、パラメーターを 3 つの種類の 1 つとして定義します。</span><span class="sxs-lookup"><span data-stu-id="fa36c-109">The model defines parameters as one of three types.</span></span> <span data-ttu-id="fa36c-110">これらは、呼び出された関数またはメソッドによって使用される情報を呼び出し元が設定する入力パラメーター、呼び出し元の関数またはメソッドによって設定された出力パラメーター、呼び出し元に返される入力パラメーター、または 2 つの型の組み合わせの入出力パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="fa36c-110">They can be input parameters, set by the caller with information to be used by the called function or method, output parameters, set by the called function or method and returned to the caller, or input-output parameters, a combination of the two types.</span></span> <span data-ttu-id="fa36c-111">出力パラメーターは、多くの場合、データへのポインターまたはデータへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="fa36c-111">Output parameters are frequently pointers to data or pointers to pointers to data.</span></span> <span data-ttu-id="fa36c-112">呼び出された関数は、出力パラメーターのデータを割り当てるのを担当しますが、呼び出し元はポインターのメモリを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="fa36c-112">Although the called function is responsible for allocating the data for output parameters, the caller allocates the memory for the pointer.</span></span> 
  
<span data-ttu-id="fa36c-113">これらの種類のパラメーターのメモリを割り当て、解放するルールについて、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="fa36c-113">The rules for allocating and releasing memory for these types of parameters are explained in the following table.</span></span>
  
|<span data-ttu-id="fa36c-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="fa36c-114">**Type**</span></span>|<span data-ttu-id="fa36c-115">**メモリ割り当て**</span><span class="sxs-lookup"><span data-stu-id="fa36c-115">**Memory allocation**</span></span>|<span data-ttu-id="fa36c-116">**メモリの解放**</span><span class="sxs-lookup"><span data-stu-id="fa36c-116">**Memory release**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fa36c-117">Input</span><span class="sxs-lookup"><span data-stu-id="fa36c-117">Input</span></span>  <br/> |<span data-ttu-id="fa36c-118">呼び出し元は責任を負い、任意のメカニズムを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa36c-118">Caller is responsible and can use any mechanism.</span></span>  <br/> |<span data-ttu-id="fa36c-119">呼び出し元は責任を負い、任意のメカニズムを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa36c-119">Caller is responsible and can use any mechanism.</span></span>  <br/> |
|<span data-ttu-id="fa36c-120">出力</span><span class="sxs-lookup"><span data-stu-id="fa36c-120">Output</span></span>  <br/> |<span data-ttu-id="fa36c-121">呼び出された関数は責任を負い **、MAPIAllocateBuffer を使用する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="fa36c-121">Called function is responsible and must use **MAPIAllocateBuffer**.</span></span> <span data-ttu-id="fa36c-122">詳細については [、「MAPIAllocateBuffer」を参照してください](mapiallocatebuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="fa36c-122">For more information, see [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>  <br/> |<span data-ttu-id="fa36c-123">呼び出し元は責任を負い **、MAPIFreeBuffer を使用する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="fa36c-123">Caller is responsible and must use **MAPIFreeBuffer**.</span></span> <span data-ttu-id="fa36c-124">詳細については [、「MAPIFreeBuffer」を参照してください](mapifreebuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="fa36c-124">For more information, see [MAPIFreeBuffer](mapifreebuffer.md).</span></span>  <br/> |
|<span data-ttu-id="fa36c-125">入出力</span><span class="sxs-lookup"><span data-stu-id="fa36c-125">Input-output</span></span>  <br/> |<span data-ttu-id="fa36c-126">呼び出し元は、最初の割り当てを担当し、呼び出された関数は **、MAPIAllocateBuffer** を使用して必要に応じて再割り当てできます。</span><span class="sxs-lookup"><span data-stu-id="fa36c-126">Caller is responsible for the initial allocation and called function can reallocate if necessary using **MAPIAllocateBuffer**.</span></span>  <br/> |<span data-ttu-id="fa36c-127">呼び出された関数は、必要に応じて初期解放を行います。</span><span class="sxs-lookup"><span data-stu-id="fa36c-127">Called function is responsible for initial freeing if reallocation is necessary.</span></span> <span data-ttu-id="fa36c-128">呼び出し元は、最終的な戻り値を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa36c-128">Caller must free the final return value.</span></span>  <br/> |
   
<span data-ttu-id="fa36c-129">エラー状態の間、インターフェイス メソッドの実装者は、一般的に呼び出し元がそれらをクリーンアップする方法がないので、出力パラメーターと入出力パラメーターに注意を払う必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa36c-129">During failure conditions, implementers of interface methods need to pay attention to output and input-output parameters because the caller generally has no way to clean them up.</span></span> <span data-ttu-id="fa36c-130">エラーが返された場合、各出力または入出力パラメーターは、呼び出し元によって初期化された値に残す必要があります。または呼び出し元の部分に対するアクションを実行せずにクリーンアップできる値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa36c-130">If an error is returned, then each output or input-output parameter must either be left at the value initialized by the caller or set to a value that can be cleaned up without any action on the part of the caller.</span></span> <span data-ttu-id="fa36c-131">たとえば、出力ポインター パラメーターは、入力時に残す必要があります。または  `void ** ppv` NULL ( ) に設定できます  `*ppv = NULL` 。</span><span class="sxs-lookup"><span data-stu-id="fa36c-131">For example, an output pointer-parameter of  `void ** ppv` must be left as it was on input or can be set to NULL (  `*ppv = NULL`).</span></span>
  

