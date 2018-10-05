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
ms.openlocfilehash: 08f3f3f937320d8a986b2002c761a37f0f749227
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397836"
---
# <a name="implementing-iunknown-in-c"></a>C++ での IUnknown の実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
C++ では[IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)、 [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)、および[リ ス](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)の[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)インターフェイスのメソッドを実装することは非常に簡単です。 渡されるパラメーターのいくつかの標準的な検証をした後は、 **QueryInterface**の実装は、サポートされているインターフェイスの一覧に対して要求されたインターフェイスの識別子をチェックします。 要求された識別子がサポートされている間にある場合は、 **AddRef**が呼び出され、 **this**ポインターが返されます。 要求された識別子がサポートされているリストにない場合は、出力のポインターは NULL に設定し、MAPI_E_INTERFACE_NOT_SUPPORTED の値が返されます。 
  
次のコード例は、状態オブジェクトのサブクラスであるオブジェクトの C++ の**QueryInterface**を実装する方法を示しています、 [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)インタ フェースです。 **IMAPIStatus**は、 **IUnknown**から継承[IMAPIProp: IUnknown](imapipropiunknown.md)。 したがって場合は、呼び出し元は、これらのインタ フェースのいずれかの確認メッセージが表示、 **this**ポインターが返されますインターフェイス継承によって関連しているため。 
  
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

コード例を次に**AddRef**および**Release**メソッドを実装する方法を示しています、`CMyMAPIObject`オブジェクトです。 **AddRef**および**Release**を実装することが簡単であるためにインラインを実装するために多くのサービス プロバイダーを選択します。 **スレッド**と**避けるため**に、Win32 関数の呼び出しは、スレッドの安全を確保します。 **Release**メソッドがオブジェクトを削除するときに呼び出されると、デストラクターでは、オブジェクト用のメモリが解放されます。 
  
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

