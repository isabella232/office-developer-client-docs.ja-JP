---
title: Command オブジェクト (ADO)
TOCTitle: Command Object (ADO)
ms:assetid: 64f4ef03-f858-c004-b891-0c96d13a5e6e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249389(v=office.15)
ms:contentKeyID: 48545303
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231106
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 153f59ebbcfae89f6358fe0d707791aab8a8cdd7
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864075"
---
# <a name="command-object-ado"></a>Command オブジェクト (ADO)


**適用されます**Access 2013 |。Office 2013

データ ソースに対して実行する特定のコマンドを定義します。

## <a name="remarks"></a>備考

**Command** オブジェクトを使用すると、データベースに対してクエリを実行して [Recordset](recordset-object-ado.md) オブジェクトのレコードを取得したり、一括操作を実行したり、データベースの構造を操作したりできます。プロバイダーの機能によっては、 **Command** の一部のコレクション、メソッド、またはプロパティを参照すると、エラーが発生する場合があります。

**Command** オブジェクトのコレクション、メソッド、およびプロパティを使用すると、次の操作を実行できます。

  - [CommandText](commandtext-property-ado.md) プロパティを使用して、コマンドの実行可能なテキスト (SQL ステートメント) を定義できます。

  - [Parameter](parameter-object-ado.md) オブジェクトと [Parameters](parameters-collection-ado.md) コレクションを使用して、パラメーター化されたクエリまたはストアド プロシージャの引数を定義できます。

<<<<<<< 見出し
  - **Execute** メソッドを使用して、コマンドを実行し、必要に応じて [Recordset](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) オブジェクトを取得できます。
=======
  - **Execute** メソッドを使用して、コマンドを実行し、必要に応じて [Recordset](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) オブジェクトを取得できます。
>>>>>>> master

  - [CommandType](commandtype-property-ado.md) プロパティを使用して、コマンドを実行する前にそのコマンドの種類を指定し、パフォーマンスを向上できます。

  - [Prepared](prepared-property-ado.md) プロパティを使用して、コマンドの実行前に、プロバイダーがそのコマンドの準備された (コンパイル済みの) バージョンを保存するかどうかを制御できます。

  - [CommandTimeout](commandtimeout-property-ado.md) プロパティを使用して、コマンドの実行までプロバイダーが待機する時間を秒数で設定できます。

  - **Command** オブジェクトの [ActiveConnection](activeconnection-property-ado.md) プロパティを使用して、開いている接続をそのオブジェクトに関連付けることができます。

  - [Name](name-property-ado.md) プロパティを設定して、 **Command** オブジェクトを関連付けられている [Connection](connection-object-ado.md) オブジェクトのメソッドとして識別できます。

  - **Command** オブジェクトを [Recordset](source-property-ado-recordset.md) の **Source** プロパティに渡すことにより、データを取得できます。

  - [Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有の属性にアクセスできます。

> [!NOTE]
> [!メモ] **Command** オブジェクトを使用せずにクエリを実行するには、クエリ文字列を [Connection](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) オブジェクトの **Execute** メソッド、または [Recordset](open-method-ado-recordset.md) オブジェクトの **Open** メソッドに渡します。ただし、コマンド テキストを永続化して再実行するか、クエリ パラメーターを使用する場合は、 **Command** オブジェクトが必要となります。

前に定義した **Connection** オブジェクトと無関係に **Command** オブジェクトを作成するには、その **ActiveConnection** プロパティを有効な接続文字列に設定します。その場合でも **Connection** オブジェクトは ADO によって作成されますが、オブジェクト変数に割り当てられることはありません。ただし、複数の **Command** オブジェクトを同一の接続に関連付ける場合は、明示的に **Connection** オブジェクトを作成して開く必要があります。こうすることで、 **Connection** オブジェクトがオブジェクト変数に割り当てられます。 **Command** オブジェクトの **ActiveConnection** プロパティをこのオブジェクト変数に設定しなかった場合、同じ接続文字列を使用しても、ADO によって各 **Command** オブジェクトに新しい **Connection** オブジェクトが作成されます。

**Command** を実行するには、関連する [Connection](name-property-ado.md) オブジェクトの該当する **Name** プロパティを使用して呼び出します。 **Command** では、その **ActiveConnection** プロパティを **Connection** オブジェクトに設定する必要があります。 **Command** にパラメーターがある場合は、その値を引数としてメソッドに渡します。

同じ接続で複数の **Command** オブジェクトを実行し、いずれかの **Command** オブジェクトが出力パラメーターを持つストアド プロシージャの場合、エラーが発生します。各 **Command** オブジェクトを実行するには、別の接続を使用するか、接続から他のすべての **Command** オブジェクトを切断します。

**Parameters** コレクションは **Command** オブジェクトの既定のメンバーです。結果として、次の 2 つのコード ステートメントは同じになります。

