---
title: Error オブジェクト-ActiveX データオブジェクト (ADO)
TOCTitle: Error object (ADO)
ms:assetid: 97e478bf-8b25-03a8-9358-abba5069cba3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249678(v=office.15)
ms:contentKeyID: 48546477
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a7c77a59368851f43b5e7bf2275f9f282546fb4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293484"
---
# <a name="error-object-ado"></a>Error オブジェクト (ADO)


**適用先:** Access 2013、Office 2013

プロバイダーを含む単一の操作に関連して発生した、データ アクセス エラーの詳細情報を格納しています。

## <a name="remarks"></a>注釈

ADO オブジェクトに関係するすべての操作では、1 つ以上のプロバイダー エラーが発生する場合があります。エラーが発生するたびに、1 つ以上の **Error** オブジェクトが [Connection](errors-collection-ado.md) オブジェクトの [Errors](connection-object-ado.md) コレクションに追加されます。別の ADO 操作でエラーが発生すると、 **Errors** コレクションがクリアされ、 **Error** オブジェクトの新しいセットが **Errors** コレクションに配置されます。

> [!NOTE]
> [!メモ] 各 **Error** オブジェクトは、ADO エラーではなく特定のプロバイダー エラーを表します。ADO エラーは、実行時の例外処理メカニズムに公開されます。たとえば、Microsoft Visual Basic の場合、ADO 固有のエラーが発生すると、 **On Error** イベントが実行され、そのエラーが **Error** オブジェクトに追加されます。ADO エラーをすべて記載した一覧については、 [ErrorValueEnum](errorvalueenum.md) のトピックを参照してください。

各エラーの詳細については、次のプロパティを含む **Error** オブジェクトのプロパティを参照してください。

- エラーのテキストを格納する、[Description](description-property-ado.md) プロパティ。これは既定のプロパティです。

- エラー定数の長整数型 ( [Long](number-property-ado.md) ) の値を格納する、 **Number** プロパティ。

- エラーの発生源となったオブジェクトを特定する、[Source](source-property-ado-error.md) プロパティ。特にデータ ソースに対する要求に続いて、 **Errors** コレクションに複数の **Error** オブジェクトが追加された場合に便利です。

- SQL データ ソースの情報を提供する、[SQLState](sqlstate-property-ado.md) プロパティと [NativeError](nativeerror-property-ado.md) プロパティ。

プロバイダー エラーは発生すると、 **Connection** オブジェクトの **Errors** コレクションに追加されます。ADO では 1 回の ADO 操作で複数のエラーを取得できるため、プロバイダー固有のエラー情報を見込んでおくことができます。エラー ハンドラーにあるこうした豊富なエラー情報を取得するには、使用している言語や環境の適切なエラー トラッピング機能を使用し、ネストされたループで **Errors** コレクションの各 **Error** オブジェクトのプロパティを列挙します。

**Microsoft Visual Basic および VBScript ユーザー**有効な**Connection**オブジェクトがない場合は、error オブジェクトからエラー情報を取得する**** 必要があります。

ADO は、プロバイダーと同様に、新たなプロバイダー エラーを発生させる可能性がある呼び出しを行う前に、 **OLE Error Info** オブジェクトをクリアします。ただし、 **Connection** オブジェクトの **Errors** コレクションがクリアされ、オブジェクトが追加されるのは、プロバイダーで新しいエラーが生成されるか、 [Clear](clear-method-ado.md) メソッドを呼び出す場合のみです。

プロパティとメソッドの中には、 **Errors** コレクションの **Error** オブジェクトとして警告を返しても、プログラムの実行を停止しないものがあります。 [Recordset](resync-method-ado.md) オブジェクトで [Resync](updatebatch-method-ado.md) メソッド、 [UpdateBatch](cancelbatch-method-ado.md) メソッド、または [CancelBatch](recordset-object-ado.md) メソッドを呼び出す前、 [Connection](open-method-ado-connection.md) オブジェクトで **Open** メソッドを呼び出す前、または [Recordset](filter-property-ado.md) オブジェクトで **Filter** プロパティを設定する前に、 **Errors** コレクションで **Clear** メソッドを呼び出す必要があります。これにより、 [Errors](count-property-ado.md) コレクションの **Count** プロパティを読み取り、返された警告を調べることができます。

