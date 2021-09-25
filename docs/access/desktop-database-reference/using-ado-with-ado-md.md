---
title: ADO と ADO MD を共に使用する
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5d74f4d587462290fa99bb2524b4dc264af9d591
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588876"
---
# <a name="using-ado-with-ado-md"></a>ADO MD を用いた ADO の使用


**適用先**: Access 2013、Office 2013

ADO と ADO MD は関連はしていますが、別々のオブジェクト モデルです。ADO には、データ ソースへの接続、コマンドの実行、表形式のデータと表形式のスキーマ メタデータの取得、およびプロバイダーのエラー情報を表示するためのオブジェクトが用意されています。ADO MD には、多次元データの取得、および多次元スキーマ メタデータの表示のためのオブジェクトが用意されています。

MDP で作業する場合、作成するアプリケーションでは、ADO、ADO MD、またはその両方を選択できます。プロジェクトから両方のライブラリを参照することにより、MDP で提供されるすべての機能に完全にアクセスすることができます。

多次元データセットを単層化した表形式で表示できることは、便利な場合があります。 これを行うには、ADO の [Recordset](recordset-object-ado.md) オブジェクトを使用します。 ADO MD セルセットのソースとしてではなく、_*Recordset**の [Open](open-method-ado-recordset.md)メソッドの * Source **_** パラメーターとして [Cellset](cellset-object-ado-md.md)のソースを **指定します**。

また、スキーマ メタデータをオブジェクトの階層としてではなく、表形式のビューで表示する場合にも役立ちます。 [Connection](connection-object-ado.md)オブジェクトの ADO [OpenSchema](openschema-method-ado.md)メソッドを使用すると、ユーザーはスキーマ情報を含む **Recordset** を開くことができる。 _ **_OpenSchema_ メソッドの QueryType *_*** パラメーターには、MDP に特に関連する [SchemaEnum](schemaenum.md)値がいくつか含まれます。 これらの値は次のとおりです。

  - **adSchemaCubes**

  - **adSchemaDimensions**

  - **adSchemaHierarchies**

  - **adSchemaLevels**

  - **adSchemaMeasures**

  - **adSchemaMembers**

ADO の列挙値を ADO MD のプロパティまたはメソッドで使用するには、プロジェクトで ADO ライブラリと ADO MD ライブラリの両方に対する参照を設定する必要があります。たとえば、ADO の **adState** 列挙値を ADO MD の [State](state-property-ado-md.md) プロパティで使用できます。ライブラリへの参照を確立する方法の詳細については、開発ツールのマニュアルを参照してください。

ADO のオブジェクトおよびメソッドの詳細については、「[ADO API リファレンス](ado-api-reference.md)」を参照してください。

