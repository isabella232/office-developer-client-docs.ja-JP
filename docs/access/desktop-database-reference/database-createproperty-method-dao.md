---
title: Database.CreateProperty メソッド (DAO)
TOCTitle: CreateProperty Method
ms:assetid: f2039be9-5fd8-f673-dfbf-0a71540cdc98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836607(v=office.15)
ms:contentKeyID: 48548638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1444ebaa29b704df82ed036e755b12690105485f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868267"
---
# <a name="databasecreateproperty-method-dao"></a><span data-ttu-id="d146c-102">Database.CreateProperty メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="d146c-102">Database.CreateProperty Method (DAO)</span></span>


<span data-ttu-id="d146c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d146c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d146c-p101">新しいユーザー定義の **[Property](property-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="d146c-p101">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="d146c-106">構文</span><span class="sxs-lookup"><span data-stu-id="d146c-106">Syntax</span></span>

<span data-ttu-id="d146c-107">*式*です。CreateProperty (***名前***、***型***、***値***、 ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="d146c-107">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="d146c-108">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="d146c-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="d146c-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d146c-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d146c-110">名前</span><span class="sxs-lookup"><span data-stu-id="d146c-110">Name</span></span></p></th>
<th><p><span data-ttu-id="d146c-111">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="d146c-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="d146c-112">データ型</span><span class="sxs-lookup"><span data-stu-id="d146c-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="d146c-113">説明</span><span class="sxs-lookup"><span data-stu-id="d146c-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d146c-114">名前</span><span class="sxs-lookup"><span data-stu-id="d146c-114">Name</span></span></p></td>
<td><p><span data-ttu-id="d146c-115">省略可能</span><span class="sxs-lookup"><span data-stu-id="d146c-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="d146c-116"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="d146c-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d146c-p102">新しい <strong>Property</strong> オブジェクトの一意の名前を表す文字列型 ( <strong>String</strong> ) の値。有効な <strong>Property</strong> 名の詳細については、 <strong>Name</strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="d146c-p102">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d146c-119">型</span><span class="sxs-lookup"><span data-stu-id="d146c-119">Type</span></span></p></td>
<td><p><span data-ttu-id="d146c-120">省略可能</span><span class="sxs-lookup"><span data-stu-id="d146c-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="d146c-121"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="d146c-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d146c-p103">新しい <strong>Property</strong> オブジェクトのデータ型を定義する定数。有効なデータ型については、 <strong><a href="field-type-property-dao.md">Type</a></strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="d146c-p103">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d146c-124">値</span><span class="sxs-lookup"><span data-stu-id="d146c-124">Value</span></span></p></td>
<td><p><span data-ttu-id="d146c-125">省略可能</span><span class="sxs-lookup"><span data-stu-id="d146c-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="d146c-126"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="d146c-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d146c-p104">初期プロパティ値を格納しているバリアント型 ( <strong>Variant</strong> ) の値。詳細については、 <strong><a href="field-value-property-dao.md">Value</a></strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="d146c-p104">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d146c-129">DDL</span><span class="sxs-lookup"><span data-stu-id="d146c-129">DDL</span></span></p></td>
<td><p><span data-ttu-id="d146c-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="d146c-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="d146c-131"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="d146c-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d146c-132"><strong>バリアント型</strong>(<strong>ブール型</strong>のサブタイプ)<strong>プロパティ</strong>は、DDL オブジェクトであるかどうかを示す。</span><span class="sxs-lookup"><span data-stu-id="d146c-132">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="d146c-133">既定値は、False です。</span><span class="sxs-lookup"><span data-stu-id="d146c-133">The default is False.</span></span> <span data-ttu-id="d146c-134">DDL が True の場合は、ユーザーが変更または dbSecWriteDef 権限を持たない<strong>プロパティ</strong>オブジェクトを削除できません。</span><span class="sxs-lookup"><span data-stu-id="d146c-134">If DDL is True, users can't change or delete this <strong>Property</strong> object unless they have dbSecWriteDef permission.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d146c-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="d146c-135">Return value</span></span>

<span data-ttu-id="d146c-136">プロパティ</span><span class="sxs-lookup"><span data-stu-id="d146c-136">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="d146c-137">注釈</span><span class="sxs-lookup"><span data-stu-id="d146c-137">Remarks</span></span>

<span data-ttu-id="d146c-138">ユーザー定義の **Property** オブジェクトを作成できるのは、持続的なオブジェクトの **[Properties](properties-collection-dao.md)** コレクション内だけです。</span><span class="sxs-lookup"><span data-stu-id="d146c-138">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="d146c-p106">**CreateProperty** の使用時に省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。オブジェクトの追加後は、一部のプロパティの設定は変更できません。詳細については、 **Name**、 **Type**、および **Value** の各プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d146c-p106">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="d146c-142">名は、既にコレクションのメンバーであるオブジェクトを参照している場合、 **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d146c-142">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="d146c-p107">ユーザー定義の **Property** オブジェクトをコレクションから削除するには、 [Properties](fields-delete-method-dao.md) コレクションの \*\*\*\*Delete\*\*\*\* メソッドを使用します。組み込みのプロパティは削除できません。</span><span class="sxs-lookup"><span data-stu-id="d146c-p107">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection. You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="d146c-145">DDL 引数を省略した場合のデフォルト値は False (DDL 以外)。</span><span class="sxs-lookup"><span data-stu-id="d146c-145">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="d146c-146">対応する DDL プロパティは公開されていないので、DDL から DDL 以外に変更する **Property** オブジェクトを削除し、再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d146c-146">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


## <a name="example"></a><span data-ttu-id="d146c-147">例</span><span class="sxs-lookup"><span data-stu-id="d146c-147">Example</span></span>

<span data-ttu-id="d146c-p109">この例では、ユーザー定義のプロパティに値を設定します。プロパティが存在しない場合は、 **CreateProperty** メソッドを使用して作成してから値を設定します。このプロシージャを実行するには、SetProperty プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="d146c-p109">This example tries to set the value of a user-defined property. If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property. The SetProperty procedure is required for this procedure to run.</span></span>

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
             If prpLoop <> "" Then Debug.Print "  " & _ 
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
