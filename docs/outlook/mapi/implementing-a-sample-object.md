---
title: サンプル オブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a681e68c0718e49da331946d75ecb7b4fab7afe2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332831"
---
# <a name="implementing-a-sample-object"></a>サンプル オブジェクトの実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
アドバイズシンクオブジェクト- [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md)インターフェイスをサポートするオブジェクトは、クライアントアプリケーションが通知を処理するために実装する MAPI オブジェクトです。 **IMAPIAdviseSink**は[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)から直接継承し、 **notify**という1つのメソッドのみを含みます。 そのため、アドバイズシンクオブジェクトを実装するために、クライアントは**IUnknown**および[onnotify](imapiadvisesink-onnotify.md)の3つのメソッドのコードを作成します。
  
mapidefs.h ヘッダーファイルは、次のように**DECLARE_MAPI_INTERFACE**を使用して**IMAPIAdviseSink**インターフェイスの実装を定義します。
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

アドバイズシンクオブジェクトを実装するクライアントは、手動で、または**MAPI_IUNKNOWN_METHODS**および**MAPI_IMAPIADVISESINK_METHODS**マクロを使用して、オブジェクト内でインターフェイスを定義できます。 オブジェクト実装者は、可能な限りインターフェイスマクロを使用して、オブジェクト間の一貫性を確保し、時間と労力を節約する必要があります。 
  
[iunknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドと[iunknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドの実装は比較的単純です。通常はわずかな数行のコードが必要になります。 そのため、オブジェクトを実装するクライアントおよびサービスプロバイダーは、 **AddRef**および**Release**の実装をインラインにすることができます。 次のコードは、 **AddRef**および**Release**のインライン実装を使用して C++ アドバイズシンクオブジェクトを定義する方法を示しています。
  
```cpp
class  CMAPIAdviseSink : public IMAPIAdviseSink
{
public:
    STDMETHODIMP QueryInterface
                    (REFIID                     riid,
                     LPVOID *                   ppvObj);
    inline STDMETHODIMP_(ULONG) AddRef
                    () { InterlockedIncrement(m_cRef);
                         ++m_cRef;
                         InterlockedDecrement(m_cRef);
                         return m_cRef; };
    inline STDMETHODIMP_(ULONG) Release
                    () { InterlockedIncrement(m_cRef);
                         ULONG ulCount = --m_cRef;
                         InterlockedDecrement(m_cRef);
                         if (!ulCount)  delete this;
                         return ulCount;};
    MAPI_IMAPIADVISESINK_METHODS(IMPL);
    BOOL WINAPI AddConnection (LPMDB pMDBObj, ULONG ulConnection);
    void WINAPI RemoveAllLinks (LPMDB pMDBObj);
// Constructors and destructors.
public :
    inline CMAPIAdviseSink  (CStoreClient * pStore)
                            { m_cRef = 1;
                              m_ulConnection = 0;
                              m_pStore = pStore;
                              AddRef;};
    ~CMAPIAdviseSink () {Release};
private :
    ULONG               m_cRef;
    CStoreClient *      m_pStore;
    ULONG               m_ulConnection;
};
 
```

C では、アドバイズシンクオブジェクトは次の要素で構成されています。
  
- **IUnknown**および**IMAPIAdviseSink**の各メソッドの実装へのポインターを含む vtable へのポインター。
    
- データメンバー。
    
次のコード例は、C でアドバイズシンクオブジェクトを定義し、その vtable を構築する方法を示しています。 
  
```cpp
// Object definition.
typedef struct _ADVISESINK
{
    const ADVISE_Vtbl FAR *    lpVtbl;
    ULONG             cRef;
    STORECLIENT      *pStore;
    ULONG             ulConnection;
} ADVISESINK, *LPADVISESINK;
// vtable definition.
static const ADVISE_Vtbl vtblADVISE =
{
    ADVISE_QueryInterface,
    ADVISE_AddRef,
    ADVISE_Release,
    ADVISE_OnNotify
};
 
```

C でオブジェクトを宣言した後、次のコードに示すように、vtable ポインターを構築された vtable のアドレスに設定して初期化する必要があります。
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a>関連項目

- [MAPI のプロパティの概要](mapi-property-overview.md)
- [MAPI オブジェクトの実装](implementing-mapi-objects.md)

