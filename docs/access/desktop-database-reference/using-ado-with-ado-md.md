---
title: ADO と ADO MD を共に使用する
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 80c87f57a96f98de704e3cfa9b7689a522e4a7af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312748"
---
# <a name="using-ado-with-ado-md"></a>ADO MD を用いた ADO の使用


**適用先:** Access 2013、Office 2013

ADO と ADO MD は関連はしていますが、別々のオブジェクト モデルです。ADO には、データ ソースへの接続、コマンドの実行、表形式のデータと表形式のスキーマ メタデータの取得、およびプロバイダーのエラー情報を表示するためのオブジェクトが用意されています。ADO MD には、多次元データの取得、および多次元スキーマ メタデータの表示のためのオブジェクトが用意されています。

MDP で作業する場合、作成するアプリケーションでは、ADO、ADO MD、またはその両方を選択できます。プロジェクトから両方のライブラリを参照することにより、MDP で提供されるすべての機能に完全にアクセスすることができます。

多次元データセットを単層化した表形式で表示できることは、便利な場合があります。 これを行うには、ADO の [Recordset](recordset-object-ado.md) オブジェクトを使用します。 [Cellset オブジェクト](cellset-object-ado-md.md)のソースを指定する場合、ADO MD ***Cellset*** のソースとしてではなく、**Recordset** の Open メソッドの **[Source](open-method-ado-recordset.md)** パラメーターとして指定します。

また、オブジェクトの階層としてではなく、表形式のビューでスキーマのメタデータを表示すると便利な場合もあります。 [Connection](connection-object-ado.md)オブジェクトの ADO [OpenSchema](openschema-method-ado.md)メソッドを使用すると、ユーザーはスキーマ情報を含む**Recordset**を開くことができます。 **OpenSchema**メソッドの***QueryType***パラメーターには、mdps に特に関連する複数の[schemaenum](schemaenum.md)値があります。 これらの値は次のとおりです。

  - **adSchemaCubes**

  - **adschemadimensions**

  - **adschemahierarchies**

  - **adSchemaLevels**

  - **adschemameasures**

  - **adSchemaMembers**

ADO の列挙値を ADO MD のプロパティまたはメソッドで使用するには、プロジェクトで ADO ライブラリと ADO MD ライブラリの両方に対する参照を設定する必要があります。たとえば、ADO の **adState** 列挙値を ADO MD の [State](state-property-ado-md.md) プロパティで使用できます。ライブラリへの参照を確立する方法の詳細については、開発ツールのマニュアルを参照してください。

ADO のオブジェクトおよびメソッドの詳細については、「[ADO API リファレンス](ado-api-reference.md)」を参照してください。

