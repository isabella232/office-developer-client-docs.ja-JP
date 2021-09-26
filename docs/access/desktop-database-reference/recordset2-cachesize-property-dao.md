---
title: Recordset2.CacheSize プロパティ (DAO)
TOCTitle: CacheSize Property
ms:assetid: d8d195cc-6696-0583-31eb-b9988f8b7c6f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835090(v=office.15)
ms:contentKeyID: 48548042
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052927
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: a200c9ecab66b40ff6d9ac8fc474734702d5bdf9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611764"
---
# <a name="recordset2cachesize-property-dao"></a>Recordset2.CacheSize プロパティ (DAO)


**適用先**: Access 2013、Office 2013

ローカルにキャッシュされる ODBC データ ソースから取得するレコード数を設定または取得します。値の取得および設定が可能です。長整数型 ( **Long**) の値を使用します。

## <a name="syntax"></a>構文

*式* .CacheSize

*式* Recordset2 オブジェクトを **表す変数** 。

## <a name="remarks"></a>注釈

**CacheSize** プロパティの値の有効範囲は 5 ～ 1200 ですが、使用可能なメモリ容量を超えることはできません。通常の値は 100 です。0 に設定するとキャッシュ機能がオフになります。

**Recordset** オブジェクトを使用してリモート サーバーからデータを取得する場合、データ キャッシュ機能を使用するとパフォーマンスが向上します。キャッシュは、サーバーから最後に取得したデータを保持するローカル メモリ内の領域です。このキャッシュは、アプリケーションを実行しているときに、ユーザーが最後に取得したデータを再度要求する場合に役立ちます。ユーザーがデータを要求すると、Microsoft Access データベース エンジンは、より時間のかかるサーバーからのデータの取得を行う前に、要求されたデータがキャッシュにあるかどうかを調べます。キャッシュには、ODBC データ ソースのデータのみが保存されます。

Microsoft Access データベース エンジンに接続された、リンク テーブルなどの ODBC データ ソースに対してローカル キャッシュを作成できます。キャッシュを作成するには、リモート データ ソースの **Recordset** オブジェクトを開き、 **CacheSize** プロパティと **[CacheStart](recordset2-cachestart-property-dao.md)** プロパティを設定した後、 **[FillCache](recordset2-fillcache-method-dao.md)** メソッドを使用するか、または **Move** メソッドを使用して各レコードを順に取得します。

**CacheSize** プロパティは、アプリケーションで同時に処理できるレコード数に基づいて設定できます。たとえば、画面に表示するときのデータ ソースとして **Recordset** オブジェクトを使用している場合、そのオブジェクトの **CacheSize** プロパティを 20 に設定すると、同時に 20 レコード表示できます。

Microsoft Access データベース エンジンは、キャッシュ領域内にあるレコードはキャッシュから取得するように要求し、キャッシュ領域内に存在しないレコードはサーバーから取得するように要求します。

キャッシュから取得したレコードには、他のユーザーが平行してソース データに加えた変更は反映されていません。

すべてのキャッシュ データを強制的に更新するには、 **Recordset** オブジェクトの **CacheSize** プロパティを 0 に設定し、そのプロパティを当初要求したキャッシュ サイズに再設定した後、 **FillCache** メソッドを使用します。

## <a name="example"></a>例

この例では、**CreateTableDef** メソッドと **FillCache** メソッド、および **CacheSize**、**CacheStart**、**SourceTableName** の各プロパティを使用して、リンクされたテーブルのレコードを 2 回列挙します。その後、50 レコードのキャッシュを使用してレコードを 2 回列挙します。さらに、リンクされたテーブルの処理にキャッシュを使用しなかった場合と使用した場合のパフォーマンスの統計を表示します。

```vb
    Sub ClientServerX3() 
     
     Dim dbsCurrent As Database 
     Dim tdfRoyalties As TableDef 
     Dim rstRemote As Recordset2 
     Dim sngStart As Single 
     Dim sngEnd As Single 
     Dim sngNoCache As Single 
     Dim sngCache As Single 
     Dim intLoop As Integer 
     Dim strTemp As String 
     Dim intRecords As Integer 
     
     ' Open a database to which a linked table can be 
     ' appended. 
     Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
     ' Create a linked table that connects to a Microsoft SQL 
     ' Server database. 
     Set tdfRoyalties = _ 
     dbsCurrent.CreateTableDef("Royalties") 
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     tdfRoyalties.Connect = _ 
     "ODBC;DATABASE=pubs;DSN=Publishers" 
     tdfRoyalties.SourceTableName = "roysched" 
     dbsCurrent.TableDefs.Append tdfRoyalties 
     Set rstRemote = _ 
     dbsCurrent.OpenRecordset("Royalties") 
     
     With rstRemote 
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     sngStart = Timer 
     
     For intLoop = 1 To 2 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     .MoveNext 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngNoCache = sngEnd - sngStart 
     
     ' Cache the first 50 records. 
     .MoveFirst 
     .CacheSize = 50 
     .FillCache 
     sngStart = Timer 
     
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     For intLoop = 1 To 2 
     intRecords = 0 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     ' Count the records. If the end of the 
     ' cache is reached, reset the cache to the 
     ' next 50 records. 
     intRecords = intRecords + 1 
     .MoveNext 
     If intRecords Mod 50 = 0 Then 
     .CacheStart = .Bookmark 
     .FillCache 
     End If 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngCache = sngEnd - sngStart 
     
     ' Display performance results. 
     MsgBox "Caching Performance Results:" & vbCr & _ 
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
