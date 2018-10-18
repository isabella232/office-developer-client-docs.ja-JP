---
<span data-ttu-id="6c3af-101"><<<<<<< ヘッド タイトル: 以下のプロパティ (ADO) TOCTitle: 以下のプロパティ (ADO) === タイトル: 以下のプロパティ (ADO) TOCTitle: 以下のプロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="6c3af-101"><<<<<<< HEAD title: NativeError Property (ADO) TOCTitle: NativeError Property (ADO) ======= title: NativeError property (ADO) TOCTitle: NativeError property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6c3af-102">マスターの ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15) ms:contentKeyID: 48546685 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="6c3af-102">master ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15) ms:contentKeyID: 48546685 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="6c3af-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="6c3af-103"><<<<<<< HEAD</span></span>
# <a name="nativeerror-property-ado"></a><span data-ttu-id="6c3af-104">NativeError プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="6c3af-104">NativeError Property (ADO)</span></span>
=======
# <a name="nativeerror-property-ado"></a><span data-ttu-id="6c3af-105">以下のプロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="6c3af-105">NativeError property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6c3af-106">master</span><span class="sxs-lookup"><span data-stu-id="6c3af-106">master</span></span>


<span data-ttu-id="6c3af-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c3af-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6c3af-108">指定された [Error](error-object-ado.md) オブジェクトでプロバイダー固有のエラー コードを示します。</span><span class="sxs-lookup"><span data-stu-id="6c3af-108">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="6c3af-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="6c3af-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="6c3af-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="6c3af-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="6c3af-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="6c3af-111">Return value</span></span>
>>>>>>> <span data-ttu-id="6c3af-112">master</span><span class="sxs-lookup"><span data-stu-id="6c3af-112">master</span></span>

<span data-ttu-id="6c3af-113">エラー コードを示す長整数型 ( **Long** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="6c3af-113">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c3af-114">解説</span><span class="sxs-lookup"><span data-stu-id="6c3af-114">Remarks</span></span>

<span data-ttu-id="6c3af-p101">**NativeError** プロパティは、特定の **Error** オブジェクトの、データベース固有のエラー情報を取得するために使用します。たとえば、Microsoft ODBC Provider for OLE DB と Microsoft SQL Server データベースを使う場合、SQL Server から送信されたネイティブ エラー コードは、ODBC と ODBC Provider を経由して ADO の **NativeError** プロパティに渡されます。</span><span class="sxs-lookup"><span data-stu-id="6c3af-p101">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object. For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

