---
title: Database.PopulatePartial メソッド (DAO)
TOCTitle: PopulatePartial Method
ms:assetid: fa3227a2-c961-6a98-32b3-5b6e5329a21d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837034(v=office.15)
ms:contentKeyID: 48548834
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101186
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fa52050e91c1a291dd59f9cde1ea36c320406dd6
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860267"
---
# <a name="databasepopulatepartial-method-dao"></a>Database.PopulatePartial メソッド (DAO)


**適用されます**Access 2013 |。Office 2013


部分レプリカ内の変更をフル レプリカと同期させ、部分レプリカ内のすべてのレコードを消去し、現在のレプリカ フィルターに基づいて部分レプリカのデータを再設定します (Microsoft Office Access データベース エンジンのデータベースのみ)。

## <a name="syntax"></a>構文

*式*です。PopulatePartial (***DbPathName***)

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
<td><p>DbPathName</p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p>レコードの設定元となるフル レプリカのパスおよび名前。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

部分レプリカとフル レプリカを同期させると、部分レプリカ内に "孤立化した" レコードが作成されることがあります。 たとえばに、 **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** で、[得意先] テーブルがある場合」領域 = 'CA'"です。 ユーザーが部分レプリカで得意先の地域を CA から NY に変更し、その後、 **[Synchronize](database-synchronize-method-dao.md)** メソッドを使用して同期が行われた場合、この変更がフル レプリカに反映されますが、部分レプリカ内で NY を持つレコードはレプリカのフィルター抽出条件に一致しなくなるため、孤立化します。

孤立化したレコードの問題を解決するには、 **PopulatePartial** メソッドを使用します。 **PopulatePartial** メソッドは **Synchronize** メソッドと似ていますが、すべての変更をフル レプリカと同期させ、部分レプリカ内のすべてのレコードを削除し、現在のレプリカ フィルターに基づいて部分レプリカを再設定します。レプリカ フィルターが変更されていない場合でも、 **PopulatePartial** は必ず部分レプリカ内のすべてのレコードを消去し、現在のフィルターに基づいて部分レプリカを再設定します。

一般に、部分レプリカの作成時、およびレプリカ フィルターを変更したときは **PopulatePartial** メソッドを使用してください。アプリケーションでレプリカ フィルターを変更する場合は、次の手順を実行します。

1.  フル レプリカと、フィルターが変更される部分レプリカを同期させます。

2.  **ReplicaFilter** プロパティおよび **[PartialReplica](relation-partialreplica-property-dao.md)** プロパティを使用して、レプリカ フィルターに必要な変更を行います。

3.  **PopulatePartial** メソッドを呼び出して、部分レプリカのすべてのレコードを削除し、新しいレプリカのフィルター抽出条件に一致するすべてのレコードをフル レプリカから送信します。

レプリカ フィルターが変更された場合、最初に **PopulatePartial** を呼び出さずに **Synchronize** メソッドが呼び出されると、トラップ可能なエラーが発生します。

**PopulatePartial** メソッドは、排他的に開かれている部分レプリカでのみ呼び出すことができます。また、部分レプリカ内で実行しているコードから **PopulatePartial** メソッドを呼び出すことはできません。代わりに、フル レプリカまたは別のデータベースから部分レプリカを排他モードで開き、 **PopulatePartial** を呼び出してください。


> [!NOTE]
> [!メモ] **PopulatePartial** は部分レプリカを消去して再設定する前に単方向の同期を行いますが、 **PopulatePartial** を呼び出す前に **Synchronize** を呼び出すことをお勧めします。 **Synchronize** の呼び出しが失敗した場合は、トラップ可能なエラーが発生するためです。このエラーを使用して、(部分レプリカのすべてのレコードを削除する) **PopulatePartial** メソッドを実行するかどうかを判断できます。 **PopulatePartial** が単独で呼び出された場合、レコードの同期中にエラーが発生したとしても、部分レプリカ内のレコードが削除されますが、これは目的の結果ではないことがあります。



## <a name="example"></a>例

次の使用例では、レプリカ フィルターを変更した後で **PopulatePartial** メソッドを使用します。

```vb 
Sub PopulatePartialX() 
 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 ' Open the partial replica in exclusive mode. 
 Set dbsTemp = OpenDatabase("F:\SALES\FY96CA.MDB", True) 
 
 With dbsTemp 
 Set tdfCustomers = .TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 .Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 
 ' Populate records from the full replica. 
 .PopulatePartial "C:\SALES\FY96.MDB" 
 
 .Close 
 End With 
 
End Sub 
 
```

