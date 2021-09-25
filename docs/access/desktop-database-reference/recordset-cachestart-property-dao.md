---
title: Recordset.CacheStart プロパティ (DAO)
TOCTitle: CacheStart Property
ms:assetid: 03814312-660a-d8e9-8a7b-bc14d66e05ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844802(v=office.15)
ms:contentKeyID: 48542986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053171
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 84ea617bf555b38de79ed36e0209248ef6c2af3b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580917"
---
# <a name="recordsetcachestart-property-dao"></a>Recordset.CacheStart プロパティ (DAO)


**適用先:** Access 2013、Office 2013

ODBC データ ソースからローカルでキャッシュされるデータを含むダイナセット タイプの Recordset オブジェクトの最初のレコードのブックマークを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .CacheStart

*expression*: **Recordset** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**Recordset** オブジェクトを使用してリモート サーバーからデータを取得する場合、データをキャッシュすることでパフォーマンスが向上します。キャッシュは、サーバーから直前に取得されたデータを格納するローカル メモリ内の領域で、ユーザーがアプリケーションの実行中にそのデータを再び要求する場合に便利です。ユーザーがデータを要求すると、Microsoft Access データベース エンジンは、時間がかかるサーバーからのデータ取得ではなく、要求されたデータがキャッシュにあるかどうかをまず確認します。キャッシュに保存されるのは、ODBC データ ソースのデータのみです。

リンク テーブルなど、Microsoft Access データベース エンジンに接続された ODBC データ ソースは、すべてローカル キャッシュを使用できます。キャッシュを作成するには、リモート データ ソースから **Recordset** オブジェクトを開き、 **CacheSize** プロパティと **[CacheStart](recordset-cachestart-property-dao.md)** プロパティを設定した後、 **[FillCache](recordset-fillcache-method-dao.md)** メソッドを使用するか、または **Move** メソッドを使用してレコードを 1 つずつ移動します。

**CacheStart** プロパティの設定値は、キャッシュされる **Recordset** オブジェクトの最初のレコードのブックマークです。任意のレコードのブックマークを使用して、 **CacheStart** プロパティを設定できます。キャッシュを開始するレコードをカレント レコードにして、 **CacheStart** プロパティを **[Bookmark](recordset-bookmark-property-dao.md)** プロパティと同じ値に設定します。

Microsoft Access データベース エンジンは、キャッシュ範囲内のレコードはキャッシュから要求し、キャッシュ範囲外のレコードはサーバーから要求します。

キャッシュから取得したレコードには、他のユーザーが並行してソース データに加えた変更は反映されていません。

キャッシュされたすべてのデータを強制的に更新するには、 **Recordset** オブジェクトの **CacheSize** プロパティを 0 に設定し、最初に要求したキャッシュのサイズに再設定した後、 **FillCache** メソッドを使用します。

