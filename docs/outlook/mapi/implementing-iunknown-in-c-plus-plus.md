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
# <a name="implementing-iunknown-in-c"></a>C++ での IUnknown の実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
C++ の iunknown インターフェイスの iunknown: [: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)、 [iunknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)、および[iunknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドの実装は非常に簡単です。 [](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) 渡されたパラメーターの標準的な検証の後、 **QueryInterface**の実装は、サポートされているインターフェイスのリストに対して、要求されたインターフェイスの識別子をチェックします。 要求された識別子がサポートされている場合は、 **AddRef**が呼び出され、**この**ポインターが返されます。 要求された識別子がサポートされているリストに含まれていない場合、出力ポインターは NULL に設定され、MAPI_E_INTERFACE_NOT_SUPPORTED 値が返されます。 
  
次のコード例は、ステータスオブジェクト ( [imapistatus: imapistatus](imapistatusimapiprop.md)インターフェイスのサブクラスであるオブジェクト) に対する**QueryInterface**を C++ で実装する方法を示しています。 **imapistatus**は、 **iunknown**から[imapistatus: iunknown](imapipropiunknown.md)を継承します。 そのため、発信者がこれらのインターフェイスのいずれかを要求した場合、インターフェイスは継承によって関連付けられるため、**この**ポインターを返すことができます。 
  
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

次のコード例は、 `CMyMAPIObject`オブジェクトの**AddRef**メソッドと**Release**メソッドを実装する方法を示しています。 **AddRef**と**Release**の実装は簡単であるため、多くのサービスプロバイダーはそれらをインラインで実装することを選択します。 Win32 関数**InterlockedIncrement**および**InterlockedDecrement**の呼び出しにより、スレッドセーフが保証されます。 オブジェクトのメモリはデストラクターによって解放されます。これは、 **Release**メソッドによってオブジェクトが削除されるときに呼び出されます。 
  
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

## <a name="see-also"></a>関連項目

- [MAPI オブジェクトの実装](implementing-mapi-objects.md)
- [IUnknown インターフェイスの実装](implementing-the-iunknown-interface.md)

