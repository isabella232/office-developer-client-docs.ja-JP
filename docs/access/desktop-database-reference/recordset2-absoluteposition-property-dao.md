---
title: Recordset2.AbsolutePosition プロパティ (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: 91ca203f-0c80-67f4-e180-415b6af05030
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197637(v=office.15)
ms:contentKeyID: 48546358
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053074
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4f521daab352e090c52fd7a94bdd28abb0e34291
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478593"
---
# <a name="recordset2absoluteposition-property-dao"></a>Recordset2.AbsolutePosition プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

**Recordset2** オブジェクトのカレント レコードの相対的なレコード番号を設定または取得します。

## <a name="syntax"></a>構文

*式*です。AbsolutePosition

*式***Recordset2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**AbsolutePosition** プロパティを使用すると、ダイナセット タイプまたはスナップショット タイプの **Recordset2** オブジェクト内における順序位置に基づいて、カレント レコードを参照するポインターを特定のレコードに移動できます。また、 **AbsolutePosition** プロパティの設定値を調べると、カレント レコードのレコード番号を特定できます。

**AbsolutePosition** プロパティの値は 0 から始まるため (つまり、設定値 0 は **Recordset2** オブジェクトの最初のレコードを表します)、このプロパティを、格納済みのレコードの数に等しいかまたはそれを超える値に設定できません。このような値に設定すると、トラップ可能なエラーが発生します。 **RecordCount** プロパティの設定値を調べると、 **Recordset2** オブジェクトに格納済みのレコードの数を確認できます。 **AbsolutePosition** プロパティに設定できる最大の値は、 **RecordCount** プロパティから 1 を引いた値です。

ない場合、現在のレコードとして、 **Recordset2**オブジェクトにレコードが存在しない場合、 **AbsolutePosition**は-1 を返します。 カレント レコードを削除した場合、 **AbsolutePosition** プロパティに値が定義されていないため、そのレコードを参照するとトラップ可能なエラーが発生します。 新しいレコードは、レコード順序の末尾に追加されます。

このプロパティをレコード番号の代わりに使用しないでください。ブックマークが、特定の位置を保持してその位置に戻るための推奨手段であり、すべての種類の **Recordset2** オブジェクトでカレント レコードの位置を指定するための唯一の手段です。特に、レコードの位置は、それより前にある 1 つ以上のレコードを削除すると変わります。また、SQL ステートメントで ORDER BY 句を使用して **Recordset** オブジェクトを作成した場合を除き、そのオブジェクト内の各レコードの順序は保証されないため、 **Recordset2** オブジェクトを再作成すると、同じレコードの絶対的な位置が以前と同じになる保証はありません。


> [!NOTE]
> <UL>
> <LI>
> <P>新たに開いた後でまだレコードを格納していない <STRONG>Recordset2</STRONG> オブジェクトの <STRONG>AbsolutePosition</STRONG> プロパティを 0 より大きい値に設定すると、トラップ可能なエラーが発生します。 <STRONG>MoveLast</STRONG> メソッドを使用して、まず <STRONG>Recordset2</STRONG> オブジェクトに値を設定してください。</P>
> <LI>
> <P><STRONG>AbsolutePosition</STRONG>プロパティは、前方スクロール タイプの<STRONG>Recordset2</STRONG>オブジェクト、または Microsoft Access データベース エンジンに接続された ODBC データベースに対するパススルー クエリから開いた<STRONG>Recordset2</STRONG>オブジェクトでは使用できません。</P></LI></UL>



## <a name="example"></a>例

この例では、 **AbsolutePosition** プロパティを使用して、 **Recordset2** オブジェクトのすべてのレコードを列挙するループ処理の進捗を追跡します。

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
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
