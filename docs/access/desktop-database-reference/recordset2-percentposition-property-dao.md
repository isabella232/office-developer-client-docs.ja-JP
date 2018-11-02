---
title: Recordset2.PercentPosition プロパティ (DAO)
TOCTitle: PercentPosition Property
ms:assetid: 830a7d26-6817-233f-ce24-80b572c1c100
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196732(v=office.15)
ms:contentKeyID: 48545996
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052973
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 316dd9e8b430ba0dbb741bc1af81517749d84f77
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921888"
---
# <a name="recordset2percentposition-property-dao"></a>Recordset2.PercentPosition プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

**[Recordset](recordset-object-dao.md)** オブジェクト内のレコード数の割合に基づいて、 **Recordset** オブジェクトのカレント レコードのおよその位置を示す値を設定または取得します。

## <a name="syntax"></a>構文

*式*です。PercentPosition

*式***Recordset2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Recordset** オブジェクト内のカレント レコードのおよその位置を示したり変更したりするには、 **PercentPosition** プロパティを確認または設定します。ベース テーブルから直接開いたダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクトを使用する場合は、 **PercentPosition** プロパティを設定または確認する前に、最後のレコードに移動して **Recordset** オブジェクトに値を設定します。 **Recordset** オブジェクトに値がすべて設定される前に **PercentPosition** プロパティを使用すると、移動量は、 **[RecordCount](recordset2-recordcount-property-dao.md)** プロパティの設定値に示されている、アクセス済みのレコード数に対する割合になります。 **[MoveLast](recordset2-movelast-method-dao.md)** メソッドを使用すると、最後のレコードに移動できます。


> [!NOTE]
> <P>[!メモ] <STRONG>PercentPosition</STRONG> プロパティを使用してカレント レコードを <STRONG>Recordset</STRONG> オブジェクトの特定のレコードに移動する方法は推奨されず、この操作を行うには、 <STRONG><A href="recordset2-bookmark-property-dao.md">Bookmark</A></STRONG> プロパティの使用が適しています。</P>



いったん **PercentPosition** プロパティをある値に設定すると、その値に対応するおよその位置にあるレコードがカレント レコードになり、 **PercentPosition** プロパティはカレント レコードのおよその位置が反映された値に再設定されます。たとえば、 **Recordset** オブジェクトに格納されているレコードが 5 件のみの場合に、その **PercentPosition** プロパティの値を 77 に設定すると、 **PercentPosition** プロパティから取得される値は 77 ではなく 80 になることがあります。

**PercentPosition**プロパティは、前方スクロール タイプの**Recordset**オブジェクト、またはリモート ・ データベースに対してパススルー クエリから**レコード セット**オブジェクトを除いて、**レコード セット**オブジェクトのすべての種類に適用されます。

フォームまたはテキスト ボックスのスクロール バーに **PercentPosition** プロパティを使用すると、 **Recordset** オブジェクト内のカレント レコードの位置を示すことができます。

## <a name="example"></a>例

この例では、 **PercentPosition** プロパティを使用して、 **Recordset** オブジェクトの先頭を基準として、カレント レコードを参照するポインターの位置を示します。

```vb
    Sub PercentPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim strFind As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' PercentPosition only works with dynasets or snapshots. 
     Set rstProducts = dbsNorthwind.OpenRecordset( _ 
     "SELECT ProductName FROM Products " & _ 
     "ORDER BY ProductName", dbOpenSnapshot) 
     
     With rstProducts 
     ' Populate the Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show current record information and ask user 
     ' for input. 
     strMessage = "Product: " & !ProductName & vbCr & _ 
     "The record pointer is " & _ 
     Format(.PercentPosition, "##0.0") & _ 
     "% from the " & vbCr & _ 
     "beginning of the Recordset." & vbCr & _ 
     "Please enter a character search string " & _ 
     "for a product name." 
     strFind = Trim(InputBox(strMessage)) 
     If strFind = "" Then Exit Do 
     
     ' Try to find a record matching the search string. 
     .FindFirst "ProductName >= '" & strFind & "'" 
     If .NoMatch Then .MoveLast 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
