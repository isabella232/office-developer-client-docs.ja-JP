---
title: TableDef.ReplicaFilter プロパティ (DAO)
TOCTitle: ReplicaFilter Property
ms:assetid: f44273de-2b6a-750f-cb7c-12c3ac2da503
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836681(v=office.15)
ms:contentKeyID: 48548683
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055548
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a5cc7394b01dcd79d17e3fcc7568bb8081ee12ce
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872642"
---
# <a name="tabledefreplicafilter-property-dao"></a>TableDef.ReplicaFilter プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

フル レプリカのレコードのどの部分を該当するテーブルにレプリケートするかを示す、部分レプリカ内の **[TableDef](tabledef-object-dao.md)** オブジェクトの値を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。ReplicaFilter

*式***テーブル定義**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

設定値または戻り値は、次の表に示すように、レプリケートするレコードの部分を示す文字列型 ( **String**) またはブール型 ( **Boolean**) の値です。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>文字列</p></td>
<td><p>部分レプリカ テーブル内のレコードをフル レプリカからレプリケートするために、そのレコードが満たす必要がある条件です。</p></td>
</tr>
<tr class="even">
<td><p><strong>True</strong></p></td>
<td><p>すべてのレコードをレプリケートします。</p></td>
</tr>
<tr class="odd">
<td><p><strong>False</strong></p></td>
<td><p>(既定値) レコードをレプリケートしません。</p></td>
</tr>
</tbody>
</table>


このプロパティは、SQL WHERE 句 (キーワード WHERE は省略) に似ていますが、条件にサブクエリ、 **Count** などの集計関数、またはユーザー定義関数を指定することはできません。

フル レプリカと部分レプリカの間でのみ、データを同期することができます。2 つの部分レプリカ間でデータを同期することはできません。また、部分レプリカでは、レプリケートするレコードに制限を設定できますが、レプリケートするフィールドを指定することはできません。

異なるレコードのセットをレプリケートする場合、通常、レプリカ フィルターをリセットします。たとえば、ある営業社員が別の営業社員の地域を一時的に引き継ぐ場合、データベース アプリケーションでは、一時的に両地域のデータをレプリケートしてから、前のフィルターに戻すことができます。この場合、アプリケーションでは、 **ReplicaFilter** プロパティをリセットしてから、部分レプリカを再読み込みします。

アプリケーションでレプリカ フィルターを変更する場合、次の手順に従う必要があります。

1.  **[Synchronize](database-synchronize-method-dao.md)** メソッドを使用して、フル レプリカをフィルター変更中の部分レプリカと同期します。

2.  **ReplicaFilter** プロパティを使用して、レプリカ フィルターに必要な変更を行います。

3.  **[PopulatePartial](database-populatepartial-method-dao.md)** メソッドを使用して、部分レプリカからすべてのレコードを削除し、新規レプリカのフィルター抽出条件に合うすべてのレコードをフル レプリカから転送します。

フィルターを削除するには、 **ReplicaFilter** プロパティを **False** に設定します。すべてのフィルターを削除して、 **PopulatePartial** メソッドを呼び出すと、部分レプリカのレプリケートされたテーブルにレコードが表示されることはありません。


> [!NOTE]
> <P>[!メモ] レプリカ フィルターを変更し、最初に <STRONG>PopulatePartial</STRONG> メソッドを呼び出さずに <STRONG>Synchronize</STRONG> メソッドを呼び出すと、トラップ可能なエラーが発生します。</P>



## <a name="example"></a>例

次の例では、 **ReplicaFilter** プロパティを使用して、カリフォルニア地域の顧客レコードのみレプリケートします。

```vb 
Sub ReplicaFilterX() 
 
 ' This example assumes the current open database 
 ' is the replica. 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 Set dbsTemp = OpenDatabase("Northwind.mdb") 
 Set tdfCustomers = dbsTemp.TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 dbsTemp.Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 dbsTemp.PopulatePartial "C:\SALES\FY96.MDB" 
 
 ' Now remove the replica filter (for example purposes 
 ' only). 
 tdfCustomers.ReplicaFilter = False 
 ' Repopulate the database. 
 dbsTemp.PopulatePartial "C:\SALES\DATA96.MDB" 
 
End Sub 
 
```

