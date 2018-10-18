---
title: DBEngine.CreateWorkspace メソッド (DAO)
TOCTitle: CreateWorkspace Method
ms:assetid: a7d73771-9420-0448-99e6-d6c4aa78683a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821374(v=office.15)
ms:contentKeyID: 48546888
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052966
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2464426bc7178638e8ebbfc9f5b2f6d1d1b61ca2
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602588"
---
# <a name="dbenginecreateworkspace-method-dao"></a><span data-ttu-id="6095f-102">DBEngine.CreateWorkspace メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="6095f-102">DBEngine.CreateWorkspace Method (DAO)</span></span>


<span data-ttu-id="6095f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6095f-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="6095f-104">新しい **[Workspace](workspace-object-dao.md)** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="6095f-104">Creates a new **[Workspace](workspace-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6095f-105">構文</span><span class="sxs-lookup"><span data-stu-id="6095f-105">Syntax</span></span>

<span data-ttu-id="6095f-106">*式*です。CreateWorkspace (***名前***、***ユーザー名***、***パスワード***、 ***UseType***)</span><span class="sxs-lookup"><span data-stu-id="6095f-106">*expression* .CreateWorkspace(***Name***, ***UserName***, ***Password***, ***UseType***)</span></span>

<span data-ttu-id="6095f-107">\*式\***DBEngine**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="6095f-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="6095f-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6095f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6095f-109">名前</span><span class="sxs-lookup"><span data-stu-id="6095f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6095f-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="6095f-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="6095f-111">データ型</span><span class="sxs-lookup"><span data-stu-id="6095f-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="6095f-112">説明</span><span class="sxs-lookup"><span data-stu-id="6095f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6095f-113">名前</span><span class="sxs-lookup"><span data-stu-id="6095f-113">Name</span></span></p></td>
<td><p><span data-ttu-id="6095f-114">必須</span><span class="sxs-lookup"><span data-stu-id="6095f-114">Required</span></span></p></td>
<td><p><span data-ttu-id="6095f-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="6095f-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6095f-p101">新しい <strong>Workspace</strong> オブジェクトの一意の名前を表す文字列型 (<strong>String</strong>) の値。有効な <strong>Workspace</strong> 名の詳細については、<strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6095f-p101">A <strong>String</strong> that uniquely names the new <strong>Workspace</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Workspace</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6095f-118">UserName</span><span class="sxs-lookup"><span data-stu-id="6095f-118">UserName</span></span></p></td>
<td><p><span data-ttu-id="6095f-119">必須</span><span class="sxs-lookup"><span data-stu-id="6095f-119">Required</span></span></p></td>
<td><p><span data-ttu-id="6095f-120"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="6095f-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6095f-p102">新しい <strong>Workspace</strong> オブジェクトの所有者を表す文字列型 (<strong>String</strong>) の値。詳細については、<strong>UserName</strong> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6095f-p102">A <strong>String</strong> that identifies the owner of the new <strong>Workspace</strong> object. See the <strong>UserName</strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6095f-123">Password</span><span class="sxs-lookup"><span data-stu-id="6095f-123">Password</span></span></p></td>
<td><p><span data-ttu-id="6095f-124">必須</span><span class="sxs-lookup"><span data-stu-id="6095f-124">Required</span></span></p></td>
<td><p><span data-ttu-id="6095f-125"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="6095f-125"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6095f-p103">新しい <strong>Workspace</strong> オブジェクトのパスワードが含まれる文字列型 (<strong>String</strong>) の値。パスワードは 20 文字以内にする必要があり、ASCII 文字 0 (null) 以外の任意の文字を使用できます。</span><span class="sxs-lookup"><span data-stu-id="6095f-p103">A <strong>String</strong> containing the password for the new <strong>Workspace</strong> object. The password can be up to 20 characters long and can include any characters except ASCII character 0 (null).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="6095f-p104">[!メモ] パスワードには、大文字、小文字、数字、記号を組み合わせた複雑なものを使用してください。これらの文字を混在させたものになっていないパスワードは強固とはいえません。たとえば、Y6dh!et5 は安全性の高いパスワードです。House27 は推測されやすいパスワードです。また、高い安全性を保ちながらも、書き留めておかなくても覚えておくことができるパスワードを使用してください。</span><span class="sxs-lookup"><span data-stu-id="6095f-p104">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6095f-133">UseType</span><span class="sxs-lookup"><span data-stu-id="6095f-133">UseType</span></span></p></td>
<td><p><span data-ttu-id="6095f-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="6095f-134">Optional</span></span></p></td>
<td><p><span data-ttu-id="6095f-135"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="6095f-135"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6095f-136"><strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> 値の 1 つ。</span><span class="sxs-lookup"><span data-stu-id="6095f-136">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="6095f-137">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6095f-137">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="6095f-138">型引数を<STRONG>dbUseODBC</STRONG>に設定は、実行時エラーになります。</span><span class="sxs-lookup"><span data-stu-id="6095f-138">Setting the type argument to <STRONG>dbUseODBC</STRONG> will result in a run-time error.</span></span> <span data-ttu-id="6095f-139">Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="6095f-139">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


</td>
</tr>
</tbody>
</table>


<span data-ttu-id="6095f-140"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="6095f-140"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="6095f-141">戻り値</span><span class="sxs-lookup"><span data-stu-id="6095f-141">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="6095f-142">戻り値</span><span class="sxs-lookup"><span data-stu-id="6095f-142">Return value</span></span>
>>>>>>> <span data-ttu-id="6095f-143">master</span><span class="sxs-lookup"><span data-stu-id="6095f-143">master</span></span>

<span data-ttu-id="6095f-144">Workspace</span><span class="sxs-lookup"><span data-stu-id="6095f-144">Workspace</span></span>

## <a name="remarks"></a><span data-ttu-id="6095f-145">注釈</span><span class="sxs-lookup"><span data-stu-id="6095f-145">Remarks</span></span>

<span data-ttu-id="6095f-146">**CreateWorkspace** メソッドを使用して新しい **Workspace** オブジェクトを作成すると、 **Workspace** セッションが開始され、 **Workspace** オブジェクトをアプリケーションで参照できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6095f-146">Once you use the **CreateWorkspace** method to create a new **Workspace** object, a **Workspace** session is started, and you can refer to the **Workspace** object in your application.</span></span>

<span data-ttu-id="6095f-p106">**Workspace** オブジェクトは永続的ではなく、ディスクに保存することはできません。 **Workspace** オブジェクトの作成後はそのオブジェクトのプロパティの設定を変更できませんが、 **Name** プロパティは唯一の例外であり、 **Workspace** オブジェクトを **[Workspaces](workspaces-collection-dao.md)** コレクションに追加する前に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="6095f-p106">**Workspace** objects aren't permanent, and you can't save them to disk. Once you create a **Workspace** object, you can't alter any of its property settings, except for the **Name** property, which you can modify before appending the **Workspace** object to the **[Workspaces](workspaces-collection-dao.md)** collection.</span></span>

<span data-ttu-id="6095f-p107">新しい **Workspace** オブジェクトを使用するために、このオブジェクトをコレクションに追加する必要はありません。 **Workspaces** コレクションを通じて参照する場合のみ、新しく作成した **Workspace** オブジェクトをコレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="6095f-p107">You don't have to append the new **Workspace** object to a collection before you can use it. You append a newly created **Workspace** object only if you need to refer to it through the **Workspaces** collection.</span></span>

<span data-ttu-id="6095f-151">**Workspaces** コレクションから **Workspace** オブジェクトを削除するには、開いているすべてのデータベースおよび接続を閉じてから、 [Workspace](connection-close-method-dao.md) オブジェクトの \*\*\*\*Close\*\*\*\* メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6095f-151">To remove a **Workspace** object from the **Workspaces** collection, close all open databases and connections and then use the **[Close](connection-close-method-dao.md)** method on the **Workspace** object.</span></span>

## <a name="example"></a><span data-ttu-id="6095f-152">例</span><span class="sxs-lookup"><span data-stu-id="6095f-152">Example</span></span>

<span data-ttu-id="6095f-p108">この例では、 **CreateWorkspace** メソッドを使用して Microsoft Access ワークスペースを作成します。次に、ワークスペースのプロパティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="6095f-p108">This example uses the **CreateWorkspace** method to createMicrosoft Access workspace. It then lists the properties of the workspace.</span></span>

```vb 
Sub CreateWorkspaceX() 
 
   Dim wrkAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
   DefaultType = dbUseJet 
   ' Create an unnamed Workspace object of the type  
   ' specified by the DefaultType property of DBEngine  
   ' (dbUseJet). 
   Set wrkAcc = CreateWorkspace("", "admin", "") 
 
   ' Enumerate Workspaces collection. 
   Debug.Print "Workspace objects in Workspaces collection:" 
   For Each wrkLoop In Workspaces 
      Debug.Print "  " & wrkLoop.Name 
   Next wrkLoop 
 
   With wrkAcc 
      ' Enumerate Properties collection of Microsoft Access  
      ' workspace. 
      Debug.Print _ 
         "Properties of unnamed Microsoft Access workspace" 
      On Error Resume Next 
      For Each prpLoop In .Properties 
         Debug.Print "  " & prpLoop.Name & " = " & prpLoop 
      Next prpLoop 
      On Error GoTo 0 
   End With 
 
   wrkAcc.Close 
 
End Sub 
 
```

