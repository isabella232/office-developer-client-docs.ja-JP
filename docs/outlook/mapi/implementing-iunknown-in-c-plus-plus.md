---
title: C++ での IUnknown の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68519f6c-fba8-47f5-9401-316e276f770e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 08f3f3f937320d8a986b2002c761a37f0f749227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330178"
---
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="bd86d-103">C++ での IUnknown の実装</span><span class="sxs-lookup"><span data-stu-id="bd86d-103">Implementing IUnknown in C++</span></span>

<span data-ttu-id="bd86d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd86d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd86d-105">C++ の iunknown インターフェイスの iunknown: [: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)、 [iunknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)、および[iunknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドの実装は非常に簡単です。 [](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd86d-105">Implementing the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface in C++ is fairly simple.</span></span> <span data-ttu-id="bd86d-106">渡されたパラメーターの標準的な検証の後、 **QueryInterface**の実装は、サポートされているインターフェイスのリストに対して、要求されたインターフェイスの識別子をチェックします。</span><span class="sxs-lookup"><span data-stu-id="bd86d-106">After some standard validation of the parameters that are passed in, an implementation of **QueryInterface** checks the identifier of the requested interface against the list of supported interfaces.</span></span> <span data-ttu-id="bd86d-107">要求された識別子がサポートされている場合は、 **AddRef**が呼び出され、**この**ポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="bd86d-107">If the requested identifier is among those supported, **AddRef** is called and the **this** pointer is returned.</span></span> <span data-ttu-id="bd86d-108">要求された識別子がサポートされているリストに含まれていない場合、出力ポインターは NULL に設定され、MAPI_E_INTERFACE_NOT_SUPPORTED 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="bd86d-108">If the requested identifier is not on the supported list, the output pointer is set to NULL and the MAPI_E_INTERFACE_NOT_SUPPORTED value is returned.</span></span> 
  
<span data-ttu-id="bd86d-109">次のコード例は、ステータスオブジェクト ( [imapistatus: imapistatus](imapistatusimapiprop.md)インターフェイスのサブクラスであるオブジェクト) に対する**QueryInterface**を C++ で実装する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="bd86d-109">The following code example shows how you can implement **QueryInterface** in C++ for a status object, an object that is a subclass of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="bd86d-110">**imapistatus**は、 **iunknown**から[imapistatus: iunknown](imapipropiunknown.md)を継承します。</span><span class="sxs-lookup"><span data-stu-id="bd86d-110">**IMAPIStatus** inherits from **IUnknown** through [IMAPIProp : IUnknown](imapipropiunknown.md).</span></span> <span data-ttu-id="bd86d-111">そのため、発信者がこれらのインターフェイスのいずれかを要求した場合、インターフェイスは継承によって関連付けられるため、**この**ポインターを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="bd86d-111">Therefore, if a caller asks for any of these interfaces, the **this** pointer can be returned because the interfaces are related through inheritance.</span></span> 
  
```cpp
HRESULT CMyMAPIObject::QueryInterface (REFIID   riid,
                                       LPVOID * ppvObj)
{
    // Always set out parameter to NULL, validating it first.
    if (!ppvObj)
        return E_INVALIDARG;
    *ppvObj = NULL;
    if (riid == IID_IUnknown || riid == IID_IMAPIProp ||
        riid == IID_IMAPIStatus)
    {
        // Increment the reference count and return the pointer.
        *ppvObj = (LPVOID)this;
        AddRef();
        return NOERROR;
    }
    return E_NOINTERFACE;
}

```

<span data-ttu-id="bd86d-112">次のコード例は、 `CMyMAPIObject`オブジェクトの**AddRef**メソッドと**Release**メソッドを実装する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="bd86d-112">The following code example shows how to implement the **AddRef** and **Release** methods for the  `CMyMAPIObject` object.</span></span> <span data-ttu-id="bd86d-113">**AddRef**と**Release**の実装は簡単であるため、多くのサービスプロバイダーはそれらをインラインで実装することを選択します。</span><span class="sxs-lookup"><span data-stu-id="bd86d-113">Because implementing **AddRef** and **Release** is straightforward, many service providers choose to implement them inline.</span></span> <span data-ttu-id="bd86d-114">Win32 関数**InterlockedIncrement**および**InterlockedDecrement**の呼び出しにより、スレッドセーフが保証されます。</span><span class="sxs-lookup"><span data-stu-id="bd86d-114">The calls to the Win32 functions **InterlockedIncrement** and **InterlockedDecrement** ensure thread safety.</span></span> <span data-ttu-id="bd86d-115">オブジェクトのメモリはデストラクターによって解放されます。これは、 **Release**メソッドによってオブジェクトが削除されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="bd86d-115">The memory for the object is freed by the destructor, which is called when the **Release** method deletes the object.</span></span> 
  
```cpp
ULONG CMyMAPIObject::AddRef()
{
    InterlockedIncrement(m_cRef);
    return m_cRef;
}
ULONG CMyMAPIObject::Release()
{
    // Decrement the object's internal counter.
    ULONG ulRefCount = InterlockedDecrement(m_cRef);
    if (0 == m_cRef)
    {
        delete this;
    }
    return ulRefCount;
}
 
```

## <a name="see-also"></a><span data-ttu-id="bd86d-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd86d-116">See also</span></span>

- [<span data-ttu-id="bd86d-117">MAPI オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="bd86d-117">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="bd86d-118">IUnknown インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="bd86d-118">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

