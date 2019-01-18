---
title: Recordset2.Clone メソッド (DAO)
TOCTitle: Clone Method
ms:assetid: f0d32cb1-03f6-395d-2509-b2139a5fdc68
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836567(v=office.15)
ms:contentKeyID: 48548614
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6780a27d573f5ff7ff41060074fb8abb9f8e2b80
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711332"
---
# <a name="recordset2clone-method-dao"></a>Recordset2.Clone メソッド (DAO)

**適用されます**Access 2013、Office 2013。

元の [Recordset2](recordset-object-dao.md) オブジェクトを参照する複製の ****Recordset**** オブジェクトを作成します。

## <a name="syntax"></a>構文

*式*です。クローン

*式***Recordset2**オブジェクトを表す変数です。

## <a name="return-value"></a>戻り値

Recordset

## <a name="remarks"></a>注釈

**Clone** メソッドは、複数の複製 **Recordset** オブジェクトを作成するために使用します。各レコードセットには、カレント レコードを個別に設定できます。 **Clone** を使用するだけならば、オブジェクトや基になる構造に含まれるデータは変更されません。 **Clone** メソッドを使用すると、複数の **Recordset2** オブジェクト間で各自のブックマークを交換できるため、ブックマークを共有できます。

**Clone** メソッドは、レコードセットでカレント レコードが複数必要となる操作を行う場合に使用できます。この方法は、2 つ目のレコードセットを開くよりも迅速で効率的です。 **Clone** メソッドを使用してレコードセットを作成すると、初期状態ではカレント レコードが設定されていません。レコードセットの複製を使用する前に、特定のレコードをカレント レコードに設定するには、 **[Bookmark](recordset2-bookmark-property-dao.md)** プロパティを設定するか、 **[Move](recordset-movefirst-method-dao.md)** メソッドのうちのいずれか、 **[Find](recordset2-findfirst-method-dao.md)** メソッドのうちのいずれか、または **[Seek](recordset2-seek-method-dao.md)** メソッドを使用する必要があります。

元のオブジェクトまたは複製オブジェクトのどちらかで **[Close](connection-close-method-dao.md)** メソッドを使用しても、もう一方のオブジェクトに影響が及ぶことはありません。たとえば、元のレコードセットで **Close** を使用しても、複製が閉じられることはありません。

> [!NOTE]
> - 保留中のトランザクションで複製レコードセットを閉じると、 **Rollback** 操作が暗黙的に実行されます。
> - Microsoft Access ワークスペースでテーブル タイプの **Recordset** オブジェクトを複製した場合、 **[Index](recordset2-index-property-dao.md)** プロパティの設定はレコードセットの新しいコピーに反映されません。このため、 **Index** プロパティの設定を手動でコピーする必要があります。

## <a name="example"></a>例

次の例では、 **Clone** メソッドを使用してレコードセットのコピーを作成し、ユーザーが各コピーのレコード ポインターの位置を個別に設定できるようにします。

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset2 
       Dim intLoop As Integer 
       Dim strMessage As String 
       Dim strFind As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' If the following SQL statement will be used often,  
       ' creating a permanent QueryDef will result in better 
       ' performance. 
       Set arstProducts(1) = dbsNorthwind.OpenRecordset( _ 
          "SELECT ProductName FROM Products " & _ 
          "ORDER BY ProductName", dbOpenSnapshot) 
     
       ' Create two clones of the original Recordset. 
       Set arstProducts(2) = arstProducts(1).Clone 
       Set arstProducts(3) = arstProducts(1).Clone 
     
       Do While True 
     
          ' Loop through the array so that on each pass, the  
          ' user is searching a different copy of the same  
          ' Recordset. 
          For intLoop = 1 To 3 
     
             ' Ask for search string while showing where the 
             ' current record pointer is for each Recordset. 
             strMessage = _ 
                "Recordsets from Products table:" & vbCr & _ 
                "  1 - Original - Record pointer at " & _ 
                arstProducts(1)!ProductName & vbCr & _ 
                "  2 - Clone - Record pointer at " & _ 
                arstProducts(2)!ProductName & vbCr & _ 
                "  3 - Clone - Record pointer at " & _ 
                arstProducts(3)!ProductName & vbCr & _ 
                "Enter search string for #" & intLoop & ":" 
             strFind = Trim(InputBox(strMessage)) 
             If strFind = "" Then Exit Do 
     
             ' Find the search string; if there's no match, jump 
             ' to the last record. 
             With arstProducts(intLoop) 
                .FindFirst "ProductName >= '" & strFind & "'" 
                If .NoMatch Then .MoveLast 
             End With 
     
          Next intLoop 
     
       Loop 
     
       arstProducts(1).Close 
       arstProducts(2).Close 
       arstProducts(3).Close 
       dbsNorthwind.Close 
     
    End Sub
```
