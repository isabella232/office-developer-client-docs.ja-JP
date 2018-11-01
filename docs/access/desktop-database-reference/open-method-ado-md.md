---
title: Open メソッド (ADO MD)
TOCTitle: Open Method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9b39fa77700fcd1553738d359b8efd7097c183a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870276"
---
# <a name="open-method-ado-md"></a>Open メソッド (ADO MD)


**適用されます**Access 2013、Office 2013。

多次元クエリの結果を取得し、結果をセルセットに返します。

## <a name="syntax"></a>構文

*セルセット*。オープン*ソース*、 *ActiveConnection*

## <a name="parameters"></a>パラメーター

  - *Source*

  - 省略可能です。 Multidimensional Expression (MDX) クエリのような有効な多次元クエリを評価するバリアント型 ( **Variant** ) を指定します。 *変換元*の引数は、 [Source](source-property-ado-md.md)プロパティに対応します。 MDX の詳細については、Microsoft Data Access Components SDK の OLE DB for OLAP のマニュアルを参照してください。

  - *ActiveConnection*

  - 省略可能です。 有効な ADO **Connection** オブジェクトの変数名、または接続の定義のどちらかを指定する文字列を評価するバリアント型 ( [Variant](connection-object-ado.md) ) を指定します。 [Cellset](cellset-object-ado-md.md)オブジェクトを開くときに接続を*暗黙的*に指定します。 この引数に接続の定義を指定すると、ADO により、指定されたパラメーターを使用して新しい接続が開かれます。 *暗黙的*では、 [ActiveConnection](activeconnection-property-ado-md.md)プロパティに対応します。

## <a name="remarks"></a>解説

**Open** メソッドのパラメーターのどちらかが省略され、 **Cellset** を開こうとするよりも前に、対応するプロパティ値が設定されていない場合、エラーが発生します。

