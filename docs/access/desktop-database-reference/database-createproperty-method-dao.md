---
title: CreateProperty メソッド (DAO)
TOCTitle: CreateProperty Method
ms:assetid: f2039be9-5fd8-f673-dfbf-0a71540cdc98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836607(v=office.15)
ms:contentKeyID: 48548638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f966e041a6d2aff773f6c3849c0846ef362d1142
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294975"
---
# <a name="databasecreateproperty-method-dao"></a><span data-ttu-id="177f5-102">CreateProperty メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="177f5-102">Database.CreateProperty method (DAO)</span></span>

<span data-ttu-id="177f5-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="177f5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="177f5-104">新しいユーザー定義の **[Property](property-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="177f5-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="177f5-105">.</span><span class="sxs-lookup"><span data-stu-id="177f5-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="177f5-106">構文</span><span class="sxs-lookup"><span data-stu-id="177f5-106">Syntax</span></span>

<span data-ttu-id="177f5-107">*式*。CreateProperty (***Name***、 ***Type***、 ***Value***、 ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="177f5-107">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="177f5-108">\*式\***Database**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="177f5-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="177f5-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="177f5-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="177f5-110">名前</span><span class="sxs-lookup"><span data-stu-id="177f5-110">Name</span></span></p></th>
<th><p><span data-ttu-id="177f5-111">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="177f5-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="177f5-112">データ型</span><span class="sxs-lookup"><span data-stu-id="177f5-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="177f5-113">説明</span><span class="sxs-lookup"><span data-stu-id="177f5-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="177f5-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="177f5-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="177f5-115">Optional</span><span class="sxs-lookup"><span data-stu-id="177f5-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="177f5-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="177f5-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="177f5-p102">新しい <strong>Property</strong> オブジェクトの一意の名前を表す文字列型 ( <strong>String</strong> ) の値。有効な <strong>Property</strong> 名の詳細については、 <strong>Name</strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="177f5-p102">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="177f5-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="177f5-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="177f5-120">省略可能</span><span class="sxs-lookup"><span data-stu-id="177f5-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="177f5-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="177f5-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="177f5-p103">新しい <strong>Property</strong> オブジェクトのデータ型を定義する定数。有効なデータ型については、 <strong><a href="field-type-property-dao.md">Type</a></strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="177f5-p103">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="177f5-124"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="177f5-124"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="177f5-125">Optional</span><span class="sxs-lookup"><span data-stu-id="177f5-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="177f5-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="177f5-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="177f5-p104">初期プロパティ値を格納しているバリアント型 ( <strong>Variant</strong> ) の値。詳細については、 <strong><a href="field-value-property-dao.md">Value</a></strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="177f5-p104">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="177f5-129"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="177f5-129"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="177f5-130">Optional</span><span class="sxs-lookup"><span data-stu-id="177f5-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="177f5-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="177f5-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="177f5-132"><strong>Property</strong> が DDL オブジェクトであるかどうかを示す、サブタイプがブール型 (<strong>Boolean</strong>) であるバリアント型 (<strong>Variant</strong>) の値。</span><span class="sxs-lookup"><span data-stu-id="177f5-132">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="177f5-133">既定は False です。</span><span class="sxs-lookup"><span data-stu-id="177f5-133">The default is False.</span></span> <span data-ttu-id="177f5-134">DDL が True の場合、ユーザーは、dbsecwritedef 権限を持っていない限り、この<strong>プロパティ</strong>オブジェクトを変更または削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="177f5-134">If DDL is True, users can't change or delete this <strong>Property</strong> object unless they have dbSecWriteDef permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="177f5-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="177f5-135">Return value</span></span>

<span data-ttu-id="177f5-136">プロパティ</span><span class="sxs-lookup"><span data-stu-id="177f5-136">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="177f5-137">注釈</span><span class="sxs-lookup"><span data-stu-id="177f5-137">Remarks</span></span>

<span data-ttu-id="177f5-138">ユーザー定義の **Property** オブジェクトを作成できるのは、持続的なオブジェクトの **[Properties](properties-collection-dao.md)** コレクション内だけです。</span><span class="sxs-lookup"><span data-stu-id="177f5-138">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="177f5-p106">**CreateProperty** を使用するときに 1 つ以上の省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に、適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。オブジェクトをコレクションに追加した後は、一部のプロパティ設定を変更できなくなります。詳細については、 **Name**、 **Type**、および **Value** の各プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="177f5-p106">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="177f5-142">name が既にコレクションのメンバーであるオブジェクトを参照している場合、 **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="177f5-142">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="177f5-143">ユーザー定義の **Property** オブジェクトをコレクションから削除するには、 **[Properties](fields-delete-method-dao.md)** コレクションの **Delete** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="177f5-143">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection.</span></span> <span data-ttu-id="177f5-144">組み込みのプロパティは削除できません。</span><span class="sxs-lookup"><span data-stu-id="177f5-144">You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="177f5-145">ddl 引数を省略すると、既定では False (非 DDL) になります。</span><span class="sxs-lookup"><span data-stu-id="177f5-145">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="177f5-146">対応する DDL プロパティは公開されていないので、DDL から DDL 以外に変更する **Property** オブジェクトを削除し、再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="177f5-146">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


## <a name="example"></a><span data-ttu-id="177f5-147">例</span><span class="sxs-lookup"><span data-stu-id="177f5-147">Example</span></span>

<span data-ttu-id="177f5-p109">この例では、ユーザー定義のプロパティに値を設定します。プロパティが存在しない場合は、 **CreateProperty** メソッドを使用して作成してから値を設定します。このプロシージャを実行するには、SetProperty プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="177f5-p109">This example tries to set the value of a user-defined property. If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property. The SetProperty procedure is required for this procedure to run.</span></span>

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
