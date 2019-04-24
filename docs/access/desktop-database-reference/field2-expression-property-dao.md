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
# <a name="field2expression-property-dao"></a>"Field2/式" プロパティ (DAO)

**適用先:** Access 2013、Office 2013

集計フィールドの数式を表す式を取得または設定します。 値の取得と設定が可能な文字列型 (**String**) の値です。

## <a name="version-information"></a>バージョン情報

追加されたバージョン: Access 2010

## <a name="syntax"></a>構文

*式*。表現

*式***Field2**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

Access 2013 では、値を計算するテーブル フィールドを作成できます。この計算には、同じテーブルのフィールドの値と Access の組み込み関数を含めることができます。

計算には他のテーブルまたはクエリのフィールドを含めることはできません。

計算の結果は値の取得のみ可能です。

## <a name="example"></a>例

次の例は、集計フィールドを作成する方法を示します。 CreateField メソッドで、" **FullName**" という名前のフィールドを作成します。次に、 Expression プロパティを、フィールドの値を計算する式に設定します。

**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。

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

