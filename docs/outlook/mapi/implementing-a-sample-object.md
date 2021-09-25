---
title: サンプル オブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8f2613dae143de41276e105a32a0d504aeb5b886
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551262"
---
# <a name="implementing-a-sample-object"></a>サンプル オブジェクトの実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
シンク オブジェクト [(IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) インターフェイスをサポートするオブジェクト) は、クライアント アプリケーションが通知を処理するために実装する MAPI オブジェクトです。 **IMAPIAdviseSink** は [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) から直接継承し、1 つのメソッド **OnNotify のみを含む**。 したがって、アアドバイス シンク オブジェクトを実装するために、クライアントは **IUnknown** および OnNotify の 3 つのメソッドのコード [を作成します](imapiadvisesink-onnotify.md)。
  
Mapidefs.h ヘッダー ファイルは、次のように **、IMAPIAdviseSink** インターフェイス **DECLARE_MAPI_INTERFACE定義します**。
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

シンク オブジェクトにアドバイスを実装するクライアントは、手動で、またはマクロを使用して、オブジェクト内のインターフェイス **MAPI_IUNKNOWN_METHODS定義MAPI_IMAPIADVISESINK_METHODS****できます。** オブジェクト実装者は、可能な限りインターフェイス マクロを使用して、オブジェクト間の一貫性を確保し、時間と労力を節約する必要があります。 
  
[IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドと[IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドの実装は、通常は数行のコードしか必要とならないので、比較的簡単です。 したがって、オブジェクトを実装するクライアントとサービス プロバイダーは **、AddRef** 実装と Release 実装 **をインライン** にできます。 次のコードは、AddRef と Release のインライン実装を使用して C++ アアドバイス シンク オブジェクトを定義 **する方法を** 示 **しています**。
  
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

C では、アアドバイス シンク オブジェクトは次の要素で構成されます。
  
- **IUnknown** および **IMAPIAdviseSink** の各メソッドの実装へのポインターを含む vtable へのポインター。
    
- データ メンバー。
    
次のコード例は、C でアアドバイス シンク オブジェクトを定義し、その vtable を構築する方法を示しています。 
  
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

