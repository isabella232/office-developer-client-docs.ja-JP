---
title: インターネット発行に ADO を使用する
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3c6ec66f838691398afbff5f4f117bf4b8cff13f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557751"
---
# <a name="using-ado-for-internet-publishing"></a>Internet Publishing 用の ADO の使用


**適用先:** Access 2013、Office 2013



「[OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md)」では、ADO を使用して異種データにアクセスする場合の具体的な例が示されています。 このセクションの例はインターネット発行プロバイダーの使用に固有ですが、他のプロバイダーと ADO を使用して電子メール ストアへのプロバイダーなどの異種データに対して ADO を使用する場合の原則は似ている必要があります。

## <a name="urls"></a>URL

接続文字列およびコマンド テキストの代わりに Uniform Resource Locator (URL) を使用して、データ ソースおよびファイルやディレクトリの場所を指定することができます。既存の [Connection](connection-object-ado.md) オブジェクトや **Recordset** オブジェクトだけでなく、 **Record** オブジェクトや **Stream** オブジェクトでも URL を使用できます。

URL の使用の詳細については、「[絶対 URL と相対 URL](absolute-and-relative-urls.md)」を参照してください。

## <a name="record-fields"></a>レコードのフィールド

The distinguishing difference between heterogeneous data and homogeneous data is that for the former, each row of data, or **Record**, can have a different set of columns, or **Fields**. For homogeneous data, each row has the same set of columns. For more information about the fields specific to the Internet Publishing Provider, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).

## <a name="appending-new-fields"></a>新規フィールドの追加

一部の ADO オブジェクトは、**Record** オブジェクトおよび **Stream** オブジェクトと連携するように拡張されています。

  - [Fields](fields-collection-ado.md) コレクションの [Append](append-method-ado.md) メソッドは、 [Field](field-object-ado.md) オブジェクトを作成してコレクションに追加しますが、 **Field** の値を指定することもできます。

  - [Update](update-method-ado.md) メソッドは、フィールドのコレクションへの追加またはコレクションからの削除を終結します。

  - **Append** メソッドに対するショートカットおよび代替手段として、未定義のフィールドまたは以前に削除されたフィールドに値を代入するだけで、フィールドを作成することができます。

## <a name="see-also"></a>関連項目

- [インターネット発行シナリオのトピック](internet-publishing-scenario.md)
