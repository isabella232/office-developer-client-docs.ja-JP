---
title: Provider プロパティ (ADO)
TOCTitle: Provider Property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 890f80534ff47c4dea67b34f345bce0f90328c60
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476184"
---
# <a name="provider-property-ado"></a>Provider プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

[Connection](connection-object-ado.md) オブジェクトのプロバイダー名を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

プロバイダー名を示す文字列型 ( **String** ) の値を設定または取得します。

## <a name="remarks"></a>解説

接続用のプロバイダーの名前を設定または取得するには、**Provider** プロパティを使用します。このプロパティは、[ConnectionString](connectionstring-property-ado.md) プロパティまたは [Open](open-method-ado-connection.md) メソッドの *ConnectionString* 引数の内容によって設定することもできます。ただし、**Open** メソッドを呼び出すときに複数の箇所でプロバイダーを指定すると、予期しない結果が生じる可能性があります。プロバイダーを指定しない場合、このプロパティは既定値の MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)) になります。

**Provider** プロパティは、接続が閉じているときは値の設定および取得が可能で、接続が開いているときは値の取得のみが可能です。設定値は **Connection** オブジェクトを開くか、 [Connection](properties-collection-ado.md) オブジェクトの **Properties** コレクションにアクセスするまで有効になりません。設定が無効である場合は、エラーが発生します。

