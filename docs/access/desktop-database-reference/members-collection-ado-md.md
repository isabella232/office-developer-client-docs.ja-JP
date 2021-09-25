---
title: Members コレクション (ADO MD)
TOCTitle: Members collection (ADO MD)
ms:assetid: 1389c554-e4f1-107d-22c6-7fe851d53d23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248910(v=office.15)
ms:contentKeyID: 48543371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 474b2ccb10fbd4d68e89c352fa8700e33a2923da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602214"
---
# <a name="members-collection-ado-md"></a>Members コレクション (ADO MD)


**適用先**: Access 2013、Office 2013

レベル、または軸上の位置からの [Member](member-object-ado-md.md) オブジェクトを含みます。

## <a name="remarks"></a>注釈

**Members** コレクションには、以下の種類のメンバーを含めることができます。

  - キューブのレベルを構成するメンバーで、**Level** オブジェクトの [Members](level-object-ado-md.md) コレクションに含まれます。たとえば、「 [多次元スキーマおよびデータの概要](overview-of-multidimensional-schemas-and-data.md)」のサンプルでは、Countries レベルの 4 つのメンバーは、Canada、USA、UK、および Germany です。

  - 階層内の特定のメンバーの子であるメンバー。このメンバーは、親 の [Member](children-property-ado-md.md) オブジェクトの **Children** プロパティによって取得できます。たとえば、上記と同じサンプルでは、Canada メンバーの 2 つの子は Canada-East と Canada-West です。

  - [cellset](cellset-object-ado-md.md) の軸上の特定の位置を定義するメンバー。たとえば、「 [多次元データを処理する](working-with-multidimensional-data.md)」のセルセットでは、x 軸上の最初の位置の 2 つのメンバーは Valentine と Seattle です。この 2 つのメンバーは、**Position** オブジェクトの [Members](position-object-ado-md.md) コレクションに含まれます。

**Members** は、標準の ADO コレクションです。このコレクションのプロパティとメソッドを使用すると、次の操作を実行できます。

  - [Count](count-property-ado.md) プロパティを使用して、コレクションの尾オブジェクトの数を取得します。

  - 既定の [Item](item-property-ado.md) プロパティを使用して、コレクションからオブジェクトを返します。

  - [Refresh](refresh-method-ado.md) メソッドを使用して、プロバイダーからコレクションのオブジェクトを更新します。

