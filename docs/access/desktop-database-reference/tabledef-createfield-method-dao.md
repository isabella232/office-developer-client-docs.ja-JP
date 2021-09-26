---
title: TableDef.CreateField メソッド (DAO)
TOCTitle: CreateField Method
ms:assetid: a83d797f-ea42-4a07-dd9e-b254755f0891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821396(v=office.15)
ms:contentKeyID: 48546897
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052971
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 9a4f117592e58c282b83f3456c275c6b081c1419
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601703"
---
# <a name="tabledefcreatefield-method-dao"></a>TableDef.CreateField メソッド (DAO)

**適用先**: Access 2013 | Office 2013

新しい **[Field](field-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .CreateField(_**Name**_, _**Type**_, _**Size**_)

*式* **TableDef** オブジェクトを表す変数。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須かどうか</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>名前</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>新しい <strong>Field</strong> オブジェクトの名前を一意に指定する文字列。有効な <strong>Field</strong> 名の詳細については、<strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティを参照してください。</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>新しい <strong>Field</strong> オブジェクトのデータ型を指定する定数。有効なデータ型については、<strong><a href="field-type-property-dao.md">Type</a></strong> プロパティを参照してください。</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>テキストを格納する <strong>Field</strong> オブジェクトの最大サイズをバイト単位で示す整数型 (Integer) の値。size の有効な値については、<strong><a href="field-size-property-dao.md">Size</a></strong> プロパティを参照してください。この引数は、数値フィールドおよび固定幅フィールドでは無視されます。</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

Field

## <a name="remarks"></a>注釈

**CreateField** メソッドを使用して、新しいフィールドを作成し、そのフィールドの名前、データ型、およびサイズを指定できます。**CreateField** の使用時に省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に、適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。新しいオブジェクトの追加後は、一部のプロパティの設定は変更できません。詳細については、各プロパティのトピックを参照してください。

引数 type および引数 Size は、**TableDef** オブジェクトの **Field** オブジェクトにのみ適用されます。これらの引数は、 **Field** オブジェクトが **Index** オブジェクトまたは **Relation** オブジェクトに関連付けられている場合は無視されます。

Name が示すオブジェクトが既にコレクションのメンバーである場合に **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。

**Fields** コレクションから **Field** オブジェクトを削除するには、コレクションの **[Delete](fields-delete-method-dao.md)** メソッドを使用します。フィールドを参照するインデックスを作成した後は、 **TableDef** オブジェクトの **Fields** コレクションから **Field** オブジェクトを削除できません。

**リンクの提供元:**[UtterAccess](https://www.utteraccess.com) コミュニティ。 UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。

- [DAO を使用して既存のテーブルにハイパーリンク フィールドを追加する](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

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

