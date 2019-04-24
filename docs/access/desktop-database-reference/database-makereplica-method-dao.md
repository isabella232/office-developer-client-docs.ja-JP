---
title: MakeReplica メソッド (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 9b9e2eac360d157f28b986b6598ade58b8c34ec6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294919"
---
# <a name="databasemakereplica-method-dao"></a>MakeReplica メソッド (DAO)

**適用先:** Access 2013、Office 2013

データベースの別のレプリカから新しいレプリカを作成します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*。MakeReplica (***PathName***、 ***Description***、 ***Options***)

*式***Database**オブジェクトを表す変数を取得します。

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
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>PathName</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>新しいレプリカのパスおよびファイル名。 レプリカの名前として既存のファイル名を指定すると、エラーが発生します。</p></td>
</tr>
<tr class="even">
<td><p><em>Description</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>作成するレプリカの説明を表す文字列型 (<strong>String</strong>) の値。</p></td>
</tr>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>作成するレプリカの特性を指定する<strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong>定数。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

新しく作成した部分レプリカの **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** のすべてのプロパティは、テーブルにデータがないことを示す **False** に設定されます。

## <a name="example"></a>例

次の使用例では、**MakeReplica** メソッドを使用して、既存のデザイン マスターの新しいレプリカを作成します。 引数 intOptions には、定数 **dbRepMakeReadOnly** と定数 **dbRepMakePartial** の組み合わせ、または 0 を指定できます。 たとえば、読み取り専用の部分レプリカを作成するには、値**dbRepMakeReadOnly** + **dbRepMakePartial**を intOptions の値として渡す必要があります。

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

