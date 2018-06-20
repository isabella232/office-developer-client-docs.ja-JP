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
ms.openlocfilehash: ea9f37183f33459b09f2730b3efbb7afed3d4766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800937"
---
# <a name="implementing-objects-in-c"></a>C++ でオブジェクトを実装します。

**適用されます**: Outlook 
  
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

- [MAPI オブジェクトを実装します。](implementing-mapi-objects.md)

