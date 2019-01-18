---
title: CommandText プロパティ (ADO)
TOCTitle: CommandText property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 66797accb24cead7d7ba5732f0a9c58ee31049e5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725981"
---
# <a name="commandtext-property-ado"></a>CommandText プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

プロバイダーに対して発行するコマンド文字列を示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

SQL ステートメント、テーブル名、相対 URL、またはストアド プロシージャの呼び出しなど、プロバイダーのコマンドを含む文字列型 ( **String** ) の値を設定または取得します。既定値は "" (長さ 0 の文字列) です。

## <a name="remarks"></a>解説

**Command** オブジェクトで表されるコマンド テキストを設定または取得するには、 [CommandText](command-object-ado.md) プロパティを使用します。通常は SQL ステートメントを使いますが、ストアド プロシージャの呼び出しなど、プロバイダーが認識する、他の種類のコマンド ステートメントでもかまいません。SQL ステートメントは、特定の文法またはプロバイダーのクエリ プロセッサがサポートするバージョンである必要があります。

[Command](prepared-property-ado.md) オブジェクトの **Prepared** プロパティが **True** に設定されていて、 **CommandText** プロパティを設定するときに開いていた接続に **Command** オブジェクトがバインドされている場合、 [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) メソッドまたは **Open** メソッドを呼び出すと、クエリ (つまり、プロバイダーが保存するコンパイルされたクエリ) が準備されます。

[CommandType](commandtype-property-ado.md) プロパティの設定値によっては、 **CommandText** プロパティが変更される場合があります。 **CommandText** プロパティはいつでも読み出すことができ、ADO がコマンド実行中に使う実際のコマンド テキストの参照も可能です。

ファイルやディレクトリなどのリソースを指定する相対 URL を設定したり取得したりするには、 **CommandText** プロパティを使います。リソースは、絶対 URL で明示的に指定された位置や、開かれた [Connection](connection-object-ado.md) オブジェクトで暗黙的に指定された位置に対して相対的です。


> [!NOTE]
> [!メモ] http 体系を使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、[絶対と相対 Url](absolute-and-relative-urls.md)を参照してください。


