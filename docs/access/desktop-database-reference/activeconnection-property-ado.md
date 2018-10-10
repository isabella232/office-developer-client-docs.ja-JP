---
title: ActiveConnection プロパティ (ADO)
TOCTitle: ActiveConnection Property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d44a17d192abdb68755a2010184b4fb4d6531174
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479635"
---
# <a name="activeconnection-property-ado"></a>ActiveConnection プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

指定された [Command](connection-object-ado.md) オブジェクト、 [Recordset](command-object-ado.md) オブジェクト、または [Record](recordset-object-ado.md) オブジェクトが現在属している [Connection](record-object-ado.md) オブジェクトを示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

接続が閉じている場合には接続の定義が格納された文字列型 ( **String** ) の値を、接続が開いている場合には現在の **Connection** オブジェクトが格納されたバリアント型 ( **Variant** ) の値を設定または取得します。既定は、Null オブジェクト参照です。 [ConnectionString](connectionstring-property-ado.md) プロパティの説明を参照してください。

## <a name="remarks"></a>解説

**ActiveConnection** プロパティを使用すると、指定された **Command** オブジェクトを実行する、または指定された **Recordset** を開く **Connection** オブジェクトを調べることができます。

**Command**

**Command** オブジェクトの場合、 **ActiveConnection** プロパティは値の設定も取得も可能です。

開いている [Connection](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) オブジェクトまたは有効な接続文字列をこのプロパティに設定する前に、 **Command** オブジェクトに対して **Execute** を呼び出そうとすると、エラーが発生します。

**Microsoft Visual Basic****ActiveConnection**プロパティを*Nothing*に設定すると、**コマンド**オブジェクトを現在の**接続**からの関連付けを解除し、プロバイダーにデータ ソースに関連付けられているリソースを解放すると、します。 その後は、その **Command** オブジェクトを同じまたは別の **Connection** オブジェクトに関連付けることができます。 一部のプロバイダーを使用すると、最初のプロパティを*Nothing*に設定することがなく 1 つの**接続**から、別のプロパティ設定を変更できます。

**コマンド**オブジェクトの[Parameters](parameters-collection-ado.md)コレクションには、プロバイダーによって指定されたパラメーターが含まれています、 *Nothing*または別の**接続**オブジェクトは、 **ActiveConnection**プロパティを設定する場合、コレクションがクリアされます。 手動で[パラメーター](parameter-object-ado.md)オブジェクトを作成、使用して、**コマンド**オブジェクトの**Parameters**コレクションを設定する場合設定の**ActiveConnection**プロパティは*Nothing*または別の**接続**オブジェクトにまま**パラメーター**コレクションをそのままの状態です。

**Command** オブジェクトが関連付けられている **Connection** オブジェクトを閉じると、**ActiveConnection** プロパティが *Nothing* に設定されます。このプロパティに閉じている **Connection** オブジェクトを設定すると、エラーが発生します。

**Recordset**

開いている **Recordset** オブジェクト、および **Source** プロパティが有効な [Command](source-property-ado-recordset.md) オブジェクトに設定されている **Recordset** オブジェクトについては、 **ActiveConnection** プロパティは値の取得のみ可能です。それ以外の場合は、値の取得および設定が可能です。

このプロパティは、有効な **Connection** オブジェクトまたは有効な接続文字列に設定できます。この場合、プロバイダーが、この定義を使用して新しい **Connection** オブジェクトを作成し、接続を開きます。さらに、プログラマが **Connection** オブジェクトにアクセスして拡張エラー情報を取得したり、その他のコマンドを実行したりできるように、プロバイダーがこのプロパティを新しい **Connection** オブジェクトに設定する場合もあります。

**Recordset**オブジェクトを開くに*は、 [Open](open-method-ado-recordset.md)メソッドの暗黙的*を使用する場合、 **ActiveConnection**プロパティは、引数の値を継承します。

**Recordset** オブジェクトの **Source** プロパティを有効な **Command** オブジェクト変数に設定すると、 **Recordset** の **ActiveConnection** プロパティは、 **Command** オブジェクトの **ActiveConnection** プロパティの値を継承します。

**リモート データ サービスの使用法**クライアント側の Recordset オブジェクトで使用するとこのプロパティのみを接続文字列、または (Microsoft Visual Basic または Visual Basic、Scripting Edition) で*何も*します。

**Record**

このプロパティは、 **Record** オブジェクトが閉じている場合には値の設定および取得が可能で、接続文字列または開いている **Connection** オブジェクトの参照を格納できます。 **Record** オブジェクトが開いている場合は値の取得のみ可能で、開いている **Connection** オブジェクトの参照が格納されています。

**Connection** オブジェクトは、URL から **Record** オブジェクトが開かれたときに暗黙的に作成されます。既存の、開いている **Connection** オブジェクトで **Record** を開くには、 **Connection** オブジェクトをこのプロパティに代入するか、または **Connection** オブジェクトを [Open](open-method-ado-record.md) メソッド呼び出しのパラメーターとして使用します。 **Record** は、既存の **Record** または [Recordset](recordset-object-ado.md) から開かれた場合には、その **Record** または **Recordset** オブジェクトの **Connection** オブジェクトに自動的に関連付けられます。


> [!NOTE]
> <P>[!メモ] http スキームを使用している URL は、<A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A> を自動的に呼び出します。詳細については、「 <A href="absolute-and-relative-urls.md">絶対 URL と相対 URL</A>」を参照してください。</P>


