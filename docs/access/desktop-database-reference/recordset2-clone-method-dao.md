---
title: Recordset2.Clone メソッド (DAO)
TOCTitle: Clone Method
ms:assetid: f0d32cb1-03f6-395d-2509-b2139a5fdc68
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836567(v=office.15)
ms:contentKeyID: 48548614
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 666e27b176fb973298c791f7473dbda6fe37c7b0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928832"
---
# <a name="recordset2clone-method-dao"></a><span data-ttu-id="a46b0-102">Recordset2.Clone メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="a46b0-102">Recordset2.Clone method (DAO)</span></span>


<span data-ttu-id="a46b0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a46b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a46b0-104">元の [Recordset2](recordset-object-dao.md) オブジェクトを参照する複製の \*\*\*\*Recordset\*\*\*\* オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="a46b0-104">Creates a duplicate **[Recordset](recordset-object-dao.md)** object that refers to the original **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a46b0-105">構文</span><span class="sxs-lookup"><span data-stu-id="a46b0-105">Syntax</span></span>

<span data-ttu-id="a46b0-106">*式*です。クローン</span><span class="sxs-lookup"><span data-stu-id="a46b0-106">*expression* .Clone</span></span>

<span data-ttu-id="a46b0-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="a46b0-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="return-value"></a><span data-ttu-id="a46b0-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="a46b0-108">Return value</span></span>

<span data-ttu-id="a46b0-109">Recordset</span><span class="sxs-lookup"><span data-stu-id="a46b0-109">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="a46b0-110">注釈</span><span class="sxs-lookup"><span data-stu-id="a46b0-110">Remarks</span></span>

<span data-ttu-id="a46b0-p101">**Clone** メソッドは、複数の複製 **Recordset** オブジェクトを作成するために使用します。各レコードセットには、カレント レコードを個別に設定できます。 **Clone** を使用するだけならば、オブジェクトや基になる構造に含まれるデータは変更されません。 **Clone** メソッドを使用すると、複数の **Recordset2** オブジェクト間で各自のブックマークを交換できるため、ブックマークを共有できます。</span><span class="sxs-lookup"><span data-stu-id="a46b0-p101">Use the **Clone** method to create multiple, duplicate **Recordset** objects. Each recordset can have its own current record. Using **Clone** by itself doesn't change the data in the objects or in their underlying structures. When you use the **Clone** method, you can share bookmarks between two or more **Recordset2** objects because their bookmarks are interchangeable.</span></span>

<span data-ttu-id="a46b0-p102">**Clone** メソッドは、レコードセットでカレント レコードが複数必要となる操作を行う場合に使用できます。この方法は、2 つ目のレコードセットを開くよりも迅速で効率的です。 **Clone** メソッドを使用してレコードセットを作成すると、初期状態ではカレント レコードが設定されていません。レコードセットの複製を使用する前に、特定のレコードをカレント レコードに設定するには、 **[Bookmark](recordset2-bookmark-property-dao.md)** プロパティを設定するか、 **[Move](recordset-movefirst-method-dao.md)** メソッドのうちのいずれか、 **[Find](recordset2-findfirst-method-dao.md)** メソッドのうちのいずれか、または **[Seek](recordset2-seek-method-dao.md)** メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a46b0-p102">You can use the **Clone** method when you want to perform an operation on a recordset that requires multiple current records. This is faster and more efficient than opening a second recordset. When you create a recordset with the **Clone** method, it initially lacks a current record. To make a record current before you use the recordset clone, you must set the **[Bookmark](recordset2-bookmark-property-dao.md)** property or use one of the **[Move](recordset-movefirst-method-dao.md)** methods, one of the **[Find](recordset2-findfirst-method-dao.md)** methods, or the **[Seek](recordset2-seek-method-dao.md)** method.</span></span>

<span data-ttu-id="a46b0-p103">元のオブジェクトまたは複製オブジェクトのどちらかで **[Close](connection-close-method-dao.md)** メソッドを使用しても、もう一方のオブジェクトに影響が及ぶことはありません。たとえば、元のレコードセットで **Close** を使用しても、複製が閉じられることはありません。</span><span class="sxs-lookup"><span data-stu-id="a46b0-p103">Using the **[Close](connection-close-method-dao.md)** method on either the original or duplicate object doesn't affect the other object. For example, using **Close** on the original recordset doesn't close the clone.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="a46b0-121">保留中のトランザクションで複製レコードセットを閉じると、 <STRONG>Rollback</STRONG> 操作が暗黙的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="a46b0-121">Closing a clone recordset within a pending transaction will cause an implicit <STRONG>Rollback</STRONG> operation.</span></span></P>
> <LI>
> <P><span data-ttu-id="a46b0-p104">Microsoft Access ワークスペースでテーブル タイプの <STRONG>Recordset</STRONG> オブジェクトを複製した場合、 <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG> プロパティの設定はレコードセットの新しいコピーに反映されません。このため、 <STRONG>Index</STRONG> プロパティの設定を手動でコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a46b0-p104">When you clone a table-type <STRONG>Recordset</STRONG> object in a Microsoft Access workspace, the <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG> property setting is not cloned on the new copy of the recordset. You must copy the <STRONG>Index</STRONG> property setting manually.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="a46b0-124">例</span><span class="sxs-lookup"><span data-stu-id="a46b0-124">Example</span></span>

<span data-ttu-id="a46b0-125">次の例では、 **Clone** メソッドを使用してレコードセットのコピーを作成し、ユーザーが各コピーのレコード ポインターの位置を個別に設定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a46b0-125">This example uses the **Clone** method to create copies of a recordset and then lets the user position the record pointer of each copy independently.</span></span>

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
