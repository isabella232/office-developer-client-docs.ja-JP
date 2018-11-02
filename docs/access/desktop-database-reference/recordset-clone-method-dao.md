---
title: Recordset.Clone メソッド (DAO)
TOCTitle: Clone Method
ms:assetid: 50cbc011-7e72-4dee-488d-96e681618e8e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193824(v=office.15)
ms:contentKeyID: 48544802
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052909
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7bce54b0cf7e589641eff35c3cbed2bd54dbe3d2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923001"
---
# <a name="recordsetclone-method-dao"></a>Recordset.Clone メソッド (DAO)


**適用されます**Access 2013、Office 2013。

元の [Recordset](recordset-object-dao.md) オブジェクトを参照する、複数の ****Recordset**** オブジェクトを作成します。

## <a name="syntax"></a>構文

*式*です。クローン

*式***レコード セット**オブジェクトを表す変数です。

### <a name="return-value"></a>戻り値

Recordset

## <a name="remarks"></a>解説

**Clone** メソッドを使用して、複数の重複した **Recordset** オブジェクトを作成します。各 **Recordset** には、それぞれのカレント レコードを指定できます。 **Clone** メソッドを使用するだけでは、オブジェクトおよびその基になる構造のデータは変更されません。 **Clone** メソッドを使用すると、交換可能なブックマークを使用できるので、複数の **Recordset** オブジェクトでブックマークを共有できます。

複数のカレント レコードを必要とする **Recordset** に操作を実行する場合は、 **Clone** メソッドを使用します。この方法は、2 つ目の **Recordset** を開くより高速で効率的です。 **Clone** メソッドを使用して **Recordset** を作成すると、最初はカレント レコードがありません。 **Recordset** のクローンを使用する前にカレント レコードを指定するには、 **[Bookmark](recordset-bookmark-property-dao.md)** プロパティを設定するか、または **[Move](recordset-movefirst-method-dao.md)** メソッドの 1 つ、 **[Find](recordset-findfirst-method-dao.md)** メソッドの 1 つ、または **[Seek](recordset-seek-method-dao.md)** メソッドを使用する必要があります。

元のオブジェクトまたは複製されたオブジェクトのいずれかに **[Close](connection-close-method-dao.md)** メソッドを使用しても、他方のオブジェクトに影響はありません。たとえば、元の **Recordset** オブジェクトに **Close** メソッドを使用しても、クローンは閉じません。


> [!NOTE]
> <UL>
> <LI>
> <P>保留中のトランザクションで複製レコードセットを閉じると、 <STRONG>Rollback</STRONG> 操作が暗黙的に実行されます。</P>
> <LI>
> <P>Microsoft Access ワークスペースでテーブル タイプの <STRONG>Recordset</STRONG> オブジェクトを複製した場合、 <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG> プロパティの設定はレコードセットの新しいコピーに反映されません。このため、 <STRONG>Index</STRONG> プロパティの設定を手動でコピーする必要があります。</P></LI></UL>



## <a name="example"></a>例

この例では、 **Clone** メソッドを使用して **Recordset** のコピーを作成し、ユーザーが各コピーのレコード ポインターを個別に配置できるようにします。

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset 
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
