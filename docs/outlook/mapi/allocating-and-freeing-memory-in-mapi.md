---
title: MAPI でのメモリの割り当てと解放
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e238f6bc-e9f6-4ea4-a2e4-ff5da2a04bd5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 68250c5cbeaa366ed4555bb469c4e68d62302f28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281586"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a><span data-ttu-id="9b7b0-103">MAPI でのメモリの割り当てと解放</span><span class="sxs-lookup"><span data-stu-id="9b7b0-103">Allocating and Freeing Memory in MAPI</span></span>

  
  
<span data-ttu-id="9b7b0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b7b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b7b0-105">メモリの割り当てと解放の方法を指定するだけでなく、パブリックインターフェイスメソッドと API 関数呼び出し間で渡されるメモリを解放する必要があるかどうかを知るためのモデルを定義します。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-105">In addition to specifying how to allocate and free memory, MAPI defines a model for knowing when memory passed between public interface method and API function calls should be freed.</span></span> <span data-ttu-id="9b7b0-106">モデルは、文字列や構造体へのポインターなど、インターフェイスを指すポインターではないパラメーターに割り当てられたメモリにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-106">The model applies only to memory allocated for parameters that are not pointers to interfaces, such as strings and pointers to structures.</span></span> <span data-ttu-id="9b7b0-107">インターフェイスポインターは、 **IUnknown**を介して実装された参照カウント機構を使用します。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-107">Interface pointers use the reference counting mechanism implemented through **IUnknown**.</span></span> <span data-ttu-id="9b7b0-108">非 MAPI 関連のメモリをクライアントアプリケーションまたはサービスプロバイダー内で内部的に割り当てたり解放したりするときは、意味のあるメカニズムを使用します。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-108">When allocating and freeing non-MAPI related memory internally within a client application or service provider, use whatever mechanism makes sense.</span></span> 
  
<span data-ttu-id="9b7b0-109">モデルでは、パラメーターを3種類のいずれかとして定義します。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-109">The model defines parameters as one of three types.</span></span> <span data-ttu-id="9b7b0-110">入力パラメーターとして使用できるのは、呼び出し元によって、呼び出された関数またはメソッドによって使用される情報、出力パラメーター、呼び出された関数またはメソッドによって設定され、呼び出し元に返される、または入力出力パラメーター (2 つの型の組み合わせ) です。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-110">They can be input parameters, set by the caller with information to be used by the called function or method, output parameters, set by the called function or method and returned to the caller, or input-output parameters, a combination of the two types.</span></span> <span data-ttu-id="9b7b0-111">出力パラメーターは、データへのポインターへのポインター、またはデータへのポインターへのポインターによく見られます。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-111">Output parameters are frequently pointers to data or pointers to pointers to data.</span></span> <span data-ttu-id="9b7b0-112">呼び出された関数は出力パラメーターのデータを割り当てる役割を担いますが、呼び出し元はポインターのメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-112">Although the called function is responsible for allocating the data for output parameters, the caller allocates the memory for the pointer.</span></span> 
  
<span data-ttu-id="9b7b0-113">次の表では、これらの種類のパラメーターに対してメモリを割り当てて解放するための規則について説明します。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-113">The rules for allocating and releasing memory for these types of parameters are explained in the following table.</span></span>
  
|<span data-ttu-id="9b7b0-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="9b7b0-114">**Type**</span></span>|<span data-ttu-id="9b7b0-115">**メモリ割り当て**</span><span class="sxs-lookup"><span data-stu-id="9b7b0-115">**Memory allocation**</span></span>|<span data-ttu-id="9b7b0-116">**メモリリリース**</span><span class="sxs-lookup"><span data-stu-id="9b7b0-116">**Memory release**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9b7b0-117">Input</span><span class="sxs-lookup"><span data-stu-id="9b7b0-117">Input</span></span>  <br/> |<span data-ttu-id="9b7b0-118">発信者が責任を担い、任意のメカニズムを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-118">Caller is responsible and can use any mechanism.</span></span>  <br/> |<span data-ttu-id="9b7b0-119">発信者が責任を担い、任意のメカニズムを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-119">Caller is responsible and can use any mechanism.</span></span>  <br/> |
|<span data-ttu-id="9b7b0-120">出力</span><span class="sxs-lookup"><span data-stu-id="9b7b0-120">Output</span></span>  <br/> |<span data-ttu-id="9b7b0-121">呼び出された関数は、 **MAPIAllocateBuffer**を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-121">Called function is responsible and must use **MAPIAllocateBuffer**.</span></span> <span data-ttu-id="9b7b0-122">詳細については、「 [MAPIAllocateBuffer](mapiallocatebuffer.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-122">For more information, see [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>  <br/> |<span data-ttu-id="9b7b0-123">発信者が責任を担い、 **MAPIFreeBuffer**を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-123">Caller is responsible and must use **MAPIFreeBuffer**.</span></span> <span data-ttu-id="9b7b0-124">詳細については、「 [MAPIFreeBuffer](mapifreebuffer.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-124">For more information, see [MAPIFreeBuffer](mapifreebuffer.md).</span></span>  <br/> |
|<span data-ttu-id="9b7b0-125">入力出力</span><span class="sxs-lookup"><span data-stu-id="9b7b0-125">Input-output</span></span>  <br/> |<span data-ttu-id="9b7b0-126">発信者は最初の割り当てを行い、呼び出された関数は必要に応じて**MAPIAllocateBuffer**を使用して再割り当てできます。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-126">Caller is responsible for the initial allocation and called function can reallocate if necessary using **MAPIAllocateBuffer**.</span></span>  <br/> |<span data-ttu-id="9b7b0-127">呼び出された関数は、再割り当てが必要な場合に最初の解放を行います。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-127">Called function is responsible for initial freeing if reallocation is necessary.</span></span> <span data-ttu-id="9b7b0-128">発信者は、最後の戻り値を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-128">Caller must free the final return value.</span></span>  <br/> |
   
<span data-ttu-id="9b7b0-129">エラーが発生した場合、通常、呼び出し元は、出力および入力出力パラメーターに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-129">During failure conditions, implementers of interface methods need to pay attention to output and input-output parameters because the caller generally has no way to clean them up.</span></span> <span data-ttu-id="9b7b0-130">エラーが返された場合、各出力または入力出力パラメーターは、呼び出し元によって初期化された値のままにするか、または呼び出し元の部分に対して何の処理もしなくてもクリーンアップできる値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-130">If an error is returned, then each output or input-output parameter must either be left at the value initialized by the caller or set to a value that can be cleaned up without any action on the part of the caller.</span></span> <span data-ttu-id="9b7b0-131">たとえば、の出力ポインターパラメーターは、入力`void ** ppv`時のままにするか、NULL ( `*ppv = NULL`) に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b7b0-131">For example, an output pointer-parameter of  `void ** ppv` must be left as it was on input or can be set to NULL (  `*ppv = NULL`).</span></span>
  

