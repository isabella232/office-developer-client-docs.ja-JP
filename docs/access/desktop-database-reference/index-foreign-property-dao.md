---
title: Index.Foreign プロパティ (DAO)
TOCTitle: Foreign Property
ms:assetid: 81272436-a506-4b72-fd28-2d68e76d6d9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196489(v=office.15)
ms:contentKeyID: 48545943
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052974
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 878a59d6c844c7c46cf1a38ee6e4ef165d6fca92
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926410"
---
# <a name="indexforeign-property-dao"></a><span data-ttu-id="768ec-102">Index.Foreign プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="768ec-102">Index.Foreign property (DAO)</span></span>

<span data-ttu-id="768ec-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="768ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="768ec-p101">**[Index](index-object-dao.md)** オブジェクトがテーブルの外部キーを表すかどうかを示す値を取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="768ec-p101">Returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a foreign key in a table (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="768ec-106">構文</span><span class="sxs-lookup"><span data-stu-id="768ec-106">Syntax</span></span>

<span data-ttu-id="768ec-107">*式*です。外部</span><span class="sxs-lookup"><span data-stu-id="768ec-107">*expression* .Foreign</span></span>

<span data-ttu-id="768ec-108">\*式\***Index**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="768ec-108">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="768ec-109">注釈</span><span class="sxs-lookup"><span data-stu-id="768ec-109">Remarks</span></span>

<span data-ttu-id="768ec-110">戻り値はブール型 ( **Boolean**) の値で、 **Index** オブジェクトが外部キーを表す場合には **True** が返されます。</span><span class="sxs-lookup"><span data-stu-id="768ec-110">The return value is a **Boolean** data type that returns **True** if the **Index** object represents a foreign key.</span></span>

<span data-ttu-id="768ec-111">外部キーは外部テーブルの 1 つ以上のフィールドで構成され、このキーで主テーブルのすべての行が一意に識別されます。</span><span class="sxs-lookup"><span data-stu-id="768ec-111">A foreign key consists of one or more fields in a foreign table that uniquely identify all rows in a primary table.</span></span>

<span data-ttu-id="768ec-112">Microsoft Office Access データベース エンジンは、外部テーブルの **Index** オブジェクトを作成し、参照整合性を適用するためのリレーションシップを作成するときに、 **Foreign** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="768ec-112">The Microsoft Access database engine creates an **Index** object for the foreign table and sets the **Foreign** property when you create a relationship that enforces referential integrity.</span></span>

## <a name="example"></a><span data-ttu-id="768ec-113">例</span><span class="sxs-lookup"><span data-stu-id="768ec-113">Example</span></span>

<span data-ttu-id="768ec-p102">この例は、 **Foreign** プロパティを使用して、 **TableDef** のどの **Index** オブジェクトが外部キーのインデックスであるかを示す方法を示します。これらのインデックスは、 **Relation** オブジェクトを作成するときに、Microsoft Access データベース エンジンによって作成されます。外部キーのインデックスの既定の名前は、主テーブルの名前に外部キー側のテーブルの名前を付加して作成されます。このプロシージャを実行するには、ForeignOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="768ec-p102">This example shows how the **Foreign** property can indicate which **Index** objects in a **TableDef** are foreign key indexes. Such indexes are created by the Microsoft Access database engine when a **Relation** is created. The default name for the foreign key indexes is the name of the primary table plus the name of the foreign table. The ForeignOutput function is required for this procedure to run.</span></span>

```vb
    Sub ForeignX() 
     
     Dim dbsNorthwind As Database 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Print report on foreign key indexes from two 
     ' TableDef objects and a QueryDef object. 
     ForeignOutput .TableDefs!Products 
     ForeignOutput .TableDefs!Orders 
     ForeignOutput .TableDefs![Order Details] 
     
     .Close 
     End With 
     
    End Sub 
     
    Function ForeignOutput(tdfTemp As TableDef) 
     
     Dim idxLoop As Index 
     
     With tdfTemp 
     Debug.Print "Indexes in " & .Name & " TableDef" 
     ' Enumerate the Indexes collection of the specified 
     ' TableDef object. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Debug.Print " Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     End With 
     
    End Function
```
