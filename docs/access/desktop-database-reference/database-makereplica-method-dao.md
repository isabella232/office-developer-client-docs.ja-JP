---
title: Database.MakeReplica メソッド (DAO)
TOCTitle: MakeReplica Method
ms:assetid: b6bf4982-0804-12ce-849f-d2b4ac2e48a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822413(v=office.15)
ms:contentKeyID: 48547286
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053371
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: afdb4fe18c3dc987795092859262aca3054b13cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569182"
---
# <a name="databasemakereplica-method-dao"></a>Database.MakeReplica メソッド (DAO)

**適用先:** Access 2013、Office 2013

データベースの別のレプリカから新しいレプリカを作成します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .MakeReplica(***PathName** _, _*_Description_*_, _*_Options_**)

*式* **Database** オブジェクトを表す変数です。

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
<td><p><em>PathName</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>新しいレプリカのパスおよびファイル名。レプリカの名前として既存のファイル名を指定すると、エラーが発生します。</p></td>
</tr>
<tr class="even">
<td><p><em>Description</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>作成するレプリカの説明を表す文字列型 (<strong>String</strong>) の値。</p></td>
</tr>
<tr class="odd">
<td><p><em>オプション</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>作成するレプリカの特性を指定する <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> クラスの定数です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

新しく作成した部分レプリカの **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** のすべてのプロパティは、テーブルにデータがないことを示す **False** に設定されます。

## <a name="example"></a>例

次の使用例では、**MakeReplica** メソッドを使用して、既存のデザイン マスターの新しいレプリカを作成します。 引数 intOptions には、定数 **dbRepMakeReadOnly** と定数 **dbRepMakePartial** の組み合わせ、または 0 を指定できます。 たとえば、読み取り専用の部分レプリカを作成するには、**値 dbRepMakeReadOnly**  +  **dbRepMakePartial** を intOptions の値として渡す必要があります。

```vb 
Function MakeAdditionalReplica(strReplicableDB As _ 
 String, strNewReplica As String, intOptions As _ 
 Integer) As Integer 
 
 Dim dbsTemp As Database 
 On Error GoTo ErrorHandler 
 
 Set dbsTemp = OpenDatabase(strReplicableDB) 
 
 ' If no options are passed to 
 ' MakeAdditionalReplica, omit the 
 ' options argument, which defaults to 
 ' a full, read/write replica. Otherwise, 
 ' use the value of intOptions. 
 
 If intOptions = 0 Then 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB 
 Else 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB, _ 
 intOptions 
 End If 
 
 dbsTemp.Close 
 
ErrorHandler: 
 Select Case Err 
 Case 0: 
 MakeAdditionalReplica = 0 
 Exit Function 
 Case Else: 
 MsgBox "Error " & Err & " : " & Error 
 MakeAdditionalReplica = Err 
 Exit Function 
 End Select 
 
End Function 
 
```

