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
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="a8196-103">IUnknown インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="a8196-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="a8196-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8196-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8196-105">[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)インターフェイスのメソッドは、すべての MAPI オブジェクトに実装されており、オブジェクト間の通信とオブジェクトの管理をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a8196-105">The methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="a8196-106">**iunknown**には、次の3つのメソッドがあります。 [iunknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)、 [iunknown::: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)、および[iunknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a8196-106">**IUnknown** has three methods: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="a8196-107">**QueryInterface**では、1つのオブジェクトが特定のインターフェイスをサポートしているかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="a8196-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="a8196-108">**QueryInterface**では、互いの機能に関する知識を持たない2つのオブジェクトが対話できます。</span><span class="sxs-lookup"><span data-stu-id="a8196-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="a8196-109">**QueryInterface**を実装するオブジェクトが問題のインターフェイスをサポートしている場合は、インターフェイスの実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="a8196-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="a8196-110">要求されたインターフェイスがオブジェクトでサポートされていない場合は、MAPI_E_INTERFACE_NOT_SUPPORTED 値を返します。</span><span class="sxs-lookup"><span data-stu-id="a8196-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="a8196-111">**QueryInterface**は、要求されたインターフェイスポインターを返すときに、新しいオブジェクトの参照カウントも増加させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8196-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="a8196-112">オブジェクトの参照カウントは、オブジェクトの寿命を管理するために使用する数値です。</span><span class="sxs-lookup"><span data-stu-id="a8196-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="a8196-113">参照カウントが1より大きい場合は、オブジェクトのメモリが使用されているため、解放できません。</span><span class="sxs-lookup"><span data-stu-id="a8196-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="a8196-114">参照カウントが0になるのは、オブジェクトが安全に解放される場合のみです。</span><span class="sxs-lookup"><span data-stu-id="a8196-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="a8196-115">他の2つの**IUnknown**メソッドである**AddRef**と**Release**は、参照カウントを管理します。</span><span class="sxs-lookup"><span data-stu-id="a8196-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="a8196-116">**AddRef**は参照カウントをインクリメントしますが、**リリース**は減少します。</span><span class="sxs-lookup"><span data-stu-id="a8196-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="a8196-117">**QueryInterface**などのインターフェイスポインターを返すメソッドまたは API 関数はすべて、 **AddRef**を呼び出して参照カウントをインクリメントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8196-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="a8196-118">インターフェイスポインターを受け取るメソッドのすべての実装は、ポインターが不要になったときに、 **Release**を呼び出してカウントを減らす必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8196-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="a8196-119">**Release**は既存の参照カウントをチェックし、count が0の場合にのみ、インターフェイスに関連付けられているメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="a8196-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a8196-120">**AddRef**と**Release**は正確な値を返す必要がないため、これらのメソッドの呼び出し元は、オブジェクトがまだ有効であるか、破棄されているかを判断するために、戻り値を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="a8196-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8196-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8196-121">See also</span></span>



[<span data-ttu-id="a8196-122">MAPI オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="a8196-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

