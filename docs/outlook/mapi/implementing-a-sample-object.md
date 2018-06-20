---
title: サンプル オブジェクトを実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 85de8dd7211fa19b7cdbda9f5ced1f00a736ca9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800913"
---
# <a name="implementing-a-sample-object"></a>サンプル オブジェクトを実装します。

**適用されます**: Outlook 
  
通知シンク オブジェクト-オブジェクトをサポートする、 [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md)インターフェイス-は、MAPI オブジェクトの通知を処理するためのクライアント アプリケーションを実装することです。 **IMAPIAdviseSink**では、 [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)から直接継承し、 **OnNotify**1 つのメソッドが含まれています。 したがって、アドバイズ シンク オブジェクトを実装するには、クライアントは**IUnknown**の 3 つの方法と[OnNotify](imapiadvisesink-onnotify.md)コードを作成します。
  
Mapidefs.h ヘッダー ファイルでは、次のように**DECLARE_MAPI_INTERFACE**を使用して、 **IMAPIAdviseSink**インターフェイスの実装を定義します。
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

実装するクライアントは、シンク オブジェクトは、手動でまたは**MAPI_IUNKNOWN_METHODS**と**MAPI_IMAPIADVISESINK_METHODS**のマクロを使用に、そのオブジェクトのインタ フェースを定義できますを案内します。 オブジェクトの実装は、オブジェクト間での整合性を確保し、時間と労力を節約するのには可能な限りインターフェイスのマクロを使用してください。 
  
通常はわずか数行のコードが必要なために、 [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)と[リ ス](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)のメソッドの実装は比較的簡単です。 したがって、クライアントとオブジェクトを実装するサービス プロバイダーは、 **AddRef**および**Release**の実装のインラインを作成できます。 次のコードは、C++ を定義する方法を示します**AddRef**および**Release**のインライン実装のシンク オブジェクトに通知します。
  
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

C では、アドバイズ シンク オブジェクトは、次の要素で構成されます。
  
- 各**IUnknown**と**IMAPIAdviseSink**内のメソッドの実装へのポインターが含まれている vtable へのポインター。
    
- データ メンバーです。
    
次のコード例では、C のアドバイズ シンク オブジェクトを定義し、v テーブルを作成する方法を示します。 
  
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

C 内のオブジェクトを宣言した後する必要があります初期化する vtable ポインターを構築された、vtable のアドレスに設定することで次のコードに示すように。
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a>関連項目

- [MAPI Property Overview](mapi-property-overview.md)
- [MAPI オブジェクトを実装します。](implementing-mapi-objects.md)

