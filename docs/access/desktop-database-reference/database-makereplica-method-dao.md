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
ms.openlocfilehash: 8596548389b066b6ff11e7103090ef50906d79a9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479033"
---
# <a name="databasemakereplica-method-dao"></a>Database.MakeReplica メソッド (DAO)

**適用されます**Access 2013 |。Office 2013

データベースの別のレプリカから新しいレプリカを作成します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。MakeReplica (***パス名***、***説明***、***オプション***)

*式***データベース**オブジェクトを表す変数です。

### <a name="parameters"></a>パラメーター

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
<td><p>パス名</p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p>新しいレプリカのパスおよびファイル名。レプリカの名前として既存のファイル名を指定すると、エラーが発生します。</p></td>
</tr>
<tr class="even">
<td><p>説明</p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p>作成するレプリカの説明を表す文字列型 (<strong>String</strong>) の値。</p></td>
</tr>
<tr class="odd">
<td><p>選択肢</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>作成するレプリカの特性を指定する<strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong>クラスの定数を取得します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

新しく作成した部分レプリカの **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** のすべてのプロパティは、テーブルにデータがないことを示す **False** に設定されます。

## <a name="example"></a>例

次の使用例では、 **MakeReplica** メソッドを使用して、既存のデザイン マスターの新しいレプリカを作成します。 IntOptions 引数は、定数**dbRepMakeReadOnly**と**dbRepMakePartial**の組み合わせ、または 0 であることができます。 たとえば、読み取り専用の部分的なレプリカを作成するにして渡す必要があります値**dbRepMakeReadOnly** + intOptions の値として**dbRepMakePartial** 。

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

