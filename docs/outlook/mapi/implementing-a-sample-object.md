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
# <a name="implementing-a-sample-object"></a><span data-ttu-id="2c522-103">サンプル オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="2c522-103">Implementing a sample object</span></span>

<span data-ttu-id="2c522-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c522-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c522-105">シンク オブジェクト [(IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) インターフェイスをサポートするオブジェクト) は、クライアント アプリケーションが通知を処理するために実装する MAPI オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="2c522-105">Advise sink objects — objects that support the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface — are MAPI objects that client applications implement for processing notifications.</span></span> <span data-ttu-id="2c522-106">**IMAPIAdviseSink** は [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) から直接継承し、1 つのメソッド **OnNotify のみを含む**。</span><span class="sxs-lookup"><span data-stu-id="2c522-106">**IMAPIAdviseSink** inherits directly from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) and contains only one method, **OnNotify**.</span></span> <span data-ttu-id="2c522-107">したがって、アアドバイス シンク オブジェクトを実装するために、クライアントは **IUnknown** および OnNotify の 3 つのメソッドのコード [を作成します](imapiadvisesink-onnotify.md)。</span><span class="sxs-lookup"><span data-stu-id="2c522-107">Therefore, to implement an advise sink object, a client creates code for the three methods in **IUnknown** and for [OnNotify](imapiadvisesink-onnotify.md).</span></span>
  
<span data-ttu-id="2c522-108">Mapidefs.h ヘッダー ファイルは、次のように **、IMAPIAdviseSink** インターフェイス **DECLARE_MAPI_INTERFACE定義します**。</span><span class="sxs-lookup"><span data-stu-id="2c522-108">The Mapidefs.h header file defines an **IMAPIAdviseSink** interface implementation by using **DECLARE_MAPI_INTERFACE**, as follows:</span></span>
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

<span data-ttu-id="2c522-109">シンク オブジェクトにアドバイスを実装するクライアントは、手動で、またはマクロを使用して、オブジェクト内のインターフェイス **MAPI_IUNKNOWN_METHODS定義MAPI_IMAPIADVISESINK_METHODS\*\*\*\*できます。**</span><span class="sxs-lookup"><span data-stu-id="2c522-109">Clients that implement advise sink objects can define their interfaces in their objects manually or with the **MAPI_IUNKNOWN_METHODS** and **MAPI_IMAPIADVISESINK_METHODS** macros.</span></span> <span data-ttu-id="2c522-110">オブジェクト実装者は、可能な限りインターフェイス マクロを使用して、オブジェクト間の一貫性を確保し、時間と労力を節約する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c522-110">Object implementers should use the interface macros whenever possible to ensure consistency across objects and to save time and effort.</span></span> 
  
<span data-ttu-id="2c522-111">[IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドと[IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドの実装は、通常は数行のコードしか必要とならないので、比較的簡単です。</span><span class="sxs-lookup"><span data-stu-id="2c522-111">Implementing the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods is relatively simple because typically only a few lines of code are needed.</span></span> <span data-ttu-id="2c522-112">したがって、オブジェクトを実装するクライアントとサービス プロバイダーは **、AddRef** 実装と Release 実装 **をインライン** にできます。</span><span class="sxs-lookup"><span data-stu-id="2c522-112">Therefore, clients and service providers that implement objects can make their **AddRef** and **Release** implementations inline.</span></span> <span data-ttu-id="2c522-113">次のコードは、AddRef と Release のインライン実装を使用して C++ アアドバイス シンク オブジェクトを定義 **する方法を** 示 **しています**。</span><span class="sxs-lookup"><span data-stu-id="2c522-113">The following code shows how to define a C++ advise sink object with inline implementations of **AddRef** and **Release**.</span></span>
  
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

<span data-ttu-id="2c522-114">C では、アアドバイス シンク オブジェクトは次の要素で構成されます。</span><span class="sxs-lookup"><span data-stu-id="2c522-114">In C, the advise sink object is composed of the following elements:</span></span>
  
- <span data-ttu-id="2c522-115">**IUnknown** および **IMAPIAdviseSink** の各メソッドの実装へのポインターを含む vtable へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2c522-115">A pointer to a vtable that contains pointers to implementations of each of the methods in **IUnknown** and **IMAPIAdviseSink**.</span></span>
    
- <span data-ttu-id="2c522-116">データ メンバー。</span><span class="sxs-lookup"><span data-stu-id="2c522-116">Data members.</span></span>
    
<span data-ttu-id="2c522-117">次のコード例は、C でアアドバイス シンク オブジェクトを定義し、その vtable を構築する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="2c522-117">The following code example shows how to define an advise sink object in C and construct its vtable.</span></span> 
  
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

<span data-ttu-id="2c522-118">C でオブジェクトを宣言した後、次のコードに示すように、vtable ポインターを構築された vtable のアドレスに設定して初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c522-118">After you declare an object in C, you must initialize it by setting the vtable pointer to the address of the constructed vtable, as shown in the following code:</span></span>
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a><span data-ttu-id="2c522-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c522-119">See also</span></span>

- [<span data-ttu-id="2c522-120">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="2c522-120">MAPI Property Overview</span></span>](mapi-property-overview.md)
- [<span data-ttu-id="2c522-121">MAPI オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="2c522-121">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

