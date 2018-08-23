---
title: C++ でオブジェクトを実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4c233f9855674080496b2e54ba9548a53738ead8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574728"
---
# <a name="implementing-objects-in-c"></a>C++ でオブジェクトを実装します。

**適用されます**: Outlook 2013 |Outlook 2016 
  
C++ クライアントおよびサービス ・ プロバイダーは、それらを実装しているインターフェイスから継承するクラスを作成することで MAPI オブジェクトを定義します。 クラスのデストラクターとコンス トラクターは、インターフェイスのメソッドはパブリックで。 クラスは、追加のメソッドを持っている場合、パブリックまたはプライベートの実装によって、できます。 すべてのデータ メンバーは、プライベートです。 
  
次のコード例では、C++ の状態オブジェクトを定義する方法を示します。 `CMyMAPIObject`クラスから継承、 [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)インタ フェースです。 この例で使用されているマクロの多くは、OLE ヘッダー ファイル Compobj.h で定義されます。 クラスの最初のメンバーは、継承の順序で継承されたインターフェイスのメソッドの後に、基本インターフェイスのメソッドです。 追加のメソッド、コンス トラクター、デストラクター、およびデータ メンバーには次のインターフェイス定義です。 
  
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

インスタンスを使用して、`CMyMAPIObject`クラス、C++ クライアントまたはサービス プロバイダーのメソッドのいずれかの呼び出しを行う次のようにします。 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>関連項目

- [MAPI オブジェクトの実装](implementing-mapi-objects.md)

