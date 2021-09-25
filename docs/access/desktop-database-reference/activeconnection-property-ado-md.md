---
title: ActiveConnection プロパティ (ADO MD)
TOCTitle: ActiveConnection property (ADO MD)
ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15)
ms:contentKeyID: 48547845
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2d4892d330eda957b7064f46bf1d5114bbdbfbae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569532"
---
# <a name="activeconnection-property-ado-md"></a>ActiveConnection プロパティ (ADO MD)

**適用先:** Access 2013、Office 2013

現在のセルセットまたはカタログが、現在どの ADO [Connection](connection-object-ado.md) オブジェクトに属しているのかを示します。

## <a name="settings-and-return-values"></a>設定および戻り値

接続を定義する文字列、または **Connection** オブジェクトを含むバリアント型 ( **Variant** ) を設定または取得します。既定値は Empty 値です。

## <a name="remarks"></a>注釈

このプロパティには、有効な ADO **Connection** オブジェクト、または有効な接続文字列を設定します。接続文字列を設定すると、この定義を使用した新規の **Connection** オブジェクトがプロバイダーによって作成され、接続が開かれます。

**Open** メソッドの [ActiveConnection](open-method-ado-md.md) 引数を使用して [Cellset](cellset-object-ado-md.md) オブジェクトを開くと、引数の値が **ActiveConnection** プロパティに継承されます。

**Catalog** オブジェクトの [ActiveConnection](catalog-object-ado-md.md) プロパティを **Nothing** に設定すると、 [CubeDefs](cubedefs-collection-ado-md.md) コレクションおよび関連付けられたすべての [Dimension](dimension-object-ado-md.md)、[Hierarchy](hierarchy-object-ado-md.md)、[Level](level-object-ado-md.md)、および [Member](member-object-ado-md.md) オブジェクトを含む、関連付けられたデータが解放されます。 **Catalog** を開くために使用した **Connection** オブジェクトを閉じると、 **ActiveConnection** プロパティを **Nothing** に設定した場合と同じ効果があります。

**Catalog** オブジェクトの **ActiveConnection** プロパティによって参照されている接続の既定のデータベースを変更すると、 **Catalog** の内容が無効になります。

開いている **Cellset** オブジェクトの **ActiveConnection** プロパティを変更しようとすると、エラーが発生します。

> [!NOTE]
> [!メモ] Visual Basic では、 **ActiveConnection** プロパティを **Connection** オブジェクトに設定する場合、必ず **Set** キーワードを使用してください。 **Set** キーワードを省略すると、 **ActiveConnection** プロパティに、実際には、 **Connection** オブジェクトの既定のプロパティである **ConnectionString** と同じものを設定していることになります。このコードは動作しますが、データ ソースへの追加の接続が作成されるため、パフォーマンスに悪い影響を与えることがあります。

MSOLAP データ プロバイダーを使用する場合、接続文字列内でデータ ソースをサーバー名に設定し、初期カタログにデータ ソースのカタログの名前を設定します。サーバーに接続されていないキューブ ファイルに接続するには、その .CUB ファイルのある場所へのフル パスを設定します。どちらの場合でも、プロバイダーにはプロバイダー名を設定します。たとえば、次の文字列を設定すると、MSOLAP プロバイダーを使用して Servername という名前のサーバーにある Bobs Video Store という名前のカタログに接続されます。

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

次の文字列は、場所 C のローカル キューブ ファイルに接続します \\ 。MSDASDK は \\ \\ oledb \\ olap \\ データ \\ bobsvid.cub をサンプルします。

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

