---
title: ActiveConnection プロパティ (ADO)
TOCTitle: ActiveConnection property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 10/17/2018
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 3be71b700b670309a021de491c9e2af2e448084d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586272"
---
# <a name="activeconnection-property-ado"></a>ActiveConnection プロパティ (ADO)

**適用先**: Access 2013、Office 2013

指定された [Command](connection-object-ado.md) オブジェクト、 [Recordset](command-object-ado.md) オブジェクト、または [Record](recordset-object-ado.md) オブジェクトが現在属している [Connection](record-object-ado.md) オブジェクトを示します。

## <a name="settings-and-return-values"></a>設定および戻り値

接続が閉じている場合には接続の定義が格納された文字列型 ( **String** ) の値を、接続が開いている場合には現在の **Connection** オブジェクトが格納されたバリアント型 ( **Variant** ) の値を設定または取得します。既定は、Null オブジェクト参照です。 [ConnectionString](connectionstring-property-ado.md) プロパティの説明を参照してください。

## <a name="remarks"></a>注釈

**ActiveConnection** プロパティを使用すると、指定された **Command** オブジェクトを実行する、または指定された **Recordset** を開く **Connection** オブジェクトを調べることができます。

### <a name="command"></a>コマンド

**Command** オブジェクトの場合、**ActiveConnection** プロパティは値の設定も取得も可能です。

開いている [Connection](/office/vba/access/concepts/miscellaneous/execute-method-ado-command.md) オブジェクトまたは有効な接続文字列をこのプロパティに設定する前に、 **Command** オブジェクトに対して **Execute** を呼び出そうとすると、エラーが発生します。

**Microsoft Visual Basic**: **ActiveConnection** プロパティを *Nothing* に設定すると **、Command** オブジェクトは現在の **Connection** から関連付け解除され、プロバイダーはデータ ソース上の関連付けられたリソースを解放します。 その後は、その **Command** オブジェクトを同じまたは別の **Connection** オブジェクトに関連付けることができます。 一部のプロバイダーでは、最初にプロパティを Nothing に設定することなく、プロパティ設定を Connection から別の **Connection** に変更 *できます*。

**Command** オブジェクトの [Parameters](parameters-collection-ado.md) コレクションにプロバイダーから供給されたパラメーターが格納されている場合は、**ActiveConnection** プロパティを *Nothing* に設定したり、他の **Connection** オブジェクトに設定したりすると、コレクションがクリアされます。手作業で [Parameter](parameter-object-ado.md) オブジェクトを作成し、それを使用して **Command** オブジェクトの **Parameters** コレクションにデータを格納した場合は、**ActiveConnection** プロパティを *Nothing* や他の **Connection** オブジェクトに設定しても、**Parameters** コレクションはそのまま残されます。

**Command** オブジェクトが関連付けられている **Connection** オブジェクトを閉じると、**ActiveConnection** プロパティが *Nothing* に設定されます。このプロパティに閉じている **Connection** オブジェクトを設定すると、エラーが発生します。

### <a name="recordset"></a>Recordset

開いている **Recordset** オブジェクト、および **Source** プロパティが有効な [Command](source-property-ado-recordset.md) オブジェクトに設定されている **Recordset** オブジェクトについては、 **ActiveConnection** プロパティは値の取得のみ可能です。それ以外の場合は、値の取得および設定が可能です。

このプロパティは、有効な **Connection** オブジェクトまたは有効な接続文字列に設定できます。この場合、プロバイダーが、この定義を使用して新しい **Connection** オブジェクトを作成し、接続を開きます。さらに、プログラマが **Connection** オブジェクトにアクセスして拡張エラー情報を取得したり、その他のコマンドを実行したりできるように、プロバイダーがこのプロパティを新しい **Connection** オブジェクトに設定する場合もあります。

[Open](open-method-ado-recordset.md) メソッドの *ActiveConnection* 引数を使用して **Recordset** オブジェクトを開いた場合、**ActiveConnection** プロパティは引数の値を継承します。

**Recordset** オブジェクトの **Source** プロパティを有効な **Command** オブジェクト変数に設定すると、**Recordset** の **ActiveConnection** プロパティは、**Command** オブジェクトの **ActiveConnection** プロパティの値を継承します。

**リモート データ サービスの使用状況**: クライアント側の Recordset オブジェクトで使用する場合、このプロパティは接続文字列または (Microsoft Visual Basic または Visual Basic、 Scripting Edition) に対して Nothing にのみ設定 *できます*。

### <a name="record"></a>Record

このプロパティは、**Record** オブジェクトが閉じている場合には値の設定および取得が可能で、接続文字列または開いている **Connection** オブジェクトの参照を格納できます。**Record** オブジェクトが開いている場合は値の取得のみ可能で、開いている **Connection** オブジェクトの参照が格納されています。

**Connection** オブジェクトは、URL から **Record** オブジェクトが開かれたときに暗黙的に作成されます。 既存の、開いている **Connection** オブジェクトで **Record** を開くには、 **Connection** オブジェクトをこのプロパティに代入するか、または **Connection** オブジェクトを [Open](open-method-ado-record.md) メソッド呼び出しのパラメーターとして使用します。 既存の **レコードまたは Recordset** からレコードを開いた [](recordset-object-ado.md)場合、その **Record** オブジェクトまたは Recordset オブジェクトの **Connection** オブジェクトに自動的に **関連付** けされます。

> [!NOTE]
> [!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、「絶対 URL と [相対 URL」を参照してください](absolute-and-relative-urls.md)。
