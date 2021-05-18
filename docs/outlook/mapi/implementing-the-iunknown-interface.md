---
title: IUnknown インターフェイスの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5165476ea131e40153191e8625af5ea3c49f47b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310046"
---
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="5001c-103">IUnknown インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="5001c-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="5001c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5001c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5001c-105">すべての MAPI オブジェクトに [実装されている IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) インターフェイスのメソッドは、オブジェクト間通信とオブジェクト管理をサポートします。</span><span class="sxs-lookup"><span data-stu-id="5001c-105">The methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="5001c-106">**IUnknown には**[、IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) [、IUnknown::QueryInterface、](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)および [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)の 3 つのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="5001c-106">**IUnknown** has three methods: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="5001c-107">**QueryInterface を使用** すると、あるオブジェクトが別のオブジェクトが特定のインターフェイスをサポートするかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="5001c-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="5001c-108">**QueryInterface を使用** すると、相互の機能に関する事前の知識を持つ 2 つのオブジェクトを操作できます。</span><span class="sxs-lookup"><span data-stu-id="5001c-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="5001c-109">**QueryInterface** を実装するオブジェクトが、対象のインターフェイスをサポートしている場合は、インターフェイスの実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="5001c-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="5001c-110">オブジェクトが要求されたインターフェイスをサポートしていない場合は、オブジェクトの値MAPI_E_INTERFACE_NOT_SUPPORTEDします。</span><span class="sxs-lookup"><span data-stu-id="5001c-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="5001c-111">**QueryInterface が要求** されたインターフェイス ポインターを返す場合は、新しいオブジェクトの参照カウントも増やす必要があります。</span><span class="sxs-lookup"><span data-stu-id="5001c-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="5001c-112">オブジェクトの参照カウントは、オブジェクトのライフスパンを管理するために使用される数値です。</span><span class="sxs-lookup"><span data-stu-id="5001c-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="5001c-113">参照カウントが 1 より大きい場合、オブジェクトのメモリはアクティブに使用されているので解放できません。</span><span class="sxs-lookup"><span data-stu-id="5001c-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="5001c-114">参照カウントが 0 に低下した場合にのみ、オブジェクトを安全に解放できます。</span><span class="sxs-lookup"><span data-stu-id="5001c-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="5001c-115">他の **2 つの IUnknown** メソッドである **AddRef** メソッドと **Release メソッドは**、参照カウントを管理します。</span><span class="sxs-lookup"><span data-stu-id="5001c-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="5001c-116">**AddRef は** 参照カウントをインクリメントし **、Release** は参照カウントをデクリメントします。</span><span class="sxs-lookup"><span data-stu-id="5001c-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="5001c-117">**QueryInterface** などのインターフェイス ポインターを返すすべてのメソッドまたは API 関数は、参照カウントをインクリメントするために **AddRef** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5001c-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="5001c-118">インターフェイス ポインターを受信するメソッドのすべての実装は、ポインターが不要になったときにカウントをデクレメントするために **Release** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5001c-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="5001c-119">**リリース** は、既存の参照カウントをチェックし、カウントが 0 の場合にのみインターフェイスに関連付けられているメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="5001c-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5001c-120">**AddRef** と **Release** は正確な値を返す必要はないので、これらのメソッドの呼び出し元は戻り値を使用して、オブジェクトがまだ有効か破棄されたのかを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5001c-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5001c-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="5001c-121">See also</span></span>



[<span data-ttu-id="5001c-122">MAPI オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="5001c-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

