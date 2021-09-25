---
title: Recordset.PercentPosition プロパティ (DAO)
TOCTitle: PercentPosition Property
ms:assetid: aebbda44-ed72-7a6c-0cd5-28c8997d4d96
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821751(v=office.15)
ms:contentKeyID: 48547077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b99c1644f5980a541e11ff5b46b0c768c65c207a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617588"
---
# <a name="recordsetpercentposition-property-dao"></a>Recordset.PercentPosition プロパティ (DAO)

**適用先**: Access 2013、Office 2013

**[Recordset](recordset-object-dao.md)** オブジェクト内のレコード数の割合に基づいて、 **Recordset** オブジェクトのカレント レコードのおよその位置を示す値を設定または取得します。

## <a name="syntax"></a>構文

*式* .PercentPosition

*式* **Recordset** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**Recordset** オブジェクト内のカレント レコードのおよその位置を示したり変更したりするには、 **PercentPosition** プロパティを確認または設定します。ベース テーブルから直接開いたダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクトを使用する場合は、 **PercentPosition** プロパティを設定または確認する前に、最後のレコードに移動して **Recordset** オブジェクトに値を設定します。 **Recordset** オブジェクトに値がすべて設定される前に **PercentPosition** プロパティを使用すると、移動量は、 **[RecordCount](recordset-recordcount-property-dao.md)** プロパティの設定値に示されている、アクセス済みのレコード数に対する割合になります。 **[MoveLast](recordset-movelast-method-dao.md)** メソッドを使用すると、最後のレコードに移動できます。

> [!NOTE]
> **PercentPosition プロパティを使用** して、Recordset オブジェクト内の特定のレコードに現在のレコードを移動することはできません。 **[Bookmark プロパティ](recordset-bookmark-property-dao.md)** は、このタスクに適しています。

いったん **PercentPosition** プロパティをある値に設定すると、その値に対応するおよその位置にあるレコードがカレント レコードになり、 **PercentPosition** プロパティはカレント レコードのおよその位置が反映された値に再設定されます。たとえば、 **Recordset** オブジェクトに格納されているレコードが 5 件のみの場合に、その **PercentPosition** プロパティの値を 77 に設定すると、 **PercentPosition** プロパティから取得される値は 77 ではなく 80 になることがあります。

**PercentPosition** プロパティは、リモート データベースに対するパススルー クエリから開いた Forward-only-type **Recordset** オブジェクトまたは **Recordset** オブジェクトを除くすべての種類の **Recordset** オブジェクトに適用されます。

フォームまたはテキスト ボックスのスクロール バーに **PercentPosition** プロパティを使用すると、 **Recordset** オブジェクト内のカレント レコードの位置を示すことができます。

## <a name="example"></a>例

この例では、 **PercentPosition** プロパティを使用して、 **Recordset** オブジェクトの先頭を基準とした、カレント レコードを参照するポインターの位置を示します。

```vb
    Sub PercentPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
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
