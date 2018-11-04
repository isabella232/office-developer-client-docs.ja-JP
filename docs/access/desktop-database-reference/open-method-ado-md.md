---
title: Open メソッド (ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 86a4dcd97171a1dc9817f69a6c010a363009e9ef
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949594"
---
# <a name="open-method-ado-md"></a>Open メソッド (ADO MD)

**適用されます**Access 2013、Office 2013。

多次元クエリの結果を取得し、結果をセルセットに返します。

## <a name="syntax"></a>構文

*セルセット*。オープン*ソース*、 *ActiveConnection*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Source* |省略可能です。 Multidimensional Expression (MDX) クエリのような有効な多次元クエリを評価するバリアント型 ( **Variant** ) を指定します。 *変換元*の引数は、 [Source](source-property-ado-md.md)プロパティに対応します。 MDX の詳細については、Microsoft Data Access Components SDK の OLE DB for OLAP のマニュアルを参照してください。|
|*ActiveConnection* |省略可能です。 有効な ADO **Connection** オブジェクトの変数名、または接続の定義のどちらかを指定する文字列を評価するバリアント型 ( [Variant](connection-object-ado.md) ) を指定します。 [Cellset](cellset-object-ado-md.md)オブジェクトを開くときに接続を*暗黙的*に指定します。 この引数に接続の定義を指定すると、ADO により、指定されたパラメーターを使用して新しい接続が開かれます。 *暗黙的*では、 [ActiveConnection](activeconnection-property-ado-md.md)プロパティに対応します。|

## <a name="remarks"></a>解説

**Open** メソッドのパラメーターのどちらかが省略され、 **Cellset** を開こうとするよりも前に、対応するプロパティ値が設定されていない場合、エラーが発生します。

