---
title: Parameter オブジェクト (ADO)
TOCTitle: Parameter Object (ADO)
ms:assetid: 7577598e-3d0c-30c6-5f24-1cfe98791798
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249481(v=office.15)
ms:contentKeyID: 48545676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7667828d2ebfdc554a7120bf495374bc50e51cfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477028"
---
# <a name="parameter-object-ado"></a>Parameter オブジェクト (ADO)


**適用されます**Access 2013 |。Office 2013

パラメーター クエリまたはストアド プロシージャに基づく、[Command](command-object-ado.md) オブジェクトに関連付けられたパラメーターまたは引数を表します。

## <a name="remarks"></a>備考

プロバイダーの多くは、パラメーター化されたコマンドをサポートしています。これらのコマンドでは、必要なアクションが事前に定義されていますが、コマンドの一部の詳細を変更するために変数 (またはパラメーター) が使用されています。たとえば、SQL SELECT ステートメントでは、あるパラメーターを使用して WHERE 句の照合条件を定義し、別のパラメーターを使用して SORT BY 句の列名を定義できます。

**Parameter** オブジェクトは、パラメーター化されたクエリ、またはストアド プロシージャの入出力引数と戻り値に関連付けられたパラメーターを表します。プロバイダーの機能によっては、 **Parameter** オブジェクトの一部のコレクション、メソッド、またはプロパティを使用できない場合があります。

**Parameter** オブジェクトのコレクション、メソッド、およびプロパティを使用すると、次の操作を実行できます。

  - [Name](name-property-ado.md) プロパティを使用して、パラメーターの名前を設定または取得できます。

  - [Value](value-property-ado.md) プロパティを使用して、パラメーターの値を設定または取得できます。 **Value** は、 **Parameter** オブジェクトの既定のプロパティです。

  - [Attributes](attributes-property-ado.md)、[Direction](direction-property-ado.md)、[Precision](precision-property-ado.md)、[NumericScale](numericscale-property-ado.md)、[Size](size-property-ado.md)、および [Type](type-property-ado.md) の各プロパティを使用して、パラメーターの特性を設定または取得できます。

  - [AppendChunk](appendchunk-method-ado.md) メソッドを使用して、長いバイナリ データまたは文字データを渡すことができます。

  - [Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有の属性にアクセスできます。

呼び出すストアド プロシージャまたはパラメーター化されたクエリに関連するパラメーターの名前とプロパティを把握している場合、[CreateParameter](createparameter-method-ado.md) メソッドを使用して、適切なプロパティが設定された **Parameter** オブジェクトを作成し、 [Append](append-method-ado.md) メソッドを使用して、それらのオブジェクトを [Parameters](parameters-collection-ado.md) コレクションに追加できます。これにより、 [Parameters](refresh-method-ado.md) コレクションの **Refresh** メソッドを呼び出してプロバイダーからパラメーター情報を取得しなくても、パラメーターの値を設定したり取得したりすることができるため、リソース消費量を少なくできます。

