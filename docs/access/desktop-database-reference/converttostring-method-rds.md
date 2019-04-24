---
title: converttostring メソッド (RDS)
TOCTitle: ConvertToString method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2c589339eb838f944ce4443c19a787eafb01c3dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295514"
---
# <a name="converttostring-method-rds"></a>converttostring メソッド (RDS)

**適用先:** Access 2013、Office 2013 

[Recordset](recordset-object-ado.md) を、レコードセットのデータを表す MIME 文字列に変換します。

## <a name="syntax"></a>構文

*DataFactory*。converttostring (*Recordset*)

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataFactory* |[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトを表すオブジェクト変数です。|
|*Recordset* |**Recordset** オブジェクトを表すオブジェクト変数。|

## <a name="remarks"></a>注釈

.asp ファイルでは、**ConvertToString** を使用して **Recordset** をサーバーで生成された HTML ページに埋め込み、クライアント コンピューターに転送します。

**ConvertToString** は、最初に **Recordset** を Cursor Service テーブルに読み込み、次に MIME 形式のストリームを生成します。

クライアントでは、リモート データ サービスで MIME 文字列を変換し、完全に機能する **Recordset** に戻すことができます。1 行が 1,024 バイト以下で行数が 400 行未満のデータは、適切に処理されます。BLOB データおよび大きな結果セットを HTTP でストリーム配信する場合は、このメソッドを使用しないでください。文字列はワイヤー圧縮されないため、オンライン向けに最適化されたテーブルグラム形式と比較して、HTTP で大きなデータ セットを転送するにはかなりの時間がかかります。テーブルグラム形式は、リモート データ サービスのネイティブ転送プロトコル形式として定義され、展開されています。

> [!NOTE]
> [!メモ] Active Server Pages を使用して、生成された MIME 文字列をクライアントの HTML ページに埋め込む場合、2.0 より前のバージョンの VBScript では、文字列のサイズが 32K に制限されていることに注意してください。この制限を超えると、エラーが返されます。.asp ファイルで MIME の埋め込みを使用するときは、クエリの適用範囲を比較的小さくするようにしてください。この問題を回避するには、[Microsoft ダウンロード センター](https://www.microsoft.com/download/default.aspx)から最新バージョンの VBScript をダウンロードしてください。


