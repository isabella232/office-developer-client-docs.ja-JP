---
title: C++ での IUnknown の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68519f6c-fba8-47f5-9401-316e276f770e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cd5a14b07888c7a17d550941909b345eff3b0276
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585459"
---
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="e30ae-103">C++ での IUnknown の実装</span><span class="sxs-lookup"><span data-stu-id="e30ae-103">Implementing IUnknown in C++</span></span>

<span data-ttu-id="e30ae-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e30ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e30ae-105">C++ では[IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)、 [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)、および[リ ス](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)の[IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)インターフェイスのメソッドを実装することは非常に簡単です。</span><span class="sxs-lookup"><span data-stu-id="e30ae-105">Implementing the [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx), and [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) methods of the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) interface in C++ is fairly simple.</span></span> <span data-ttu-id="e30ae-106">渡されるパラメーターのいくつかの標準的な検証をした後は、 **QueryInterface**の実装は、サポートされているインターフェイスの一覧に対して要求されたインターフェイスの識別子をチェックします。</span><span class="sxs-lookup"><span data-stu-id="e30ae-106">After some standard validation of the parameters that are passed in, an implementation of **QueryInterface** checks the identifier of the requested interface against the list of supported interfaces.</span></span> <span data-ttu-id="e30ae-107">要求された識別子がサポートされている間にある場合は、 **AddRef**が呼び出され、 **this**ポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="e30ae-107">If the requested identifier is among those supported, **AddRef** is called and the **this** pointer is returned.</span></span> <span data-ttu-id="e30ae-108">要求された識別子がサポートされているリストにない場合は、出力のポインターは NULL に設定し、MAPI_E_INTERFACE_NOT_SUPPORTED の値が返されます。</span><span class="sxs-lookup"><span data-stu-id="e30ae-108">If the requested identifier is not on the supported list, the output pointer is set to NULL and the MAPI_E_INTERFACE_NOT_SUPPORTED value is returned.</span></span> 
  
<span data-ttu-id="e30ae-109">次のコード例は、状態オブジェクトのサブクラスであるオブジェクトの C++ の**QueryInterface**を実装する方法を示しています、 [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="e30ae-109">The following code example shows how you can implement **QueryInterface** in C++ for a status object, an object that is a subclass of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="e30ae-110">**IMAPIStatus**は、 **IUnknown**から継承[IMAPIProp: IUnknown](imapipropiunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="e30ae-110">**IMAPIStatus** inherits from **IUnknown** through [IMAPIProp : IUnknown](imapipropiunknown.md).</span></span> <span data-ttu-id="e30ae-111">したがって場合は、呼び出し元は、これらのインタ フェースのいずれかの確認メッセージが表示、 **this**ポインターが返されますインターフェイス継承によって関連しているため。</span><span class="sxs-lookup"><span data-stu-id="e30ae-111">Therefore, if a caller asks for any of these interfaces, the **this** pointer can be returned because the interfaces are related through inheritance.</span></span> 
  
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

<span data-ttu-id="e30ae-112">コード例を次に**AddRef**および**Release**メソッドを実装する方法を示しています、`CMyMAPIObject`オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="e30ae-112">The following code example shows how to implement the **AddRef** and **Release** methods for the  `CMyMAPIObject` object.</span></span> <span data-ttu-id="e30ae-113">**AddRef**および**Release**を実装することが簡単であるためにインラインを実装するために多くのサービス プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="e30ae-113">Because implementing **AddRef** and **Release** is straightforward, many service providers choose to implement them inline.</span></span> <span data-ttu-id="e30ae-114">**スレッド**と**避けるため**に、Win32 関数の呼び出しは、スレッドの安全を確保します。</span><span class="sxs-lookup"><span data-stu-id="e30ae-114">The calls to the Win32 functions **InterlockedIncrement** and **InterlockedDecrement** ensure thread safety.</span></span> <span data-ttu-id="e30ae-115">**Release**メソッドがオブジェクトを削除するときに呼び出されると、デストラクターでは、オブジェクト用のメモリが解放されます。</span><span class="sxs-lookup"><span data-stu-id="e30ae-115">The memory for the object is freed by the destructor, which is called when the **Release** method deletes the object.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="e30ae-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="e30ae-116">See also</span></span>

- [<span data-ttu-id="e30ae-117">MAPI オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="e30ae-117">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="e30ae-118">IUnknown インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="e30ae-118">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

