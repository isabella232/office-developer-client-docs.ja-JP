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
localization_priority: Normal
ms.openlocfilehash: 94453b5bd8f5a405c5ad5b7c8a175468df2adfa2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726380"
---
# <a name="recordset2cachesize-property-dao"></a>Recordset2.CacheSize プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

ローカル メモリにキャッシュされた ODBC データ ソースから取得したレコード数を設定または取得します。値の取得および設定が可能です。長整数型 ( **Long**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。CacheSize

*式***Recordset2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**CacheSize** プロパティの値は 5 ～ 1200 の範囲内で、利用可能な空きメモリ以下である必要があります。一般的な値は 100 です。0 を設定すると、キャッシングがオフになります。

**Recordset** オブジェクトを使用してリモート サーバーからデータを取得する場合、データをキャッシュするとパフォーマンスが向上します。キャッシュとは、サーバーから最近取得したデータを保持するローカル メモリ内の領域で、アプリケーションの実行中にユーザーが再度同じデータを要求した場合に役に立ちます。ユーザーがデータを要求すると、Microsoft Access データベース エンジンでは、最初にキャッシュ内に要求されたデータがあるかどうかを確認し、より時間のかかるサーバーからの取得はキャッシュにデータがない場合に行われます。キャッシュに保存されるデータは、ODBC データ ソースのデータのみです。

リンク テーブルなどの Microsoft Access データベース エンジンに接続された ODBC データ ソースには、ローカル キャッシュを設定できます。キャッシュを作成するには、リモート データ ソースから **Recordset** オブジェクトを開き、 **CacheSize** プロパティと **[CacheStart](recordset2-cachestart-property-dao.md)** プロパティを設定し、次に、 **[FillCache](recordset2-fillcache-method-dao.md)** メソッドを使用するか、 **Move** メソッドを使用してレコード間を移動します。

**CacheSize** プロパティは、アプリケーションが一度に処理できるレコード数に基づいて設定できます。たとえば、画面に表示するデータ ソースとして **Recordset** オブジェクトを使用している場合、その **CacheSize** プロパティを 20 に設定すると、一度に 20 レコード表示できます。

Microsoft Access データベース エンジンでは、キャッシュ範囲内のレコードはキャッシュに要求し、キャッシュ範囲外のレコードはサーバーに対して要求します。

キャッシュから取得したレコードには、他のユーザーが平行してソース データに加えた変更は反映されていません。

キャッシュしたすべてのデータの更新を強制するには、 **Recordset** オブジェクトの **CacheSize** プロパティを 0 に設定し、次に、最初に要求したキャッシュのサイズにリセットしてから、 **FillCache** メソッドを使用します。

## <a name="example"></a>例

次の使用例では、 **CreateTableDef** メソッドと **FillCache** メソッド、および **CacheSize**、 **CacheStart**、 **SourceTableName** の各プロパティを使用して、リンク テーブルのレコードを 2 回列挙します。次に、50 件のレコードをキャッシュして、すべてのレコードを 2 回列挙します。最後に、リンク テーブルを使用して、キャッシュされていない実行とキャッシュされた実行のパフォーマンス統計を表示します。

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
