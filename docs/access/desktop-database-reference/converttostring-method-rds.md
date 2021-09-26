---
title: ConvertToString メソッド (RDS)
TOCTitle: ConvertToString method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f3115023d8aee71b4576c0f112f403b5c0a7d37a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597563"
---
# <a name="converttostring-method-rds"></a>ConvertToString メソッド (RDS)

**適用先**: Access 2013、Office 2013 

[Recordset](recordset-object-ado.md) を、レコードセットのデータを表す MIME 文字列に変換します。

## <a name="syntax"></a>構文

*DataFactory*.ConvertToString(*Recordset*)

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


