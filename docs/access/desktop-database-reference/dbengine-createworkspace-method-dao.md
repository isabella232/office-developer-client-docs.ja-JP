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
ms.localizationpriority: medium
ms.openlocfilehash: 2dbd5c9599ddab70974cc3fd637c6a47999933b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615593"
---
# <a name="dbenginecreateworkspace-method-dao"></a>DBEngine.CreateWorkspace メソッド (DAO)

**適用先**: Access 2013、Office 2013

新しい **[Workspace](workspace-object-dao.md)** オブジェクトを作成します。

## <a name="syntax"></a>構文

*式* .CreateWorkspace(***Name** _, _*_UserName_*_, _*_Password_*_, _*_UseType_**)

*式* **DBEngine** オブジェクトを表す変数です。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須かどうか</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>名前</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>新しい <strong>Workspace</strong> オブジェクトの一意の名前を表す文字列型 (<strong>String</strong>) の値。 有効な <strong><a href="connection-name-property-dao.md">ワークスペース名の詳細については、Name</a></strong> プロパティ <strong>を参照</strong> してください。</p></td>
</tr>
<tr class="even">
<td><p><em>UserName</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>新しい <strong>Workspace</strong> オブジェクトの所有者を表す文字列型 (<strong>String</strong>) の値。詳細については、<strong>UserName</strong> プロパティを参照してください。</p></td>
</tr>
<tr class="odd">
<td><p><em>Password</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>新しい <strong>Workspace</strong> オブジェクトのパスワードが含まれる文字列型 (<strong>String</strong>) の値。パスワードは 20 文字以内にする必要があり、ASCII 文字 0 (null) 以外の任意の文字を使用できます。</p>
<p><strong>注</strong>: 大文字と小文字、数字、記号を組み合わせた強力なパスワードを使用します。 これらの文字を混在させたものになっていないパスワードは強固とはいえません。 たとえば、Y6dh!et5 は安全性の高いパスワードです。 House27 は推測されやすいパスワードです。 強力なパスワードでありながら、書き留めておかなくても覚えておくことができるパスワードを使用してください。</p>
</td>
</tr>
<tr class="even">
<td><p><em>UseType</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong>の値の 1 つ。</p>
<p><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。 Microsoft Access データベース エンジンを使用せずに外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

ワークスペース

## <a name="remarks"></a>注釈

**CreateWorkspace** メソッドを使用して新しい **Workspace** オブジェクトを作成すると、 **Workspace** セッションが開始され、 **Workspace** オブジェクトをアプリケーションで参照できるようになります。

**Workspace** オブジェクトは永続的ではなく、ディスクに保存することはできません。 **Workspace** オブジェクトの作成後はそのオブジェクトのプロパティの設定を変更できませんが、 **Name** プロパティは唯一の例外であり、 **Workspace** オブジェクトを **[Workspaces](workspaces-collection-dao.md)** コレクションに追加する前に変更することができます。

新しい **Workspace** オブジェクトを使用するために、このオブジェクトをコレクションに追加する必要はありません。 **Workspaces** コレクションを通じて参照する場合のみ、新しく作成した **Workspace** オブジェクトをコレクションに追加します。

**Workspaces** コレクションから **Workspace** オブジェクトを削除するには、開いているすべてのデータベースと接続を閉じ **[、Workspace](connection-close-method-dao.md)** オブジェクトの Close メソッドを **使用** します。

## <a name="example"></a>例

この例では、 **CreateWorkspace** メソッドを使用して Microsoft Access ワークスペースを作成します。次に、ワークスペースのプロパティの一覧を表示します。

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

