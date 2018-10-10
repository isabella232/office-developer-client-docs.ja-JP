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
ms.openlocfilehash: 410629c3e5ebec47dd8acefd852379ee74568832
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477938"
---
# <a name="indexforeign-property-dao"></a>Index.Foreign プロパティ (DAO)

**適用されます**Access 2013 |。Office 2013

**[Index](index-object-dao.md)** オブジェクトがテーブルの外部キーを表すかどうかを示す値を取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。外部

*式***Index**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

戻り値はブール型 ( **Boolean**) の値で、 **Index** オブジェクトが外部キーを表す場合には **True** が返されます。

外部キーは外部テーブルの 1 つ以上のフィールドで構成され、このキーで主テーブルのすべての行が一意に識別されます。

Microsoft Office Access データベース エンジンは、外部テーブルの **Index** オブジェクトを作成し、参照整合性を適用するためのリレーションシップを作成するときに、 **Foreign** プロパティを設定します。

## <a name="example"></a>例

この例は、 **Foreign** プロパティを使用して、 **TableDef** のどの **Index** オブジェクトが外部キーのインデックスであるかを示す方法を示します。これらのインデックスは、 **Relation** オブジェクトを作成するときに、Microsoft Access データベース エンジンによって作成されます。外部キーのインデックスの既定の名前は、主テーブルの名前に外部キー側のテーブルの名前を付加して作成されます。このプロシージャを実行するには、ForeignOutput 関数が必要です。

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
