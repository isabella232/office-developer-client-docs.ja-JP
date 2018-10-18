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
ms.openlocfilehash: 5a899f72c6603d81244c31775c1109f66520910e
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602980"
---
# <a name="recordsetclone-method-dao"></a><span data-ttu-id="87a05-102">Recordset.Clone メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="87a05-102">Recordset.Clone Method (DAO)</span></span>


<span data-ttu-id="87a05-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="87a05-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="87a05-104">元の [Recordset](recordset-object-dao.md) オブジェクトを参照する、複数の \*\*\*\*Recordset\*\*\*\* オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="87a05-104">Creates a duplicate **[Recordset](recordset-object-dao.md)** object that refers to the original **Recordset** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="87a05-105">構文</span><span class="sxs-lookup"><span data-stu-id="87a05-105">Syntax</span></span>

<span data-ttu-id="87a05-106">*式*です。クローン</span><span class="sxs-lookup"><span data-stu-id="87a05-106">*expression* .Clone</span></span>

<span data-ttu-id="87a05-107">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="87a05-107">*expression* A variable that represents a **Recordset** object.</span></span>

<span data-ttu-id="87a05-108"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="87a05-108"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="87a05-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="87a05-109">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="87a05-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="87a05-110">Return value</span></span>
>>>>>>> <span data-ttu-id="87a05-111">master</span><span class="sxs-lookup"><span data-stu-id="87a05-111">master</span></span>

<span data-ttu-id="87a05-112">Recordset</span><span class="sxs-lookup"><span data-stu-id="87a05-112">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="87a05-113">解説</span><span class="sxs-lookup"><span data-stu-id="87a05-113">Remarks</span></span>

<span data-ttu-id="87a05-p101">**Clone** メソッドを使用して、複数の重複した **Recordset** オブジェクトを作成します。各 **Recordset** には、それぞれのカレント レコードを指定できます。 **Clone** メソッドを使用するだけでは、オブジェクトおよびその基になる構造のデータは変更されません。 **Clone** メソッドを使用すると、交換可能なブックマークを使用できるので、複数の **Recordset** オブジェクトでブックマークを共有できます。</span><span class="sxs-lookup"><span data-stu-id="87a05-p101">Use the **Clone** method to create multiple, duplicate **Recordset** objects. Each **Recordset** can have its own current record. Using **Clone** by itself doesn't change the data in the objects or in their underlying structures. When you use the **Clone** method, you can share bookmarks between two or more **Recordset** objects because their bookmarks are interchangeable.</span></span>

<span data-ttu-id="87a05-p102">複数のカレント レコードを必要とする **Recordset** に操作を実行する場合は、 **Clone** メソッドを使用します。この方法は、2 つ目の **Recordset** を開くより高速で効率的です。 **Clone** メソッドを使用して **Recordset** を作成すると、最初はカレント レコードがありません。 **Recordset** のクローンを使用する前にカレント レコードを指定するには、 **[Bookmark](recordset-bookmark-property-dao.md)** プロパティを設定するか、または **[Move](recordset-movefirst-method-dao.md)** メソッドの 1 つ、 **[Find](recordset-findfirst-method-dao.md)** メソッドの 1 つ、または **[Seek](recordset-seek-method-dao.md)** メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87a05-p102">You can use the **Clone** method when you want to perform an operation on a **Recordset** that requires multiple current records. This is faster and more efficient than opening a second **Recordset**. When you create a **Recordset** with the **Clone** method, it initially lacks a current record. To make a record current before you use the **Recordset** clone, you must set the **[Bookmark](recordset-bookmark-property-dao.md)** property or use one of the **[Move](recordset-movefirst-method-dao.md)** methods, one of the **[Find](recordset-findfirst-method-dao.md)** methods, or the **[Seek](recordset-seek-method-dao.md)** method.</span></span>

<span data-ttu-id="87a05-p103">元のオブジェクトまたは複製されたオブジェクトのいずれかに **[Close](connection-close-method-dao.md)** メソッドを使用しても、他方のオブジェクトに影響はありません。たとえば、元の **Recordset** オブジェクトに **Close** メソッドを使用しても、クローンは閉じません。</span><span class="sxs-lookup"><span data-stu-id="87a05-p103">Using the **[Close](connection-close-method-dao.md)** method on either the original or duplicate object doesn't affect the other object. For example, using **Close** on the original **Recordset** doesn't close the clone.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="87a05-124">保留中のトランザクションで複製レコードセットを閉じると、 <STRONG>Rollback</STRONG> 操作が暗黙的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="87a05-124">Closing a clone recordset within a pending transaction will cause an implicit <STRONG>Rollback</STRONG> operation.</span></span></P>
> <LI>
> <P><span data-ttu-id="87a05-p104">Microsoft Access ワークスペースでテーブル タイプの <STRONG>Recordset</STRONG> オブジェクトを複製した場合、 <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG> プロパティの設定はレコードセットの新しいコピーに反映されません。このため、 <STRONG>Index</STRONG> プロパティの設定を手動でコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="87a05-p104">When you clone a table-type <STRONG>Recordset</STRONG> object in a Microsoft Access workspace, the <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG> property setting is not cloned on the new copy of the recordset. You must copy the <STRONG>Index</STRONG> property setting manually.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="87a05-127">例</span><span class="sxs-lookup"><span data-stu-id="87a05-127">Example</span></span>

<span data-ttu-id="87a05-128">この例では、 **Clone** メソッドを使用して **Recordset** のコピーを作成し、ユーザーが各コピーのレコード ポインターを個別に配置できるようにします。</span><span class="sxs-lookup"><span data-stu-id="87a05-128">This example uses the **Clone** method to create copies of a **Recordset** and then lets the user position the record pointer of each copy independently.</span></span>

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
