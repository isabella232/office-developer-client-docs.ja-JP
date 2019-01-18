---
title: Cellset オブジェクト (ADO MD)
TOCTitle: Cellset object (ADO MD)
ms:assetid: 28d4b3b9-f907-9ec0-00e1-9666c887cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249047(v=office.15)
ms:contentKeyID: 48543869
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8cb75ad7277386cfe81b2edcffa234498318444
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702188"
---
# <a name="cellset-object-ado-md"></a>Cellset オブジェクト (ADO MD)

**適用されます**Access 2013、Office 2013。

多次元クエリの結果を表します。キューブまたは他のセルセットから選択されたセルのコレクションになります。

## <a name="remarks"></a>解説

**Cellset** 内のデータは、直接の配列のようなアクセス方法を使用して取得できます。特定のメンバーに "ドリル ダウン" してそのメンバーに関するデータを取得できます。たとえば、次のコードは、cst というセルセットの最初の軸の最初の位置の最初のメンバーのキャプションを返します。

`cst.Axes(0).Positions(0).Members(0).Caption`

セルセットには現在のセルの概念はありませんが、代わりに [Item](item-property-ado-md-cellset.md) プロパティを使用して、セルセットの特定の [Cell](cell-object-ado-md.md) オブジェクトを取得できます。取得するセルは、 **Item** プロパティの引数によって指定します。セルの一意の序数値を指定できます。セルセットの各軸上の位置番号を使用してセルを取得することもできます。セルの取得方法の詳細については、 [Item](item-property-ado-md-cellset.md) プロパティを参照してください。

**Cellset** オブジェクトのコレクション、メソッド、およびプロパティを使用すると、次の操作を実行できます。

  - **Cellset** オブジェクトの [ActiveConnection](activeconnection-property-ado-md.md) プロパティを使用して、開いている接続をそのオブジェクトに関連付けることができます。

  - [Open](open-method-ado-md.md) メソッドを使用して、多次元クエリを実行して結果を取得します。

  - **Item** プロパティを使用して、 **Cellset** から [Cell](item-property-ado-md-cellset.md) を取得します。

  - [Axes](axis-object-ado-md.md) コレクションを使用して、 **Cellset** を定義する [Axis](axes-collection-ado-md.md) オブジェクトを返します。

  - **FilterAxis** プロパティを使用して、 [Cellset](filteraxis-property-ado-md.md) 内のデータをフィルター処理するための次元に関する情報を取得します。

  - **Source** プロパティを使用して、 [Cellset](source-property-ado-md.md) を定義するためのクエリを返すか、または指定します。

  - **State** プロパティを使用して、 [Cellset](state-property-ado-md.md) の現在の状態 (開いている、閉じている、実行中、または接続中) を返します。

  - **Close** メソッドを使用して、 [Cellset](close-method-ado-md.md) を開くか、または閉じます。

  - 標準の ADO **Properties** コレクションを使用して、 [Cellset](properties-collection-ado.md) に関するプロバイダー固有の情報を取得します。

