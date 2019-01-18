---
title: Record オブジェクト (ADO)
TOCTitle: Record object (ADO)
ms:assetid: 817aaf13-78d4-1134-aa94-997e92077c22
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249557(v=office.15)
ms:contentKeyID: 48545952
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 96ddc7fc1a93543f0eea2b42a3d423ec25a00636
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721508"
---
# <a name="record-object-ado"></a>Record オブジェクト (ADO)


**適用されます**Access 2013、Office 2013。

[Recordset](recordset-object-ado.md) オブジェクトやデータ プロバイダーの行、または、半構造化データ プロバイダーから返されるファイルやディレクトリなどのオブジェクトを表します。

## <a name="remarks"></a>備考

**Record** オブジェクトはデータの 1 つの行を表し、1 行から成る **Recordset** に概念が似ています。プロバイダーの機能によっては、1 行から成る **Recordset** の代わりに、 **Record** オブジェクトが直接プロバイダーから返される場合があります (たとえば、1 行のみ選択する SQL クエリを実行したときなど)。また、 **Record** オブジェクトは、 **Recordset** オブジェクトから直接取得されることもあります。または、Microsoft Exchange OLE DB Provider などの半構造化データ プロバイダーから直接 **Record** オブジェクトが返される場合もあります。

**Record** オブジェクトに関連付けられたフィールドは、 [Record](fields-collection-ado.md) オブジェクトの **Fields** コレクションを使用して表示できます。ADO では、 **Recordset** 、 **SafeArray** 、および **Record** オブジェクトの **Fields** コレクションのスカラー値などの、オブジェクト値の列を利用できます。

**Record** オブジェクトが **Recordset** の行を表す場合、 **Source** プロパティを使用して元の [Recordset](source-property-ado-record.md) に戻すことができます。

また、**Microsoft OLE DB Provider for Internet Publishing** などの半構造化データ プロバイダーは、 [Record](microsoft-ole-db-provider-for-internet-publishing.md) オブジェクトを使用してツリー構造の名前空間をモデル化することができます。ツリー内のノードは、関連付けられた列を持つ **Record** オブジェクトを表します。列は、そのノードの属性とその他の関連情報を表します。 **Record** オブジェクトは、ツリー構造のリーフ ノードと非リーフ ノードの両方を表すことができます。非リーフ ノードは、そのコンテンツとしてほかのノードを持っていますが、リーフ ノードはそのようなコンテンツを持ちません。リーフ ノードは、通常、データのバイナリ ストリームを格納していますが、非リーフ ノードも、関連付けられた既定のバイナリ ストリームを格納している場合があります。 **Record** オブジェクトのプロパティで、ノードの種類を識別することができます。

**Record** オブジェクトは、階層構造のデータ間を移動する手段としても使用できます。 **Record** オブジェクトを作成して、それを大規模なツリー構造の特定のサブツリーのルートにすると、新しい **Record** オブジェクトを子ノードとして開くことができます。

リソース (たとえば、ファイルまたはディレクトリ) は、絶対 URL で一意に識別できます。 暗黙的に[接続](connection-object-ado.md)オブジェクトが作成され、絶対 URL を持つ**レコード**を開くと**Record**オブジェクトに設定します。 **接続**オブジェクトは、 [ActiveConnection](activeconnection-property-ado.md)プロパティを使用して**Record**オブジェクトに明示的に設定することがあります。 ファイルとディレクトリの**接続**オブジェクトを通じてアクセス可能な*コンテキスト***レコード**操作が発生する可能性を定義します。

データを変更または移動する **Record** オブジェクトのメソッドでは相対 URL も利用でき、相対 URL では、絶対 URL または **Connection** オブジェクト コンテキストを起点としてリソースを検索します。

> [!NOTE]
> [!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、[絶対と相対 Url](absolute-and-relative-urls.md)を参照してください。



**Connection** オブジェクトは各 **Record** オブジェクトに関連付けられています。したがって、 **Connection** オブジェクトのトランザクション メソッドを呼び出せば、 **Record** オブジェクトの操作をトランザクションの一部にすることもできます。

**Record** オブジェクトは ADO イベントをサポートしていないので、通知には応答しません。

**Record** オブジェクトのメソッドとプロパティを使用すると、次の操作を実行できます。

  - **ActiveConnection** プロパティを使用して、関連する [Connection](activeconnection-property-ado.md) オブジェクトを設定または取得できます。

  - [Mode](mode-property-ado.md) プロパティを使用して、アクセス権限を示すことができます。

  - **ParentURL** プロパティを使用して、 [Record](parenturl-property-ado.md) が表すリソースを格納しているディレクトリの URL を取得できます。

  - **Source** プロパティを使用して、 **Record** の派生元となる絶対 URL、相対 URL、または [Recordset](source-property-ado-record.md) を示すことができます。

  - **State** プロパティを使用して、 [Record](state-property-ado.md) の現在のステータスを示すことができます。

  - **レコード**の種類を示す、*単純な**コレクション*、または*構造化されたドキュメント*: [RecordType](recordtype-property-ado.md)プロパティを使用して。

  - [Cancel](cancel-method-ado.md) メソッドを使用して、非同期操作の実行を停止できます。

  - **Close** メソッドを使用して、データ ソースと [Record](close-method-ado.md) との関連付けを解除できます。

  - **CopyRecord** メソッドを使用して、 [Record](copyrecord-method-ado.md) が表すファイルまたはディレクトリを別の場所にコピーできます。

  - **DeleteRecord** メソッドを使用して、 [Record](deleterecord-method-ado.md) が表すファイル、ディレクトリ、またはサブディレクトリを削除できます。

  - **GetChildren** メソッドを使用して、 **Record** が表すエンティティのサブディレクトリおよびファイルを表す行を格納している [Recordset](getchildren-method-ado.md) を開くことができます。

  - **MoveRecord** メソッドを使用して、 [Record](moverecord-method-ado.md) が表すファイル、ディレクトリ、またはサブディレクトリを別の場所に移動 (名前変更) できます。

  - **Open** メソッドを使用して、 [Record](open-method-ado-record.md) を既存のデータ ソースに関連付けたり、新規ファイルまたは新規ディレクトリを作成したりできます。

