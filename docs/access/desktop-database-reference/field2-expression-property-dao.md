---
title: "\"Field2/式\" プロパティ (DAO)"
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 603dfaa9a54ddfe769b96a57b790b4657abbeb14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292819"
---
# <a name="field2expression-property-dao"></a><span data-ttu-id="42a27-102">"Field2/式" プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="42a27-102">Field2.Expression property (DAO)</span></span>

<span data-ttu-id="42a27-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="42a27-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="42a27-104">集計フィールドの数式を表す式を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="42a27-104">Gets or sets an expression that represents the formula for a calculated field.</span></span> <span data-ttu-id="42a27-105">値の取得と設定が可能な文字列型 (**String**) の値です。</span><span class="sxs-lookup"><span data-stu-id="42a27-105">Read/write **String**.</span></span>

## <a name="version-information"></a><span data-ttu-id="42a27-106">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="42a27-106">Version information</span></span>

<span data-ttu-id="42a27-107">追加されたバージョン: Access 2010</span><span class="sxs-lookup"><span data-stu-id="42a27-107">Version added: Access 2010</span></span>

## <a name="syntax"></a><span data-ttu-id="42a27-108">構文</span><span class="sxs-lookup"><span data-stu-id="42a27-108">Syntax</span></span>

<span data-ttu-id="42a27-109">*式*。表現</span><span class="sxs-lookup"><span data-stu-id="42a27-109">*expression* .Expression</span></span>

<span data-ttu-id="42a27-110">\*式\***Field2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="42a27-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="42a27-111">注釈</span><span class="sxs-lookup"><span data-stu-id="42a27-111">Remarks</span></span>

<span data-ttu-id="42a27-p102">Access 2013 では、値を計算するテーブル フィールドを作成できます。この計算には、同じテーブルのフィールドの値と Access の組み込み関数を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="42a27-p102">In Access 2013, you can create table fields that calculate values. The calculations can include values from fields in the same table as well as built-in Access functions.</span></span>

<span data-ttu-id="42a27-114">計算には他のテーブルまたはクエリのフィールドを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="42a27-114">The calculation cannot include fields from other tables or queries.</span></span>

<span data-ttu-id="42a27-115">計算の結果は値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="42a27-115">The results of the calculation are read-only.</span></span>

## <a name="example"></a><span data-ttu-id="42a27-116">例</span><span class="sxs-lookup"><span data-stu-id="42a27-116">Example</span></span>

<span data-ttu-id="42a27-p103">次の例は、集計フィールドを作成する方法を示します。 CreateField メソッドで、" **FullName**" という名前のフィールドを作成します。次に、 Expression プロパティを、フィールドの値を計算する式に設定します。</span><span class="sxs-lookup"><span data-stu-id="42a27-p103">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="42a27-120">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="42a27-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

