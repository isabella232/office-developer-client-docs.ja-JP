---
title: C++ でのオブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 89247ca1b263d6f06af73f1ffa14709a2aff23de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432955"
---
# <a name="implementing-objects-in-c"></a>C++ でのオブジェクトの実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
C++ クライアントおよびサービスプロバイダーは、実装するインターフェイスから継承するクラスを作成することによって、MAPI オブジェクトを定義します。 各インターフェイスメソッドは、クラスのコンストラクターおよびデストラクターとして、public になります。 クラスに追加のメソッドがある場合は、実装に応じてパブリックまたはプライベートにすることができます。 すべてのデータメンバーがプライベートである。 
  
次のコード例は、C++ status オブジェクトを定義する方法を示しています。 クラス`CMyMAPIObject`は[imapistatus: imapistatus](imapistatusimapiprop.md)インターフェイスから継承します。 この例で使用されているマクロの多くは、OLE ヘッダーファイル compobj で定義されています。 クラスの最初のメンバーは、基本インターフェイスのメソッドです。その後に、継承されたインターフェイスのメソッドが継承順に続きます。 インターフェイス定義の後には、追加のメソッド、コンストラクターとデストラクター、データメンバーがあります。 
  
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

`CMyMAPIObject`クラスのインスタンスを使用するために、C++ クライアントまたはサービスプロバイダーは、次のように、そのメソッドのいずれかに呼び出しを行います。 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>関連項目

- [MAPI オブジェクトの実装](implementing-mapi-objects.md)

