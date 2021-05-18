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
  
C++ での[IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) [、IUnknown::AddRef、](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)[および IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドの実装は、かなり簡単です。 [](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) 渡されるパラメーターの標準的な検証の後 **、QueryInterface** の実装は、要求されたインターフェイスの識別子とサポートされているインターフェイスの一覧をチェックします。 要求された識別子がサポートされている識別子の中に含まれる場合 **、AddRef** が呼び出され、この **ポインター** が返されます。 要求された識別子がサポートされているリストに含めされていない場合、出力ポインターは NULL に設定され、MAPI_E_INTERFACE_NOT_SUPPORTED値が返されます。 
  
次のコード例は、状態オブジェクト [(IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)インターフェイスのサブクラスであるオブジェクト) に対して C++ で **QueryInterface** を実装する方法を示しています。 **IMAPIStatus は****、IUnknown** から [IMAPIProp : IUnknown を介して継承します](imapipropiunknown.md)。 したがって、呼び出し元がこれらのインターフェイスを求める場合は、継承によってインターフェイスが関連付けされるため、このポインターを返すことができます。 
  
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

次のコード例は、オブジェクトの **AddRef** メソッドと **Release** メソッドを実装する方法を示  `CMyMAPIObject` しています。 AddRef と Releaseの **実装は** 簡単なので、多くのサービス プロバイダーがインラインで実装を選択しています。 Win32 関数の呼び出し **は、InterlockedIncrement** と **InterlockedDecrement** によってスレッドの安全性を確保します。 オブジェクトのメモリは、Release メソッドがオブジェクトを削除するときに呼び出されるデストラクタによって解放されます。 
  
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

