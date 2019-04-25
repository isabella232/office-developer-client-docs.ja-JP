---
title: Recordset.Filter プロパティ (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 7ab090dd6cf0b6e2676cf05907ac77c438f22652
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284821"
---
# <a name="recordsetfilter-property-dao"></a><span data-ttu-id="c2415-102">Recordset.Filter プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="c2415-102">Recordset.Filter Property (DAO)</span></span>

<span data-ttu-id="c2415-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2415-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2415-p101">次に開く **Recordset** オブジェクトに含めるレコードを決める値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 (**String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c2415-p101">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2415-106">構文</span><span class="sxs-lookup"><span data-stu-id="c2415-106">Syntax</span></span>

<span data-ttu-id="c2415-107">*式* .Filter</span><span class="sxs-lookup"><span data-stu-id="c2415-107">expression  . Filter</span></span>

<span data-ttu-id="c2415-108">*式\*\*\*Recordset*\* オブジェクトを返す式。</span><span class="sxs-lookup"><span data-stu-id="c2415-108">*expression*  An expression that returns a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2415-109">注釈</span><span class="sxs-lookup"><span data-stu-id="c2415-109">Remarks</span></span>

<span data-ttu-id="c2415-110">設定値または戻り値は、SQL ステートメントの WHERE 句から予約語 WHERE を除いた部分を含む文字列データ型 (String) の値です。</span><span class="sxs-lookup"><span data-stu-id="c2415-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="c2415-111">
            \*\*Filter\*\* プロパティを使用して、ダイナセット タイプ、スナップショット タイプ、または前方スクロール タイプの \*\*Recordset\*\* オブジェクトにフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="c2415-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="c2415-112">
            \*\*Filter\*\* プロパティを使用すると、既存の \*\*Recordset\*\* オブジェクトに基づいて新しい \*\*Recordset\*\* オブジェクトを開くときに、既存のオブジェクトから取得するレコードを制限できます。</span><span class="sxs-lookup"><span data-stu-id="c2415-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="c2415-113">日付が含まれたフィールドをフィルター処理するときは、米国版の Microsoft Access データベース エンジンを使用していない場合でも、米国の日付形式 (month-day-year) を使用します (この場合、連結文字列を使用して日付を構成する必要があり、たとえば、strMonth & "-" & strDay & "-" & strYear のように設定します)。</span><span class="sxs-lookup"><span data-stu-id="c2415-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="c2415-114">この形式で構成されていない場合、データが予期したとおりにフィルター処理されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="c2415-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="c2415-115">多くの場合、WHERE 句が含まれた SQL ステートメントを使用すると、より短時間で新しい **Recordset** オブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="c2415-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="c2415-116">このプロパティを文字列と非整数値を連結した値に設定し、かつシステム パラメーターでコンマなどのピリオド以外の小数点の記号が使用されている場合 (たとえば、strFilter = "PRICE \> " & lngPrice で lngPrice = 125,50)、次の **Recordset** オブジェクトを開こうとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="c2415-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE > " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next Recordset.</span></span> <span data-ttu-id="c2415-117">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Access の SQL で小数点の記号として使用できるのはピリオドのみであるためです。</span><span class="sxs-lookup"><span data-stu-id="c2415-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="c2415-118">例</span><span class="sxs-lookup"><span data-stu-id="c2415-118">Example</span></span>

<span data-ttu-id="c2415-119">次の例は、Filter プロパティを使用して、以降に開かれる Recordset に含めるレコードを決定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="c2415-119">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

<span data-ttu-id="c2415-120">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="c2415-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
