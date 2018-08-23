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
# <a name="implementing-a-sample-object"></a><span data-ttu-id="a555c-103">サンプル オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="a555c-103">Implementing a sample object</span></span>

<span data-ttu-id="a555c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a555c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a555c-105">通知シンク オブジェクト-オブジェクトをサポートする、 [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md)インターフェイス-は、MAPI オブジェクトの通知を処理するためのクライアント アプリケーションを実装することです。</span><span class="sxs-lookup"><span data-stu-id="a555c-105">Advise sink objects — objects that support the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface — are MAPI objects that client applications implement for processing notifications.</span></span> <span data-ttu-id="a555c-106">**IMAPIAdviseSink**では、 [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)から直接継承し、 **OnNotify**1 つのメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a555c-106">**IMAPIAdviseSink** inherits directly from [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) and contains only one method, **OnNotify**.</span></span> <span data-ttu-id="a555c-107">したがって、アドバイズ シンク オブジェクトを実装するには、クライアントは**IUnknown**の 3 つの方法と[OnNotify](imapiadvisesink-onnotify.md)コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="a555c-107">Therefore, to implement an advise sink object, a client creates code for the three methods in **IUnknown** and for [OnNotify](imapiadvisesink-onnotify.md).</span></span>
  
<span data-ttu-id="a555c-108">Mapidefs.h ヘッダー ファイルでは、次のように**DECLARE_MAPI_INTERFACE**を使用して、 **IMAPIAdviseSink**インターフェイスの実装を定義します。</span><span class="sxs-lookup"><span data-stu-id="a555c-108">The Mapidefs.h header file defines an **IMAPIAdviseSink** interface implementation by using **DECLARE_MAPI_INTERFACE**, as follows:</span></span>
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

<span data-ttu-id="a555c-109">実装するクライアントは、シンク オブジェクトは、手動でまたは**MAPI_IUNKNOWN_METHODS**と**MAPI_IMAPIADVISESINK_METHODS**のマクロを使用に、そのオブジェクトのインタ フェースを定義できますを案内します。</span><span class="sxs-lookup"><span data-stu-id="a555c-109">Clients that implement advise sink objects can define their interfaces in their objects manually or with the **MAPI_IUNKNOWN_METHODS** and **MAPI_IMAPIADVISESINK_METHODS** macros.</span></span> <span data-ttu-id="a555c-110">オブジェクトの実装は、オブジェクト間での整合性を確保し、時間と労力を節約するのには可能な限りインターフェイスのマクロを使用してください。</span><span class="sxs-lookup"><span data-stu-id="a555c-110">Object implementers should use the interface macros whenever possible to ensure consistency across objects and to save time and effort.</span></span> 
  
<span data-ttu-id="a555c-111">通常はわずか数行のコードが必要なために、 [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)と[リ ス](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)のメソッドの実装は比較的簡単です。</span><span class="sxs-lookup"><span data-stu-id="a555c-111">Implementing the [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) and [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) methods is relatively simple because typically only a few lines of code are needed.</span></span> <span data-ttu-id="a555c-112">したがって、クライアントとオブジェクトを実装するサービス プロバイダーは、 **AddRef**および**Release**の実装のインラインを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a555c-112">Therefore, clients and service providers that implement objects can make their **AddRef** and **Release** implementations inline.</span></span> <span data-ttu-id="a555c-113">次のコードは、C++ を定義する方法を示します**AddRef**および**Release**のインライン実装のシンク オブジェクトに通知します。</span><span class="sxs-lookup"><span data-stu-id="a555c-113">The following code shows how to define a C++ advise sink object with inline implementations of **AddRef** and **Release**.</span></span>
  
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

<span data-ttu-id="a555c-114">C では、アドバイズ シンク オブジェクトは、次の要素で構成されます。</span><span class="sxs-lookup"><span data-stu-id="a555c-114">In C, the advise sink object is composed of the following elements:</span></span>
  
- <span data-ttu-id="a555c-115">各**IUnknown**と**IMAPIAdviseSink**内のメソッドの実装へのポインターが含まれている vtable へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a555c-115">A pointer to a vtable that contains pointers to implementations of each of the methods in **IUnknown** and **IMAPIAdviseSink**.</span></span>
    
- <span data-ttu-id="a555c-116">データ メンバーです。</span><span class="sxs-lookup"><span data-stu-id="a555c-116">Data members.</span></span>
    
<span data-ttu-id="a555c-117">次のコード例では、C のアドバイズ シンク オブジェクトを定義し、v テーブルを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a555c-117">The following code example shows how to define an advise sink object in C and construct its vtable.</span></span> 
  
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

<span data-ttu-id="a555c-118">C 内のオブジェクトを宣言した後する必要があります初期化する vtable ポインターを構築された、vtable のアドレスに設定することで次のコードに示すように。</span><span class="sxs-lookup"><span data-stu-id="a555c-118">After you declare an object in C, you must initialize it by setting the vtable pointer to the address of the constructed vtable, as shown in the following code:</span></span>
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a><span data-ttu-id="a555c-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="a555c-119">See also</span></span>

- [<span data-ttu-id="a555c-120">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="a555c-120">MAPI Property Overview</span></span>](mapi-property-overview.md)
- [<span data-ttu-id="a555c-121">MAPI オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="a555c-121">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

