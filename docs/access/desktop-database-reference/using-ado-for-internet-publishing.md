---
title: インターネット発行に ADO を使用する
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1e2d939f8583fdfd98ed1ae8e51a5bbfe792e486
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479185"
---
# <a name="using-ado-for-internet-publishing"></a>インターネット発行に ADO を使用する


**適用されます**Access 2013 |。Office 2013



「[OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md)」では、ADO を使用して異種データにアクセスする場合の具体的な例が示されています。一方、このセクションの例は、Internet Publishing Provider を使用する場合に固有の例ですが、示されている原理は、他のデータ プロバイダー (電子メール ストアのプロバイダーなど) で異種データに対して ADO を使用する場合と同じです。

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

