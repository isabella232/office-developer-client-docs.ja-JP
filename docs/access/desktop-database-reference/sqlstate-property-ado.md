---
<span data-ttu-id="af945-101"><<<<<<< ヘッド タイトル: SQLState プロパティ (ADO) TOCTitle: SQLState プロパティ (ADO) === タイトル: SQLState プロパティ (ADO) TOCTitle: SQLState プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="af945-101"><<<<<<< HEAD title: SQLState Property (ADO) TOCTitle: SQLState Property (ADO) ======= title: SQLState property (ADO) TOCTitle: SQLState property (ADO)</span></span>
>>>>>>> <span data-ttu-id="af945-102">マスターの ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) ms:contentKeyID: 48547806 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="af945-102">master ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) ms:contentKeyID: 48547806 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="af945-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="af945-103"><<<<<<< HEAD</span></span>
# <a name="sqlstate-property-ado"></a><span data-ttu-id="af945-104">SQLState プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="af945-104">SQLState Property (ADO)</span></span>
=======
# <a name="sqlstate-property-ado"></a><span data-ttu-id="af945-105">SQLState プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="af945-105">SQLState property (ADO)</span></span>
>>>>>>> <span data-ttu-id="af945-106">master</span><span class="sxs-lookup"><span data-stu-id="af945-106">master</span></span>


<span data-ttu-id="af945-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="af945-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="af945-108">特定の [Error](error-object-ado.md) オブジェクトの SQL 状態を示します。</span><span class="sxs-lookup"><span data-stu-id="af945-108">Indicates the SQL state for a given [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="af945-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="af945-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="af945-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="af945-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="af945-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="af945-111">Return value</span></span>
>>>>>>> <span data-ttu-id="af945-112">master</span><span class="sxs-lookup"><span data-stu-id="af945-112">master</span></span>

<span data-ttu-id="af945-113">ANSI SQL 標準に準拠し、エラー コードを示す 5 文字の文字列型 ( **String** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="af945-113">Returns a five-character **String** value that follows the ANSI SQL standard and indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="af945-114">解説</span><span class="sxs-lookup"><span data-stu-id="af945-114">Remarks</span></span>

<span data-ttu-id="af945-p101">SQL ステートメントの処理中にエラーが発生した場合に、プロバイダーが返す 5 文字のエラー コードを取得するには **SQLState** プロパティを使用します。たとえば、Microsoft OLE DB Provider for ODBC を Microsoft SQL Server データベースと共に使用する場合、ODBC に固有のエラー、または Microsoft SQL Server に起因するエラーに基づいて、ODBC から SQL 状態のエラー コードが生成された後、ODBC エラーにマップされます。これらのエラー コードは ANSI SQL 標準で規定されていますが、実装方法はデータ ソースによって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="af945-p101">Use the **SQLState** property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement. For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors. These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</span></span>

