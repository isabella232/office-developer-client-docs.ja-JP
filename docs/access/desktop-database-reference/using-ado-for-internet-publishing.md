---
title: インターネット発行に ADO を使用する
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ae8341151c7bf7d90585794061647ba33a5c4ea7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711981"
---
# <a name="using-ado-for-internet-publishing"></a>Internet Publishing 用の ADO の使用


**適用されます**Access 2013、Office 2013。



「[OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md)」では、ADO を使用して異種データにアクセスする場合の具体的な例が示されています。 このセクションの例は、特定のインターネット パブリッシング プロバイダーを使用してありますが、中には、電子メール ストア プロバイダーなどの異機種混在のデータを他のプロバイダーで ADO を使用する場合、基本的な部分がのようなはずです。

## <a name="urls"></a>URL

接続文字列およびコマンド テキストの代わりに Uniform Resource Locator (URL) を使用して、データ ソースおよびファイルやディレクトリの場所を指定することができます。既存の [Connection](connection-object-ado.md) オブジェクトや **Recordset** オブジェクトだけでなく、 **Record** オブジェクトや **Stream** オブジェクトでも URL を使用できます。

URL の使用の詳細については、「[絶対 URL と相対 URL](absolute-and-relative-urls.md)」を参照してください。

## <a name="record-fields"></a>レコードのフィールド

異種データと同種データの主な違いをデータ、または**レコード**の行ごとに、別の列、または**フィールド**のセットを持つことができます。 同種データの場合は、各行が同じ列のセットを持ちます。 インターネット発行プロバイダーに固有のフィールドの詳細については、[レコードおよびプロバイダー提供のフィールド](records-and-provider-supplied-fields.md)を参照してください。

## <a name="appending-new-fields"></a>新規フィールドの追加

一部の ADO オブジェクトは、 **Record** オブジェクトおよび **Stream** オブジェクトと連携するように拡張されています。

  - [Fields](fields-collection-ado.md) コレクションの [Append](append-method-ado.md) メソッドは、 [Field](field-object-ado.md) オブジェクトを作成してコレクションに追加しますが、 **Field** の値を指定することもできます。

  - [Update](update-method-ado.md) メソッドは、フィールドのコレクションへの追加またはコレクションからの削除を終結します。

  - **Append** メソッドに対するショートカットおよび代替手段として、未定義のフィールドまたは以前に削除されたフィールドに値を代入するだけで、フィールドを作成することができます。

## <a name="see-also"></a>関連項目

- [インターネット公開の例のトピック](internet-publishing-scenario.md)
