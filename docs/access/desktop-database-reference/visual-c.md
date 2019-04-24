---
title: Visual C++ (Access デスクトップデータベースリファレンス)
TOCTitle: Visual C++
ms:assetid: 31d27968-e7bd-02fa-efad-26039bea30b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249091(v=office.15)
ms:contentKeyID: 48544062
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 082790c33840bfeacf0c1a6bd38af34c0617f4fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303403"
---
# <a name="visual-c"></a><span data-ttu-id="25d81-102">Visual C++</span><span class="sxs-lookup"><span data-stu-id="25d81-102">Visual C++</span></span>


<span data-ttu-id="25d81-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="25d81-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="25d81-104">ここでは、Microsoft Visual C++ で ADO イベントをインスタンス化する方法の概略を示します。</span><span class="sxs-lookup"><span data-stu-id="25d81-104">This is a schematic description of how to instantiate ADO events in Microsoft Visual C++.</span></span> <span data-ttu-id="25d81-105">詳細については、「 [ADO Events Model example (VC + +)](ado-events-model-example-vc.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25d81-105">See [ADO Events Model example (VC++)](ado-events-model-example-vc.md) for a complete description.</span></span>

<span data-ttu-id="25d81-106">ファイル adoint.h で定義されている **ConnectionEventsVt** インターフェイスおよび **RecordsetEventsVt** インターフェイスから派生するクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="25d81-106">Create classes derived from the **ConnectionEventsVt** and **RecordsetEventsVt** interfaces found in the file adoint.h.</span></span>

```cpp 
 
// BeginEventExampleVC01 
class CConnEvent : public ConnectionEventsVt 
{ 
 public: 
 STDMETHODIMP InfoMessage( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADOConnection *pConnection); 
... 
} 
 
class CRstEvent : public RecordsetEventsVt 
{ 
 public: 
 STDMETHODIMP WillChangeField( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset); 
... 
} 
// EndEventExampleVC01 
```

<span data-ttu-id="25d81-107">両方のクラスに、各イベント ハンドラー メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="25d81-107">Implement each of the event-handler methods in both classes.</span></span> <span data-ttu-id="25d81-108">各メソッドは、HRESULT の\_戻り値を返すだけで十分です。</span><span class="sxs-lookup"><span data-stu-id="25d81-108">It is sufficient that each method merely return an HRESULT of S\_OK.</span></span> <span data-ttu-id="25d81-109">しかし、イベント ハンドラーが使用できることを通知すると、既定ではそのイベント ハンドラーが継続的に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="25d81-109">However, when you make it known that your event handlers are available, they will be called continuously by default.</span></span> <span data-ttu-id="25d81-110">これを無効にして、2 回目以降は通知しないよう要求するには、 **adStatus** を **adStatusUnwantedEvent** に設定します。</span><span class="sxs-lookup"><span data-stu-id="25d81-110">Instead, you might want to request no further notification after the first time by setting **adStatus** to **adStatusUnwantedEvent**.</span></span>

```cpp 
 
// BeginEventExampleVC02 
STDMETHODIMP CConnEvent::ConnectComplete( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADOConnection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
// EndEventExampleVC02 
```

<span data-ttu-id="25d81-p103">イベント クラスは **IUnknown** から継承されるため、 **QueryInterface** 、 **AddRef** 、および **Release** の各メソッドも実装する必要があります。また、クラスのコンストラクターとデストラクターも実装します。この部分の作業を簡単に実行できるよう、最も使いやすい Visual C++ ツールを使用してください。</span><span class="sxs-lookup"><span data-stu-id="25d81-p103">The event classes inherit from **IUnknown**, so you must also implement the **QueryInterface**, **AddRef**, and **Release** methods. Also implement class constructors and destructors. Choose the Visual C++ tools with which you are most comfortable to simplify this part of the task.</span></span>

<span data-ttu-id="25d81-p104">**Recordset** (英語) オブジェクトおよび [Connection](recordset-object-ado.md) オブジェクトで、 [IConnectionPointContainer](connection-object-ado.md) インターフェイスおよび **IConnectionPoint** インターフェイスに対する **QueryInterface** を発行して、イベント ハンドラーが使用できることを通知します。その後、各クラスの **IConnectionPoint::Advise** を発行します。</span><span class="sxs-lookup"><span data-stu-id="25d81-p104">Make it known that your event handlers are available by issuing **QueryInterface** on the [Recordset](recordset-object-ado.md) and [Connection](connection-object-ado.md) objects for the **IConnectionPointContainer** and **IConnectionPoint** interfaces. Then issue **IConnectionPoint::Advise** for each class.</span></span>

<span data-ttu-id="25d81-116">たとえば、使用可能なイベント ハンドラーが存在することを **Recordset** に正常に通知できた場合に **True** を返すブール型 (Boolean) 関数を使用するとします。</span><span class="sxs-lookup"><span data-stu-id="25d81-116">For example, assume you are using a Boolean function that returns **True** if it successfully informs a **Recordset** object that you have event handlers available.</span></span>

```cpp 
 
// BeginEventExampleVC03 
HRESULT hr; 
DWORD dwEvtClass; 
IConnectionPointContainer *pCPC = NULL; 
IConnectionPoint *pCP = NULL; 
CRstEvent *pRStEvent = NULL; 
... 
_RecordsetPtr pRs; 
pRs.CreateInstance(__uuidof(Recordset)); 
pRStEvent = new CRstEvent; 
if (pRStEvent == NULL) return FALSE; 
... 
hr = pRs->QueryInterface(IID_IConnectionPointContainer, (LPVOID *)&pCPC); 
if (FAILED(hr)) return FALSE; 
hr = pCPC->FindConnectionPoint(RecordsetEvents, &pCP); 
pCPC->Release(); // Always Release now, even before checking. 
if (FAILED(hr)) return FALSE; 
hr = pCP->Advise(pRstEvent, &dwEvtClass); //Turn on event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
return TRUE; 
... 
// EndEventExampleVC03 
```

<span data-ttu-id="25d81-117">この時点では、 **RecordsetEvent** ファミリのイベントが有効になっており、 **Recordset** のイベントが発生すると、作成したメソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="25d81-117">At this point, events for the **RecordsetEvent** family are enabled and your methods will be called as **Recordset** events occur.</span></span>

<span data-ttu-id="25d81-118">その後、イベント ハンドラーを使用できないようにするときは、接続ポイントを再度取得し、 **IConnectionPoint::Unadvise** メソッドを発行します。</span><span class="sxs-lookup"><span data-stu-id="25d81-118">Later, when you want to make your event handlers unavailable, get the connection point again and issue the **IConnectionPoint::Unadvise** method.</span></span>

```cpp 
 
// BeginEventExampleVC04 
... 
hr = pCP->Unadvise(dwEvtClass); //Turn off event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
// EndEventExampleVC04 
```

<span data-ttu-id="25d81-119">必要に応じて、インターフェイスを解放し、クラス オブジェクトを破棄する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25d81-119">You must release interfaces and destroy class objects as appropriate.</span></span>

<span data-ttu-id="25d81-120">次のコードは、 **Recordset** のイベント シンク クラスの例全体を示しています。</span><span class="sxs-lookup"><span data-stu-id="25d81-120">The following code shows a complete example of a **Recordset** Event sink class.</span></span>

```vb 
 
// BeginEventExampleVC05 
#include <adoint.h> 
 
class CADORecordsetEvents : public RecordsetEventsVt 
{ 
public : 
 
 ULONG m_ulRefCount; 
 CADORecordsetEvents():m_ulRefCount(1){} 
 
 STDMETHOD(QueryInterface)(REFIID iid, LPVOID * ppvObject) 
 { 
 if (IsEqualIID(__uuidof(IUnknown), iid) || 
 IsEqualIID(__uuidof(RecordsetEventsVt), iid)) 
 { 
 *ppvObject = this; 
 return S_OK; 
 } 
 else 
 return E_NOINTERFACE; 
 } 
 
 STDMETHOD_(ULONG, AddRef)() 
 { 
 return m_ulRefCount++; 
 } 
 
 STDMETHOD_(ULONG, Release)() 
 { 
 if (--m_ulRefCount == 0) 
 { 
 delete this; 
 return 0; 
 } 
 else 
 return m_ulRefCount; 
 } 
 
 
 STDMETHOD(WillChangeField)( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(FieldChangeComplete)( 
 LONG cFields, 
 VARIANT Fields, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(WillChangeRecord)( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(RecordChangeComplete)( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(WillChangeRecordset)( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(RecordsetChangeComplete)( 
 EventReasonEnum adReason, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(WillMove)( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(MoveComplete)( 
 EventReasonEnum adReason, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(EndOfRecordset)( 
 VARIANT_BOOL *fMoreData, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(FetchProgress)( 
 long Progress, 
 long MaxProgress, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(FetchComplete)( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
}; 
// EndEventExampleVC05 
```

