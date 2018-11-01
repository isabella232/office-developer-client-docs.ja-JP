---
title: Recordset2.NoMatch プロパティ (DAO)
TOCTitle: NoMatch Property
ms:assetid: 2d7a02ff-a2bf-5f0e-bd71-a6d42c25b13a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192114(v=office.15)
ms:contentKeyID: 48543972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbc35b696f74aa0da64ec24ce38c2f8ad8cfab4d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879093"
---
# <a name="recordset2nomatch-property-dao"></a><span data-ttu-id="3f418-102">Recordset2.NoMatch プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="3f418-102">Recordset2.NoMatch Property (DAO)</span></span>


<span data-ttu-id="3f418-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3f418-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f418-104">**[Seek](recordset2-seek-method-dao.md)** メソッドを使用するかまたは **[Find](recordset2-findfirst-method-dao.md)** メソッドの 1 つを使用して、特定のレコードが見つかったかどうかを示します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="3f418-104">Indicates whether a particular record was found by using the **[Seek](recordset2-seek-method-dao.md)** method or one of the **[Find](recordset2-findfirst-method-dao.md)** methods (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="3f418-105">構文</span><span class="sxs-lookup"><span data-stu-id="3f418-105">Syntax</span></span>

<span data-ttu-id="3f418-106">*式*です。NoMatch</span><span class="sxs-lookup"><span data-stu-id="3f418-106">*expression* .NoMatch</span></span>

<span data-ttu-id="3f418-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="3f418-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f418-108">注釈</span><span class="sxs-lookup"><span data-stu-id="3f418-108">Remarks</span></span>

<span data-ttu-id="3f418-109">**[Recordset](recordset-object-dao.md)** オブジェクトを開くかまたは作成すると、そのオブジェクトの **NoMatch** プロパティは **False** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="3f418-109">When you open or create a **[Recordset](recordset-object-dao.md)** object, its **NoMatch** property is set to **False**.</span></span>

<span data-ttu-id="3f418-p101">レコードを見つける場合、テーブル タイプの **Recordset** オブジェクトに対しては **Seek** メソッドを使用し、ダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクトに対しては **Find** メソッドのいずれか 1 つを使用します。 **NoMatch** プロパティの設定値を調べ、レコードが見つかったかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="3f418-p101">To locate a record, use the **Seek** method on a table-type **Recordset** object or one of the **Find** methods on a dynaset- or snapshot-type **Recordset** object. Check the **NoMatch** property setting to see whether the record was found.</span></span>

<span data-ttu-id="3f418-p102">**Seek** メソッドまたは **Find** メソッドで検出されず、 **NoMatch** プロパティが **True** に設定されると、カレント レコードは無効になります。そのレコードに戻る必要がある場合は、 **Seek** メソッドまたは **Find** メソッドを使用する前に、カレント レコードのブックマークを取得してください。</span><span class="sxs-lookup"><span data-stu-id="3f418-p102">If the **Seek** or **Find** method is unsuccessful and the **NoMatch** property is **True**, the current record will no longer be valid. Be sure to obtain the current record's bookmark before using the **Seek** method or a **Find** method if you'll need to return to that record.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3f418-114">[!メモ] <A href="recordset-movefirst-method-dao.md">Recordset</A> オブジェクトでいずれの <STRONG><STRONG>Move</STRONG></STRONG> メソッドを使用しても、そのオブジェクトの <STRONG>NoMatch</STRONG> プロパティの設定値には反映されません。</span><span class="sxs-lookup"><span data-stu-id="3f418-114">Using any of the <STRONG><A href="recordset-movefirst-method-dao.md">Move</A></STRONG> methods on a <STRONG>Recordset</STRONG> object won't affect its <STRONG>NoMatch</STRONG> property setting.</span></span></P>



## <a name="example"></a><span data-ttu-id="3f418-115">例</span><span class="sxs-lookup"><span data-stu-id="3f418-115">Example</span></span>

<span data-ttu-id="3f418-p103">次の例では、 **NoMatch** プロパティを使用して **Seek** および **FindFirst** が成功したかどうか確認し、成功しなかった場合は適切なフィードバックを表示します。このプロシージャを実行するには、SeekMatch プロシージャと FindMatch プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="3f418-p103">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

```vb
    Sub NoMatchX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim strCountry As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Default is dbOpenTable; required if Index property will 
     ' be used. 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     With rstProducts 
     .Index = "PrimaryKey" 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with Seek method" & vbCr & _ 
     "Product ID: " & !ProductID & vbCr & _ 
     "Product Name: " & !ProductName & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter a product ID." 
     strSeek = InputBox(strMessage) 
     If strSeek = "" Then Exit Do 
     
     ' Call procedure that seeks for a record based on 
     ' the ID number supplied by the user. 
     SeekMatch rstProducts, Val(strSeek) 
     Loop 
     
     .Close 
     End With 
     
     Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
     "SELECT CompanyName, Country FROM Customers " & _ 
     "ORDER BY CompanyName", dbOpenSnapshot) 
     
     With rstCustomers 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with FindFirst method" & _ 
     vbCr & "Customer Name: " & !CompanyName & _ 
     vbCr & "Country: " & !Country & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter country on which to search." 
     strCountry = Trim(InputBox(strMessage)) 
     If strCountry = "" Then Exit Do 
     
     ' Call procedure that finds a record based on 
     ' the country name supplied by the user. 
     FindMatch rstCustomers, _ 
     "Country = '" & strCountry & "'" 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset2, _ 
     intSeek As Integer) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .Seek "=", intSeek 
     
     ' If Seek method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
     strFind As String) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .FindFirst strFind 
     
     ' If Find method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub
```
