---
title: プロパティ コレクション (DAO)
TOCTitle: Properties Collection
ms:assetid: cd07184a-a261-29c9-542f-bc2eff6f4af6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834455(v=office.15)
ms:contentKeyID: 48547753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05379dee652732bc0839abb056cc15962e3683b0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926942"
---
# <a name="properties-collection-dao"></a><span data-ttu-id="f4aa3-102">プロパティ コレクション (DAO)</span><span class="sxs-lookup"><span data-stu-id="f4aa3-102">Properties collection (DAO)</span></span>


<span data-ttu-id="f4aa3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f4aa3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f4aa3-104">**Properties** コレクションには、オブジェクトの特定のインスタンスのすべての **[Property](property-object-dao.md)** オブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f4aa3-104">A **Properties** collection contains all the **[Property](property-object-dao.md)** objects for a specific instance of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4aa3-105">解説</span><span class="sxs-lookup"><span data-stu-id="f4aa3-105">Remarks</span></span>

<span data-ttu-id="f4aa3-p101">**Connection** オブジェクトと **Error** オブジェクトを除くすべての DAO オブジェクトには、 **Properties** コレクションがあり、特定の組み込み **Property** オブジェクトが含まれます。この **Property** オブジェクトは、通常は単にプロパティと呼ばれ、オブジェクトのそれぞれのインスタンスの特徴を一意に指定します。</span><span class="sxs-lookup"><span data-stu-id="f4aa3-p101">Every DAO object except the **Connection** and **Error** objects contains a **Properties** collection, which has certain built-in **Property** objects. These **Property** objects (which are often just called properties) uniquely characterize that instance of the object.</span></span>

<span data-ttu-id="f4aa3-p102">組み込みプロパティの他に、ユーザー定義のプロパティを独自に作成して追加することもできます。既存のオブジェクトのインスタンスにユーザー定義のプロパティを追加するには、 **CreateProperty** メソッドを使用して内容を定義してから **Append** メソッドを使用してコレクションに追加します。 **Properties** コレクションに追加されていないユーザー定義の **Property** オブジェクトを参照したり、ユーザー定義の **Property** オブジェクトが含まれる **Properties** コレクションに、そのオブジェクトと同じ名前の **Property** オブジェクトを追加したりしようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f4aa3-p102">In addition to the built-in properties, you can also create and add your own user-defined properties. To add a user-defined property to an existing instance of an object, first define its characteristics with the **CreateProperty** method, then add it to the collection with the **Append** method. Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.</span></span>

<span data-ttu-id="f4aa3-111">ユーザー定義のプロパティは **Delete** メソッドを使用して **Properties** コレクションから削除できますが、組み込みプロパティは削除できません。</span><span class="sxs-lookup"><span data-stu-id="f4aa3-111">You can use the **Delete** method to remove user-defined properties from the **Properties** collection, but you can't remove built-in properties.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f4aa3-p103">[!メモ] ユーザー定義の <STRONG>Property</STRONG> オブジェクトは、1 つのオブジェクトの特定のインスタンスにのみ関連付けられます。プロパティは、選択した種類のオブジェクトのすべてのインスタンスに定義されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="f4aa3-p103">A user-defined <STRONG>Property</STRONG> object is associated only with the specific instance of an object. The property isn't defined for all instances of objects of the selected type.</span></span></P>



<span data-ttu-id="f4aa3-114">コレクション内の組み込み **Property** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="f4aa3-114">To refer to a built-in **Property** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="f4aa3-115">オブジェクトです。**プロパティ**(0)</span><span class="sxs-lookup"><span data-stu-id="f4aa3-115">object.**Properties**(0)</span></span>

<span data-ttu-id="f4aa3-116">オブジェクトです。**プロパティ**("name")</span><span class="sxs-lookup"><span data-stu-id="f4aa3-116">object.**Properties**("name")</span></span>

<span data-ttu-id="f4aa3-117">オブジェクトです。**プロパティ**\!\[名\]</span><span class="sxs-lookup"><span data-stu-id="f4aa3-117">object.**Properties**\!\[name\]</span></span>

<span data-ttu-id="f4aa3-118">組み込みプロパティの場合、次の構文を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="f4aa3-118">For a built-in property, you can also use this syntax:</span></span>

<span data-ttu-id="f4aa3-119">object.name</span><span class="sxs-lookup"><span data-stu-id="f4aa3-119">object.name</span></span>


> [!NOTE]
> <P><span data-ttu-id="f4aa3-120">ユーザー定義のプロパティでは、完全なオブジェクトを使用する必要があります。<STRONG>プロパティ</STRONG>("name") の構文です。</span><span class="sxs-lookup"><span data-stu-id="f4aa3-120">For a user-defined property, you must use the full object.<STRONG>Properties</STRONG>("name") syntax.</span></span></P>



<span data-ttu-id="f4aa3-p104">同じ構文を使って、 **Property** オブジェクトの **Value** プロパティを参照することもできます。 **Property** オブジェクト自身、または **Property** オブジェクトの **Value** プロパティのどちらを参照するのかは、参照のコンテキストで決まります。</span><span class="sxs-lookup"><span data-stu-id="f4aa3-p104">With the same syntax forms, you can also refer to the **Value** property of a **Property** object. The context of the reference will determine whether you are referring to the **Property** object itself or the **Value** property of the **Property** object.</span></span>

## <a name="example"></a><span data-ttu-id="f4aa3-123">例</span><span class="sxs-lookup"><span data-stu-id="f4aa3-123">Example</span></span>

<span data-ttu-id="f4aa3-p105">この例では、カレント データベースでユーザー定義のプロパティを作成し、 **Type** プロパティと **Value** プロパティを設定してデータベースの **Properties** コレクションに追加します。次に、データベースのすべてのプロパティを列挙します。</span><span class="sxs-lookup"><span data-stu-id="f4aa3-p105">This example creates a user-defined property for the current database, sets its **Type** and **Value** properties, and appends it to the **Properties** collection of the database. Then the example enumerates all properties in the database.</span></span>

```vb
    Sub PropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpNew As Property 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Create and append user-defined property. 
     Set prpNew = .CreateProperty() 
     prpNew.Name = "UserDefined" 
     prpNew.Type = dbText 
     prpNew.Value = "This is a user-defined property." 
     .Properties.Append prpNew 
     
     ' Enumerate all properties of current database. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     With prpLoop 
     Debug.Print " " & .Name 
     Debug.Print " Type: " & .Type 
     Debug.Print " Value: " & .Value 
     Debug.Print " Inherited: " & _ 
     .Inherited 
     End With 
     Next prpLoop 
     
     ' Delete new property because this is a 
     ' demonstration. 
     .Properties.Delete "UserDefined" 
     End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="f4aa3-p106">この例では、ユーザー定義のプロパティに値を設定します。プロパティが存在しない場合は、 **CreateProperty** メソッドを使用して作成してから値を設定します。このプロシージャを実行するには、SetProperty プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="f4aa3-p106">This example tries to set the value of a user-defined property. If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property. The SetProperty procedure is required for this procedure to run.</span></span>

```vb
    Sub CreatePropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Set the Archive property to True. 
     SetProperty dbsNorthwind, "Archive", True 
     
     With dbsNorthwind 
     Debug.Print "Properties of " & .Name 
     
     ' Enumerate Properties collection of the Northwind 
     ' database. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     
     ' Delete the new property since this is a 
     ' demonstration. 
     .Properties.Delete "Archive" 
     
     .Close 
     End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
     booTemp As Boolean) 
     
     Dim prpNew As Property 
     Dim errLoop As Error 
     
     ' Attempt to set the specified property. 
     On Error GoTo Err_Property 
     dbsTemp.Properties("strName") = booTemp 
     On Error GoTo 0 
     
     Exit Sub 
     
    Err_Property: 
     
     ' Error 3270 means that the property was not found. 
     If DBEngine.Errors(0).Number = 3270 Then 
     ' Create property, set its value, and append it to the 
     ' Properties collection. 
     Set prpNew = dbsTemp.CreateProperty(strName, _ 
     dbBoolean, booTemp) 
     dbsTemp.Properties.Append prpNew 
     Resume Next 
     Else 
     ' If different error has occurred, display message. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & vbCr & _ 
     errLoop.Description 
     Next errLoop 
     End 
     End If 
     
    End Sub
```
