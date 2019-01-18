---
title: Recordset.AbsolutePosition プロパティ (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 22284abf537f57d98d5f0416b58a9a2ac3c6ebe5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702505"
---
# <a name="recordsetabsoluteposition-property-dao"></a>Recordset.AbsolutePosition プロパティ (DAO)

**適用されます**Access 2013、Office 2013。

**Recordset** オブジェクトのカレント レコードの相対的なレコード番号を設定または取得します。

## <a name="syntax"></a>構文

*式*です。AbsolutePosition

*式***レコード セット**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**AbsolutePosition** プロパティを使用すると、ダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクト内における順序位置に基づいて、カレント レコードを参照するポインターを特定のレコードに移動できます。また、 **AbsolutePosition** プロパティの設定値を調べると、カレント レコードのレコード番号を特定できます。

**AbsolutePosition** プロパティの値は 0 から始まるため (つまり、設定値 0 は **Recordset** オブジェクトの最初のレコードを表します)、このプロパティを、格納済みのレコードの数に等しいかまたはそれを超える値に設定できません。このような値に設定すると、トラップ可能なエラーが発生します。 **RecordCount** プロパティの設定値を調べると、 **Recordset** オブジェクトに格納済みのレコードの数を確認できます。 **AbsolutePosition** プロパティに設定できる最大の値は、 **RecordCount** プロパティから 1 を引いた値です。

ない場合、現在のレコードとして**レコード セット**オブジェクトのレコードが存在しない場合、 **AbsolutePosition**は-1 を返します。 カレント レコードを削除した場合、 **AbsolutePosition** プロパティに値が定義されていないため、そのレコードを参照するとトラップ可能なエラーが発生します。 新しいレコードは、レコード順序の末尾に追加されます。

このプロパティをレコード番号の代わりに使用しないでください。ブックマークが、特定の位置を保持してその位置に戻るための推奨手段であり、すべての種類の **Recordset** オブジェクトでカレント レコードの位置を指定する唯一の手段です。特に、レコードの位置は、それより前にある 1 つ以上のレコードを削除すると変わります。また、SQL ステートメントで ORDER BY 句を使用して **Recordset** オブジェクトを作成した場合を除き、そのオブジェクト内の各レコードの順序は保証されないため、 **Recordset** オブジェクトを再作成すると、同じレコードの絶対的な位置が以前と同じになる保証はありません。

> [!NOTE]
> - 新たに開いた後でまだレコードを格納していない **Recordset** オブジェクトの **AbsolutePosition** プロパティを 0 より大きい値に設定すると、トラップ可能なエラーが発生します。**MoveLast** メソッドを使用して、まず **Recordset** オブジェクトに値を設定してください。
> - 前方スクロール タイプの **Recordset** オブジェクト、または Microsoft Access データベース エンジンに接続された ODBC データベースに対して実行したパススルー クエリによって開いた **Recordset** オブジェクトでは、**AbsolutePosition** プロパティを使用できません。

## <a name="example"></a>例

この例では、 **AbsolutePosition** プロパティを使用して、 **Recordset** オブジェクトのすべてのレコードを列挙するループ処理の進捗を追跡します。

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim strMessage As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' AbsolutePosition only works with dynasets or snapshots. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          ' Populate Recordset. 
          .MoveLast 
          .MoveFirst 
     
          ' Enumerate Recordset. 
          Do While Not .EOF 
             ' Display current record information. Add 1 to  
             ' AbsolutePosition value because it is zero-based. 
             strMessage = "Employee: " & !LastName & vbCr & _ 
                "(record " & (.AbsolutePosition + 1) & _ 
                " of " & .RecordCount & ")" 
             If MsgBox(strMessage, vbOKCancel) = vbCancel _ 
                Then Exit Do 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
