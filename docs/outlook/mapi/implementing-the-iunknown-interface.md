---
title: IUnknown インターフェイスを実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 55bf8831af8f78767b2607c21ab54c32f6e4245f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800961"
---
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="f3867-103">IUnknown インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="f3867-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="f3867-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f3867-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f3867-105">すべての MAPI オブジェクトに実装されている、 [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)インターフェイスのメソッドをサポートして通信とオブジェクト管理を決める基準について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3867-105">The methods of the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="f3867-106">**IUnknown**には 3 つの方法: [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)、 [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)、および[リ ス](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="f3867-106">**IUnknown** has three methods: [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="f3867-107">**QueryInterface**には、別のオブジェクトが特定のインターフェイスをサポートしているかどうかを決定する 1 つのオブジェクトが有効にします。</span><span class="sxs-lookup"><span data-stu-id="f3867-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="f3867-108">**QueryInterface**を持つ他の機能の予備知識がない 2 つのオブジェクトを操作できます。</span><span class="sxs-lookup"><span data-stu-id="f3867-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="f3867-109">**QueryInterface**を実装するオブジェクトには、対象のインターフェイスをサポートして場合、は、インターフェイスの実装にポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="f3867-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="f3867-110">オブジェクトが要求されたインターフェイスをサポートしていない場合は、MAPI_E_INTERFACE_NOT_SUPPORTED 値を返します。</span><span class="sxs-lookup"><span data-stu-id="f3867-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="f3867-111">**QueryInterface**に要求されたインターフェイス ポインターが返されるとき、新しいオブジェクトの参照カウントも増加する必要です。</span><span class="sxs-lookup"><span data-stu-id="f3867-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="f3867-112">オブジェクトの参照カウントは、オブジェクトの有効期間を管理するために使用する数値値です。</span><span class="sxs-lookup"><span data-stu-id="f3867-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="f3867-113">参照カウントが 1 より大きい場合は、積極的に使用されているため、オブジェクトのメモリを解放できません。</span><span class="sxs-lookup"><span data-stu-id="f3867-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="f3867-114">だけすると、リファレンス カウントが 0 にオブジェクトを安全に解放できることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f3867-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="f3867-115">他の 2 つ**IUnknown**のメソッド、 **AddRef**と**リリース**では、参照カウントを管理します。</span><span class="sxs-lookup"><span data-stu-id="f3867-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="f3867-116">**AddRef**は、**リリース**をデクリメントしているときに、参照カウントをインクリメントしています。</span><span class="sxs-lookup"><span data-stu-id="f3867-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="f3867-117">すべてのメソッドや、 **QueryInterface**などのインターフェイス ポインターを返すための API 関数は、参照カウントをインクリメントするのに**AddRef**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3867-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="f3867-118">インターフェイス ポインターを受け取るメソッドのすべての実装では、ポインターが不要になったときにカウントをデクリメントする**リリース**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3867-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="f3867-119">**リリース**は、カウントが 0 である場合にのみに、インターフェイスに関連付けられているメモリを解放して、既存の参照カウントを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3867-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f3867-120">**AddRef**および**Release**は、正確な値を返す必要はありません、ためこれらのメソッドの呼び出し元で必要がありますオブジェクトがまだ有効であるかが破棄されたかどうかを判断するのに戻り値は使用しません。</span><span class="sxs-lookup"><span data-stu-id="f3867-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f3867-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="f3867-121">See also</span></span>



[<span data-ttu-id="f3867-122">MAPI オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="f3867-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

