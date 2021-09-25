---
title: C++ でのオブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2b471dc260731aedc3b97a134a0facee1ef7471e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579886"
---
# <a name="implementing-objects-in-c"></a>C++ でのオブジェクトの実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
C++ クライアントとサービス プロバイダーは、実装しているインターフェイスから継承するクラスを作成して MAPI オブジェクトを定義します。 各インターフェイス メソッドは、クラスのコンストラクターとデストラクタと同様にパブリックです。 クラスに追加のメソッドがある場合は、実装に応じてパブリックまたはプライベートにできます。 すべてのデータ メンバーはプライベートです。 
  
次のコード例は、C++ 状態オブジェクトを定義する方法を示しています。 クラス  `CMyMAPIObject` は [IMAPIStatus : IMAPIProp インターフェイスから継承](imapistatusimapiprop.md) します。 この例で使用されるマクロの多くは、OLE ヘッダー ファイル Compobj.h で定義されています。 クラスの最初のメンバーは、基本インターフェイスのメソッドで、継承順に継承されたインターフェイスのメソッドが続きます。 インターフェイス定義の後には、追加のメソッド、コンストラクターとデストラクタ、およびデータ メンバーが含まれます。 
  
```cpp
class  CMyMAPIObject : public IMAPIStatus
{
public:
// Methods of IUnknown.
    STDMETHODIMP QueryInterface (REFIID riid, LPVOID * ppvObj);
    STDMETHODIMP_(ULONG) AddRef ();
    STDMETHODIMP_(ULONG) Release ();
    MAPI_IMAPIPROP_METHODS(IMPL);
    MAPI_IMAPISTATUS_METHODS(IMPL);
// Other methods specific to CMyMAPIObject.
    BOOL WINAPI Method1 ();
    void WINAPI Method2 ();
// Constructors and destructors.
public :
    CMyMAPIObject () {};
    ~CMyMAPIObject () {};
// Data members specific to CMyMAPIObject.
private :
    ULONG               m_cRef;
    CAnotherObj *       m_pObj;
};
 
```

クラスのインスタンスを使用するには、C++ クライアントまたはサービス プロバイダーが次のようにそのメソッドの 1 つを  `CMyMAPIObject` 呼び出します。 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>関連項目

- [MAPI オブジェクトの実装](implementing-mapi-objects.md)

