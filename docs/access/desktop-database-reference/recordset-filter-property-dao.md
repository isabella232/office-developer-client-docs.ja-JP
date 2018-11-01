---
title: Recordset.Filter プロパティ (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35ae33c9b7979e6dd98d94652a61c8737397c7a3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884304"
---
# <a name="recordsetfilter-property-dao"></a><span data-ttu-id="9da62-102">Recordset.Filter プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="9da62-102">Recordset.Filter Property (DAO)</span></span>

<span data-ttu-id="9da62-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9da62-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9da62-p101">次に開く **Recordset** オブジェクトに含めるレコードを決める値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String** ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9da62-p101">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9da62-106">構文</span><span class="sxs-lookup"><span data-stu-id="9da62-106">Syntax</span></span>

<span data-ttu-id="9da62-107">*式*です。フィルター</span><span class="sxs-lookup"><span data-stu-id="9da62-107">*expression* .Filter</span></span>

<span data-ttu-id="9da62-108">\*式\***レコード セット**オブジェクトを返す式です。</span><span class="sxs-lookup"><span data-stu-id="9da62-108">*expression* An expression that returns a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9da62-109">注釈</span><span class="sxs-lookup"><span data-stu-id="9da62-109">Remarks</span></span>

<span data-ttu-id="9da62-110">設定値または戻り値は、SQL ステートメントの WHERE 句から予約語 WHERE を除いた部分を含む文字列データ型 (String) の値です。</span><span class="sxs-lookup"><span data-stu-id="9da62-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="9da62-111">ダイナセット タイプ、スナップショット タイプまたは前方のみタイプの**Recordset**オブジェクトにフィルターを適用するのにには、 **Filter**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="9da62-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="9da62-112">**Filter** プロパティを使用すると、既存の **Recordset** オブジェクトに基づいて新しい **Recordset** オブジェクトを開くときに、既存のオブジェクトから取得するレコードを制限できます。</span><span class="sxs-lookup"><span data-stu-id="9da62-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="9da62-113">(月-日-年) 米国の日付形式を使用して、米国版の Microsoft Access データベース エンジンを使用していない場合でも、日付を含むフィールドをフィルターするとき (文字列、たとえば、strMonth を連結することにより、任意の日付をアセンブリする必要が場合 &"-"& strDay &"、"& strYear)。</span><span class="sxs-lookup"><span data-stu-id="9da62-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="9da62-114">この形式で構成されていない場合、データが予期したとおりにフィルター処理されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="9da62-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="9da62-115">多くの場合、WHERE 句が含まれた SQL ステートメントを使用すると、より短時間で新しい **Recordset** オブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="9da62-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="9da62-116">非 – 整数値と連結した文字列にプロパティを設定して、システム パラメーター、米国以外の小数点の記号、カンマなどを指定するかどうか (たとえば、strFilter ="価格\>"& lngPrice でと lngPrice = 125,50)、しようとするときにエラーが発生しました。次の**レコード セット**を開きます。</span><span class="sxs-lookup"><span data-stu-id="9da62-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="9da62-117">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Access の SQL で小数点の記号として使用できるのはピリオドのみであるためです。</span><span class="sxs-lookup"><span data-stu-id="9da62-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="9da62-118">例</span><span class="sxs-lookup"><span data-stu-id="9da62-118">Example</span></span>

<span data-ttu-id="9da62-119">次の例は、 Filter プロパティを使用して、以降に開かれる Recordset に含めるレコードを決定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9da62-119">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

<span data-ttu-id="9da62-120">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="9da62-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```
