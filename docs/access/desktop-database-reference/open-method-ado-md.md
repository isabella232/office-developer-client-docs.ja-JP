---
title: Open メソッド (ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54f7ce4d5d588e644707cd7b466c29f619850824
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288400"
---
# <a name="open-method-ado-md"></a>Open メソッド (ADO MD)

**適用先:** Access 2013、Office 2013

多次元クエリの結果を取得し、結果をセルセットに返します。

## <a name="syntax"></a>構文

*Cellset*。オープン*ソース*、 *ActiveConnection*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Source* |省略可能です。Multidimensional Expression (MDX) クエリのような有効な多次元クエリを評価するバリアント型 (**Variant**) を指定します。*Source* 引数は、[Source](source-property-ado-md.md) プロパティに対応します。MDX の詳細については、Microsoft Data Access Components SDK の OLE DB for OLAP のマニュアルを参照してください。|
|*ActiveConnection* |省略可能です。有効な ADO [Connection](connection-object-ado.md) オブジェクトの変数名、または接続の定義のどちらかを指定する文字列を評価するバリアント型 (**Variant**) を指定します。*ActiveConnection* 引数は、[Cellset](cellset-object-ado-md.md) オブジェクトを開くための接続を指定します。この引数に接続の定義を渡すと、指定されたパラメーターを使用して新しい接続が ADO によって開かれます。*ActiveConnection* 引数は、[ActiveConnection](activeconnection-property-ado-md.md) プロパティに対応します。|

## <a name="remarks"></a>注釈

**Open** メソッドのパラメーターのどちらかが省略され、**Cellset** を開こうとするよりも前に、対応するプロパティ値が設定されていない場合、エラーが発生します。

