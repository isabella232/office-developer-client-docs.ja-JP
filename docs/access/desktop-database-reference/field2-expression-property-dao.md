---
title: Field2.Expression プロパティ (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f3cbb7ca4078fb92ad721d85679dabee9237f85
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478406"
---
# <a name="field2expression-property-dao"></a><span data-ttu-id="79739-102">Field2.Expression プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="79739-102">Field2.Expression Property (DAO)</span></span>

<span data-ttu-id="79739-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="79739-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="79739-p101">演算フィールドの数式を表す式式を取得または設定します。値の取得および設定が可能です。文字列型 ( **String** ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="79739-p101">Gets or sets an expression that represents the formula for a calculated field. Read/write **String**.</span></span>

## <a name="version-information"></a><span data-ttu-id="79739-106">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="79739-106">Version Information</span></span>

<span data-ttu-id="79739-107">追加バージョン: Access 2010</span><span class="sxs-lookup"><span data-stu-id="79739-107">Version Added: Access 2010</span></span>

## <a name="syntax"></a><span data-ttu-id="79739-108">構文</span><span class="sxs-lookup"><span data-stu-id="79739-108">Syntax</span></span>

<span data-ttu-id="79739-109">*式*です。式</span><span class="sxs-lookup"><span data-stu-id="79739-109">*expression* .Expression</span></span>

<span data-ttu-id="79739-110">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="79739-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="79739-111">注釈</span><span class="sxs-lookup"><span data-stu-id="79739-111">Remarks</span></span>

<span data-ttu-id="79739-p102">Access 2013 では、値を計算するテーブル フィールドを作成できます。この計算には、同じテーブルのフィールドの値と Access の組み込み関数を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="79739-p102">In Access 2013, you can create table fields that calculate values. The calculations can include values from fields in the same table as well as built-in Access functions.</span></span>

<span data-ttu-id="79739-114">計算には他のテーブルまたはクエリのフィールドを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="79739-114">The calculation cannot include fields from other tables or queries.</span></span>

<span data-ttu-id="79739-115">計算の結果は値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="79739-115">The results of the calculation are read-only.</span></span>

## <a name="example"></a><span data-ttu-id="79739-116">例</span><span class="sxs-lookup"><span data-stu-id="79739-116">Example</span></span>

<span data-ttu-id="79739-p103">次の例は、集計フィールドを作成する方法を示します。 CreateField メソッドで、" **FullName**" という名前のフィールドを作成します。次に、 Expression プロパティを、フィールドの値を計算する式に設定します。</span><span class="sxs-lookup"><span data-stu-id="79739-p103">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="79739-120">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="79739-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

