---
title: ADO イベント モデルの使用例 (vc++)
TOCTitle: ADO Events Model example (VC++)
ms:assetid: 3785406b-844c-419f-e6ac-78aa8c4e78b2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249132(v=office.15)
ms:contentKeyID: 48544197
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9f4ef26113d81910fa989196a0b58865e1ca62f3
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945755"
---
# <a name="ado-events-model-example-vc"></a><span data-ttu-id="cc23f-102">ADO イベント モデルの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="cc23f-102">ADO Events Model example (VC++)</span></span>

<span data-ttu-id="cc23f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cc23f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc23f-104">「[ADO イベントのインスタンス化 (言語別)](https://msdn.microsoft.com/library/jj250244\(v=office.15\))」の Visual C++ のセクションには、ADO イベント モデルのインスタンスを作成する方法についての一般的な説明があります。</span><span class="sxs-lookup"><span data-stu-id="cc23f-104">The Visual C++ section of [ADO Event Instantiation by Language](https://msdn.microsoft.com/library/jj250244\(v=office.15\)) gives a general description of how to instantiate the ADO event model.</span></span> <span data-ttu-id="cc23f-105">次の具体的な例によって作成される環境内でイベント モデルのインスタンスを作成するのでは、**\#インポート**ディレクティブです。</span><span class="sxs-lookup"><span data-stu-id="cc23f-105">The following is a specific example of instantiating the event model within the environment created by the **\#import** directive.</span></span>

<span data-ttu-id="cc23f-106">一般的な説明では、メソッド シグネチャの参照として **adoint.h** を使います。</span><span class="sxs-lookup"><span data-stu-id="cc23f-106">The general description uses **adoint.h** as a reference for method signatures.</span></span> <span data-ttu-id="cc23f-107">ただし、全般的な説明で、いくつかの詳細を若干変更を使用した結果、**\#インポート**ディレクティブ。</span><span class="sxs-lookup"><span data-stu-id="cc23f-107">However, a few details in the general description change slightly as a result of using the **\#import** directive:</span></span>

- <span data-ttu-id="cc23f-108">**\#インポート**ディレクティブの基本的なフォームに**typedef**のおよびメソッド シグネチャのデータ型および修飾子を解決します。</span><span class="sxs-lookup"><span data-stu-id="cc23f-108">The **\#import** directive resolves **typedef**'s, and method signature data types and modifiers to their fundamental forms.</span></span>

- <span data-ttu-id="cc23f-109">純粋仮想メソッドを上書きする必要がありますが、すべて先頭に"**生\_**」です。</span><span class="sxs-lookup"><span data-stu-id="cc23f-109">The pure virtual methods that must be overwritten are all prefixed by "**raw\_**".</span></span>

<span data-ttu-id="cc23f-110">コードの一部は、単にコーディングのスタイルを示します。</span><span class="sxs-lookup"><span data-stu-id="cc23f-110">Some of the code simply reflects coding style.</span></span>

- <span data-ttu-id="cc23f-111">**Advise** メソッドが使う **IUnknown** のポインターは、 **QueryInterface** の呼び出しを使って明示的に取得されます。</span><span class="sxs-lookup"><span data-stu-id="cc23f-111">The pointer to **IUnknown** used by the **Advise** method is obtained explicitly with a call to **QueryInterface**.</span></span>

- <span data-ttu-id="cc23f-112">クラス定義にデストラクターを明示的にコーディングする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cc23f-112">You don't need to explicitly code a destructor in the class definitions.</span></span>

- <span data-ttu-id="cc23f-113">QueryInterface、AddRef、および Release に関して、より強固な実装をコーディングすることもできます。</span><span class="sxs-lookup"><span data-stu-id="cc23f-113">You may want to code more robust implementations of QueryInterface, AddRef, and Release.</span></span>

- <span data-ttu-id="cc23f-114">\*\* \_ \_Uuidof()\*\* ディレクティブは、インターフェイス Id を取得するのには広範囲に使用します。</span><span class="sxs-lookup"><span data-stu-id="cc23f-114">The **\_\_uuidof()** directive is used extensively to obtain interface IDs.</span></span>

<span data-ttu-id="cc23f-115">最後に、例には動作可能なコードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cc23f-115">Finally, the example contains some working code.</span></span>

- <span data-ttu-id="cc23f-116">例は、コンソール アプリケーションとして記述されています。</span><span class="sxs-lookup"><span data-stu-id="cc23f-116">The example is written as a console application.</span></span>

- <span data-ttu-id="cc23f-117">コメントの下で、独自のコードを挿入する必要があります」といくつかの作業を行うと"です。</span><span class="sxs-lookup"><span data-stu-id="cc23f-117">You should insert your own code under the comment, "// Do some work ".</span></span>

- <span data-ttu-id="cc23f-p103">既定では、すべてのイベント ハンドラーは、何も実行しないで後続の通知を取り消します。ユーザーは、アプリケーションに適したコードを挿入し、必要に応じて通知を利用してください。</span><span class="sxs-lookup"><span data-stu-id="cc23f-p103">All the event handlers default to doing nothing, and canceling further notifications. You should insert the appropriate code for your application, and allow notifications if required.</span></span>

<!-- end list -->

```cpp 
 
// eventmodel.cpp : Defines the entry point for the console application. 
// 
 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
#include <comdef.h> 
#include <stdio.h> 
 
//----The Connection events---------------------------------------------- 
 
class CConnEvent : public ConnectionEventsVt 
{ 
private: 
 ULONG m_cRef; 
 public: 
 CConnEvent() { m_cRef = 0; }; 
 ~CConnEvent() {}; 
 
 
 STDMETHODIMP QueryInterface(REFIID riid, void ** ppv); 
 STDMETHODIMP_(ULONG) AddRef(void); 
 STDMETHODIMP_(ULONG) Release(void); 
 
 STDMETHODIMP raw_InfoMessage( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_BeginTransComplete( 
 LONG TransactionLevel, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_CommitTransComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_RollbackTransComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_WillExecute( 
 BSTR *Source, 
 CursorTypeEnum *CursorType, 
 LockTypeEnum *LockType, 
 long *Options, 
 EventStatusEnum *adStatus, 
 struct _Command *pCommand, 
 struct _Recordset *pRecordset, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_ExecuteComplete( 
 LONG RecordsAffected, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Command *pCommand, 
 struct _Recordset *pRecordset, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_WillConnect( 
 BSTR *ConnectionString, 
 BSTR *UserID, 
 BSTR *Password, 
 long *Options, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_ConnectComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_Disconnect( 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection); 
}; 
 
//-----The Recordset events---------------------------------------------- 
 
class CRstEvent : public RecordsetEventsVt 
 { 
 private: 
 ULONG m_cRef; 
 public: 
 CRstEvent() { m_cRef = 0; }; 
 ~CRstEvent() {}; 
 
 STDMETHODIMP QueryInterface(REFIID riid, void ** ppv); 
 STDMETHODIMP_(ULONG) AddRef(void); 
 STDMETHODIMP_(ULONG) Release(void); 
 
 STDMETHODIMP raw_WillChangeField( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_FieldChangeComplete( 
 LONG cFields, 
 VARIANT Fields, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_WillChangeRecord( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_RecordChangeComplete( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_WillChangeRecordset( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_RecordsetChangeComplete( 
 EventReasonEnum adReason, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_WillMove( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_MoveComplete( 
 EventReasonEnum adReason, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_EndOfRecordset( 
 VARIANT_BOOL *fMoreData, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_FetchProgress( 
 long Progress, 
 long MaxProgress, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_FetchComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
}; 
 
 
//-----Implement each connection method---------------------------------- 
 
 STDMETHODIMP CConnEvent::raw_InfoMessage( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_BeginTransComplete( 
 LONG TransactionLevel, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_CommitTransComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_RollbackTransComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_WillExecute( 
 BSTR *Source, 
 CursorTypeEnum *CursorType, 
 LockTypeEnum *LockType, 
 long *Options, 
 EventStatusEnum *adStatus, 
 struct _Command *pCommand, 
 struct _Recordset *pRecordset, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_ExecuteComplete( 
 LONG RecordsAffected, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Command *pCommand, 
 struct _Recordset *pRecordset, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_WillConnect( 
 BSTR *ConnectionString, 
 BSTR *UserID, 
 BSTR *Password, 
 long *Options, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_ConnectComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_Disconnect( 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 
//-----Implement each recordset method----------------------------------- 
 
 STDMETHODIMP CRstEvent::raw_WillChangeField( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_FieldChangeComplete( 
 LONG cFields, 
 VARIANT Fields, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_WillChangeRecord( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_RecordChangeComplete( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_WillChangeRecordset( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_RecordsetChangeComplete( 
 EventReasonEnum adReason, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_WillMove( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_MoveComplete( 
 EventReasonEnum adReason, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_EndOfRecordset( 
 VARIANT_BOOL *fMoreData, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_FetchProgress( 
 long Progress, 
 long MaxProgress, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_FetchComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 
//-----Implement QueryInterface, AddRef, and Release--------------------- 
 
 STDMETHODIMP CRstEvent::QueryInterface(REFIID riid, void ** ppv) 
 { 
 *ppv = NULL; 
 if (riid == __uuidof(IUnknown) || 
 riid == __uuidof(RecordsetEventsVt)) *ppv = this; 
 if (*ppv == NULL) 
 return ResultFromScode(E_NOINTERFACE); 
 AddRef(); 
 return NOERROR; 
 } 
 STDMETHODIMP_(ULONG) CRstEvent::AddRef(void) { return ++m_cRef; }; 
 STDMETHODIMP_(ULONG) CRstEvent::Release() 
 { 
 if (0 != --m_cRef) return m_cRef; 
 delete this; 
 return 0; 
 } 
 
 STDMETHODIMP CConnEvent::QueryInterface(REFIID riid, void ** ppv) 
 
 { 
 *ppv = NULL; 
 if (riid == __uuidof(IUnknown) || 
 riid == __uuidof(ConnectionEventsVt)) *ppv = this; 
 if (*ppv == NULL) 
 return ResultFromScode(E_NOINTERFACE); 
 AddRef(); 
 return NOERROR; 
 } 
 STDMETHODIMP_(ULONG) CConnEvent::AddRef() { return ++m_cRef; }; 
 STDMETHODIMP_(ULONG) CConnEvent::Release() 
 { 
 if (0 != --m_cRef) return m_cRef; 
 delete this; 
 return 0; 
 } 
 
//-----Write your main block of code------------------------------------- 
 
int main(int argc, char* argv[]) 
{ 
 HRESULT hr; 
 DWORD dwConnEvt; 
 DWORD dwRstEvt; 
 IConnectionPointContainer *pCPC = NULL; 
 IConnectionPoint *pCP = NULL; 
 IUnknown *pUnk = NULL; 
 CRstEvent *pRstEvent = NULL; 
 CConnEvent *pConnEvent= NULL; 
 int rc = 0; 
 _RecordsetPtr pRst; 
 _ConnectionPtr pConn; 
 
 ::CoInitialize(NULL); 
 
 hr = pConn.CreateInstance(__uuidof(Connection)); 
 if (FAILED(hr)) return rc; 
 
 hr = pRst.CreateInstance(__uuidof(Recordset)); 
 if (FAILED(hr)) return rc; 
 
 // Start using the Connection events 
 
 hr = pConn->QueryInterface(__uuidof(IConnectionPointContainer), 
 (void **)&pCPC); 
 if (FAILED(hr)) return rc; 
 hr = pCPC->FindConnectionPoint(__uuidof(ConnectionEvents), &pCP); 
 pCPC->Release(); 
 if (FAILED(hr)) return rc; 
 
 pConnEvent = new CConnEvent(); 
 hr = pConnEvent->QueryInterface(__uuidof(IUnknown), (void **) &pUnk); 
 if (FAILED(hr)) return rc; 
 hr = pCP->Advise(pUnk, &dwConnEvt); 
 pCP->Release(); 
 if (FAILED(hr)) return rc; 
 
 // Start using the Recordset events 
 
 hr = pRst->QueryInterface(__uuidof(IConnectionPointContainer), 
 (void **)&pCPC); 
 if (FAILED(hr)) return rc; 
 hr = pCPC->FindConnectionPoint(__uuidof(RecordsetEvents), &pCP); 
 pCPC->Release(); 
 if (FAILED(hr)) return rc; 
 
 pRstEvent = new CRstEvent(); 
 hr = pRstEvent->QueryInterface(__uuidof(IUnknown), (void **) &pUnk); 
 if (FAILED(hr)) return rc; 
 hr = pCP->Advise(pUnk, &dwRstEvt); 
 pCP->Release(); 
 if (FAILED(hr)) return rc; 
 
 // Do some work 
 
 pConn->Open("dsn=Pubs;", "MyUserName", "MyPassword", adConnectUnspecified); 
 pRst->Open("SELECT * FROM authors", (IDispatch *) pConn, 
 adOpenStatic, adLockReadOnly, adCmdText); 
 pRst->MoveFirst(); 
 while (pRst->EndOfFile == FALSE) 
 { 
 wprintf(L"Name = '%s'\n", (wchar_t*) 
 ((_bstr_t) pRst->Fields->GetItem("au_lname")->Value)); 
 pRst->MoveNext(); 
 } 
 
 pRst->Close(); 
 pConn->Close(); 
 
 // Stop using the Connection events 
 
 hr = pConn->QueryInterface(__uuidof(IConnectionPointContainer), 
 (void **) &pCPC); 
 if (FAILED(hr)) return rc; 
 hr = pCPC->FindConnectionPoint(__uuidof(ConnectionEvents), &pCP); 
 pCPC->Release(); 
 if (FAILED(hr)) return rc; 
 hr = pCP->Unadvise( dwConnEvt ); 
 pCP->Release(); 
 if (FAILED(hr)) return rc; 
 
 // Stop using the Recordset events 
 hr = pRst->QueryInterface(__uuidof(IConnectionPointContainer), 
 (void **) &pCPC); 
 if (FAILED(hr)) return rc; 
 hr = pCPC->FindConnectionPoint(__uuidof(RecordsetEvents), &pCP); 
 pCPC->Release(); 
 if (FAILED(hr)) return rc; 
 hr = pCP->Unadvise( dwRstEvt ); 
 pCP->Release(); 
 if (FAILED(hr)) return rc; 
 
 CoUninitialize(); 
 return 1; 
} 
```

