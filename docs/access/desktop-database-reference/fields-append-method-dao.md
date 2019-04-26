---
title: Fields.Append メソッド (DAO)
TOCTitle: Append Method
ms:assetid: a0e553ba-6a57-09af-3436-4f6ca3cbe561
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820791(v=office.15)
ms:contentKeyID: 48546719
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: ec3cacbe1f1c7ac5d6bda16bdd47891dc58ebfe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292588"
---
# <a name="fieldsappend-method-dao"></a><span data-ttu-id="826c6-102">Fields.Append メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="826c6-102">Fields.Append Method (DAO)</span></span>

<span data-ttu-id="826c6-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="826c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="826c6-104">新しい **[Field](field-object-dao.md)** を **[Fields](fields-collection-dao.md)** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="826c6-104">Adds a new **[Field](field-object-dao.md)** to the **[Fields](fields-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="826c6-105">構文</span><span class="sxs-lookup"><span data-stu-id="826c6-105">Syntax</span></span>

<span data-ttu-id="826c6-106">*expression* .Append(***Object***)</span><span class="sxs-lookup"><span data-stu-id="826c6-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="826c6-107">*expression*: **Fields** オブジェクトを表す変数。</span><span class="sxs-lookup"><span data-stu-id="826c6-107">*expression*  A variable that represents a **Fields** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="826c6-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="826c6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="826c6-109">名前</span><span class="sxs-lookup"><span data-stu-id="826c6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="826c6-110">必須/省略可能</span><span class="sxs-lookup"><span data-stu-id="826c6-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="826c6-111">データ型</span><span class="sxs-lookup"><span data-stu-id="826c6-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="826c6-112">説明</span><span class="sxs-lookup"><span data-stu-id="826c6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="826c6-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="826c6-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="826c6-114">必須</span><span class="sxs-lookup"><span data-stu-id="826c6-114">Required</span></span></p></td>
<td><p><span data-ttu-id="826c6-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="826c6-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="826c6-116">コレクションに追加するフィールドを表すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="826c6-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="826c6-117">注釈</span><span class="sxs-lookup"><span data-stu-id="826c6-117">Remarks</span></span>

<span data-ttu-id="826c6-118">**Append** メソッドを使用して、データベースへの新しいテーブルの追加、テーブルへのフィールドの追加、またはインデックスへのフィールドの追加を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="826c6-118">You can use the **Append** method to add a new table to a database, add a field to a table, and add a field to an index.</span></span>

<span data-ttu-id="826c6-119">追加されたオブジェクトは、ディスクに格納され、**Delete** メソッドを使用して削除するまで持続します。</span><span class="sxs-lookup"><span data-stu-id="826c6-119">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="826c6-120">新しいオブジェクトの追加は直ちに実行されますが、データベース構造の変更によって他のコレクションが影響を受ける場合は、そのコレクションの **Refresh** メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="826c6-120">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="826c6-p101">追加しようとしているオブジェクトが不完全である (たとえば、**Indexes** コレクションに追加する前に **Index** オブジェクトの **Fields** コレクションに **Field** オブジェクトが 1 つも追加されていない) 場合や、1 つ以上の従属オブジェクトのプロパティが正しく設定されていない場合、**Append** メソッドを使用すると、エラーが発生します。たとえば、フィールドの種類が指定されていないのに、**TableDef** オブジェクトの **Fields** コレクションに **Field** オブジェクトを追加しようとすると、**Append** メソッドで実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="826c6-p101">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error. For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="826c6-123">例</span><span class="sxs-lookup"><span data-stu-id="826c6-123">Example</span></span>

<span data-ttu-id="826c6-p102">次の例では、 **Append** メソッドまたは **Delete** メソッドを使用して、 **TableDef** の **Fields** コレクションを変更します。このプロシージャを実行するには、AppendDeleteField プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="826c6-p102">This example uses either the **Append** method or the **Delete** method to modify the **Fields** collection of a **TableDef**. The AppendDeleteField procedure is required for this procedure to run.</span></span>

```vb
    Sub AppendX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Add three new fields. 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "E-mail", dbText, 50 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Http", dbText, 80 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Quota", dbInteger, 5 
     
     Debug.Print "Fields after Append" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show the new fields. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     ' Delete the newly added fields. 
     AppendDeleteField tdfEmployees, "DELETE", "E-mail" 
     AppendDeleteField tdfEmployees, "DELETE", "Http" 
     AppendDeleteField tdfEmployees, "DELETE", "Quota" 
     
     Debug.Print "Fields after Delete" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show that the new 
     ' fields have been deleted. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub AppendDeleteField(tdfTemp As TableDef, _ 
     strCommand As String, strName As String, _ 
     Optional varType, Optional varSize) 
     
     With tdfTemp 
     
     ' Check first to see if the TableDef object is 
     ' updatable. If it isn't, control is passed back to 
     ' the calling procedure. 
     If .Updatable = False Then 
     MsgBox "TableDef not Updatable! " & _ 
     "Unable to complete task." 
     Exit Sub 
     End If 
     
     ' Depending on the passed data, append or delete a 
     ' field to the Fields collection of the specified 
     ' TableDef object. 
     If strCommand = "APPEND" Then 
     .Fields.Append .CreateField(strName, _ 
     varType, varSize) 
     Else 
     If strCommand = "DELETE" Then .Fields.Delete _ 
     strName 
     End If 
     
     End With 
     
    End Sub
```
