---
title: Source プロパティ (ADO Record)
TOCTitle: Source property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e9c15b0c67aa19b6f629fb3f966be1cb0458fe26
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605884"
---
# <a name="source-property-ado-record"></a>Source プロパティ (ADO Record)


**適用先**: Access 2013、Office 2013

[Record](record-object-ado.md) で表されるデータ ソースまたはオブジェクトを示します。

## <a name="settings-and-return-values"></a>設定および戻り値

**Record** が表すエンティティを示すバリアント型 (**Variant**) の値を設定または取得します。

## <a name="remarks"></a>注釈

**Source** プロパティは、**Record** オブジェクトの [Open](open-method-ado-record.md) メソッドの *Source* 引数を返します。 このプロパティには絶対 URL または相対 URL の文字列を格納できます。 絶対 URL を使用すると、 [ActiveConnection](activeconnection-property-ado.md) プロパティを設定せずに、直接 **Record** オブジェクトを開くことができます。 この場合、暗黙の **Connection** オブジェクトが作成されます。

**Source** プロパティには、既に開いている **Recordset** への参照も格納でき、この参照は **Recordset** 内の現在の行を表す **Record** オブジェクトを開きます。

また、 **Source** プロパティには、プロバイダーから 1 つのデータ行を返す [Command](command-object-ado.md) オブジェクトへの参照も格納できます。

**ActiveConnection** プロパティも設定する場合は、 **Source** プロパティはその接続範囲内に存在する同じオブジェクトを指している必要があります。たとえば、ツリー構造の名前空間では、 **Source** プロパティに絶対 URL が格納されている場合、接続文字列の URL で指定されたノードの範囲内に存在するノードを指している必要があります。 **Source** プロパティに相対 URL が格納されている場合、 **ActiveConnection** プロパティで設定されたコンテキスト内でのみ有効になります。

**Source** プロパティは、 **Record** オブジェクトが閉じている場合は値の取得および設定が可能で、 **Record** オブジェクトが開いている場合は値の取得のみ可能です。

> [!NOTE]
> [!メモ] http スキーマを使用している URL は自動的に [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を呼び出します。 詳細については、「絶対 URL と [相対 URL」を参照してください](absolute-and-relative-urls.md)。


