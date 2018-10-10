---
title: Microsoft Access SQL と ANSI SQL の比較
TOCTitle: Comparison of Microsoft Access SQL and ANSI SQL
ms:assetid: 0686f98f-10fe-0e02-e9d1-84ff3e755b57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844937(v=office.15)
ms:contentKeyID: 48543052
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd28cebe731ee3c922adec0bc3357e998dc1959b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477642"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a><span data-ttu-id="fa1ef-102">Microsoft Access SQL と ANSI SQL の比較</span><span class="sxs-lookup"><span data-stu-id="fa1ef-102">Comparison of Microsoft Access SQL and ANSI SQL</span></span>


<span data-ttu-id="fa1ef-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa1ef-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fa1ef-p101">Microsoft Access データベース エンジン SQL は、ANSI 文字セット 89 レベル 1 の仕様にほぼ準拠しています。ただし、Microsoft® Access SQL は一部の ANSI SQL 機能に対応していません。その一方で、ANSI SQL ではサポートされていない予約語や機能が実装されています。</span><span class="sxs-lookup"><span data-stu-id="fa1ef-p101">Microsoft Access database engine SQL is generally ANSI-89 Level 1 compliant. However, certain ANSI SQL features are not implemented in Microsoft® Access SQL. Conversely, Microsoft Access SQL includes reserved words and features not supported in ANSI SQL.</span></span>

## <a name="major-differences"></a><span data-ttu-id="fa1ef-107">主な相違点</span><span class="sxs-lookup"><span data-stu-id="fa1ef-107">Major Differences</span></span>

  - <span data-ttu-id="fa1ef-p102">Microsoft Office Access SQL と ANSI SQL とでは、異なる予約語およびデータ型があります。詳細については、「[SQL 予約語](sql-reserved-words.md)」および「[Microsoft Jet データベース エンジン SQL と ANSI SQL のデータ型](equivalent-ansi-sql-data-types.md)」を参照してください。Microsoft Office Access Database Engine OLE DB Provider と組み合わせて使うと、追加の予約語を使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa1ef-p102">Microsoft Access SQL and ANSI SQL each have different reserved words and data types. For more information, see [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md) and [Equivalent ANSI SQL Data Types](equivalent-ansi-sql-data-types.md). Using the Microsoft Access Database Engine OLE DB Provider there are additional reserved words.</span></span>

  - <span data-ttu-id="fa1ef-111">**[Between...And](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="fa1ef-111">**[Between…And](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**</span></span>
    
    <span data-ttu-id="fa1ef-112">*式 1*\[いない\]**の間で** *value1* **と** *value2*</span><span class="sxs-lookup"><span data-stu-id="fa1ef-112">*expr1* \[NOT\] **Between** *value1* **And** *value2*</span></span>
    
    <span data-ttu-id="fa1ef-113">Microsoft Access SQL では、引数 *value1* に引数 *value2* より大きい値を指定できますが、ANSI SQL では引数 *value1* は必ず引数 *value2* 以下の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa1ef-113">In Microsoft Access SQL, *value1* can be greater than *value2*; in ANSI SQL, *value1* must be equal to or less than *value2.*</span></span>

  - <span data-ttu-id="fa1ef-p103">Microsoft Office Access SQL では、ANSI SQL の[ワイルドカード文字](using-wildcard-characters-in-string-comparisons.md)と、 **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))** 演算子の指定項目の中で使われる Microsoft Office Access データベース エンジンに固有のワイルドカード文字の両方がサポートされています。ANSI SQL のワイルドカード文字と Microsoft Office Access データベース エンジンに固有のワイルドカード文字は互いに排他的です。このため、これらを同時に使用することはできず、どちらか一方を使用する必要があります。ANSI SQL のワイルドカード文字を使用できるのは、Microsoft Office Access データベース エンジンと Microsoft Office Access Database Engine OLE DB Provider を組み合わせて使う場合だけです。Microsoft Office Access または DAO を介して ANSI SQL のワイルドカード文字を使うと、リテラルとして解釈されます。Microsoft Office Access Database Engine OLE DB Provider を使用しているときは、Microsoft Office Access データベース エンジンのワイルドカード文字がリテラルとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="fa1ef-p103">Microsoft Access SQL supports both ANSI SQL wildcard characters and [wildcard characters](using-wildcard-characters-in-string-comparisons.md) that are specific to the Microsoft Access database engine to use with the **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))** operator. The use of the ANSI and Microsoft Access database engine wildcard characters is mutually exclusive. You must use one set or the other and cannot mix them. The ANSI SQL wildcards are only available when using the Microsoft Access database engine and the Microsoft Access Database Engine OLE DB Provider. If you try to use the ANSI SQL wildcards through Microsoft Access or DAO, then they will be interpreted as literals. The opposite is true when using the Microsoft Access Database Engine OLE DB Provider.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="fa1ef-120">一致する文字</span><span class="sxs-lookup"><span data-stu-id="fa1ef-120">Matching character</span></span></p></th>
    <th><p><span data-ttu-id="fa1ef-121">Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="fa1ef-121">Microsoft Access SQL</span></span></p></th>
    <th><p><span data-ttu-id="fa1ef-122">ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="fa1ef-122">ANSI SQL</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="fa1ef-123">任意の 1 文字</span><span class="sxs-lookup"><span data-stu-id="fa1ef-123">Any single character</span></span></p></td>
    <td><p><span data-ttu-id="fa1ef-124">?</span><span class="sxs-lookup"><span data-stu-id="fa1ef-124"></span></span></p></td>
    <td><p><span data-ttu-id="fa1ef-125">_ (アンダースコア)</span><span class="sxs-lookup"><span data-stu-id="fa1ef-125">_ (underscore)</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="fa1ef-126">0 文字以上の文字列</span><span class="sxs-lookup"><span data-stu-id="fa1ef-126">Zero or more characters</span></span></p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


  - <span data-ttu-id="fa1ef-p104">一般的に、Microsoft Access SQL の方が ANSI SQL よりも制限がありません。たとえば、式のグループ化や並べ替えが可能です。</span><span class="sxs-lookup"><span data-stu-id="fa1ef-p104">Microsoft Access SQL is generally less restrictive. For example, it permits grouping and ordering on expressions.</span></span>

  - <span data-ttu-id="fa1ef-129">Microsoft Access SQL では、ANSI SQL よりも強力な式がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="fa1ef-129">Microsoft Access SQL supports more powerful expressions.</span></span>

## <a name="enhanced-features-of-microsoft-access-sql"></a><span data-ttu-id="fa1ef-130">Microsoft Access SQL の拡張機能</span><span class="sxs-lookup"><span data-stu-id="fa1ef-130">Enhanced Features of Microsoft Access SQL</span></span>

<span data-ttu-id="fa1ef-131">Microsoft Access SQL には、次の拡張機能があります。</span><span class="sxs-lookup"><span data-stu-id="fa1ef-131">Microsoft Access SQL provides the following enhanced features:</span></span>

  - <span data-ttu-id="fa1ef-132">クロス集計クエリをサポートする [TRANSFORM](transform-statement-microsoft-access-sql.md) ステートメント。</span><span class="sxs-lookup"><span data-stu-id="fa1ef-132">The [TRANSFORM](transform-statement-microsoft-access-sql.md) statement, which provides support for crosstab queries.</span></span>

  - <span data-ttu-id="fa1ef-133">[StDev](sql-aggregate-functions-sql.md) や **VarP** などの **集計関数**。</span><span class="sxs-lookup"><span data-stu-id="fa1ef-133">Additional [aggregate functions](sql-aggregate-functions-sql.md), such as **StDev** and **VarP**.</span></span>

  - <span data-ttu-id="fa1ef-134">パラメーター クエリの定義に使用する [PARAMETERS](parameters-declaration-microsoft-access-sql.md) 宣言。</span><span class="sxs-lookup"><span data-stu-id="fa1ef-134">The [PARAMETERS](parameters-declaration-microsoft-access-sql.md) declaration for defining parameter queries.</span></span>

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a><span data-ttu-id="fa1ef-135">Microsoft Access SQL でサポートされていない ANSI SQL の機能</span><span class="sxs-lookup"><span data-stu-id="fa1ef-135">ANSI SQL Features Not Supported in Microsoft Access SQL</span></span>

<span data-ttu-id="fa1ef-136">Microsoft Access SQL では、ANSI SQL の次の機能がサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="fa1ef-136">Microsoft Access SQL does not support the following ANSI SQL features:</span></span>

  - <span data-ttu-id="fa1ef-p105">DISTINCT 集計関数の参照。たとえば、Microsoft Access SQL では、SUM(DISTINCT *columnname*) のような DISTINCT 集計関数の参照がサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="fa1ef-p105">DISTINCT aggregate function references. For example, Microsoft Access SQL does not allow SUM(DISTINCT *columnname*).</span></span>

  - <span data-ttu-id="fa1ef-139">制限する*nn* ROWS 句クエリで返される行の数を制限するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fa1ef-139">The LIMIT TO *nn* ROWS clause used to limit the number of rows returned by a query.</span></span> <span data-ttu-id="fa1ef-140">クエリの適用範囲を制限するために使用できるのは、 [WHERE 句](https://msdn.microsoft.com/library/ff195245\(v=office.15\))のみです。</span><span class="sxs-lookup"><span data-stu-id="fa1ef-140">You can use only the [WHERE clause](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) to limit the scope of a query.</span></span>
