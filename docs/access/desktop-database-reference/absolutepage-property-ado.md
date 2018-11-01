---
title: AbsolutePage プロパティ (ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: a285f9f9533e4ecd903e6cc6c0e427bf44c84ca4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870535"
---
# <a name="absolutepage-property-ado"></a>AbsolutePage プロパティ (ADO)

**適用されます**Access 2013、Office 2013。

カレント レコードがあるページを示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

設定 ([PageCount](pagecount-property-ado.md))、[レコード セット](recordset-object-ado.md)オブジェクト内のページの数を 1 から**long 型**の値を返します。 または[PositionEnum](positionenum.md)値のいずれかを返します。

## <a name="remarks"></a>解説

このプロパティを使用すると、カレント レコードが置かれているページのページ番号を識別できます。このプロパティは、[PageSize](pagesize-property-ado.md) プロパティを使用して、各ページが **PageSize** と等しいレコード数を持つように (ただし最終ページのみ例外で、レコード数が少なくなる場合があります) **Recordset** オブジェクトの行セットの合計カウントを一連のページへと論理的に分割します。このプロパティを使用するには、プロバイダーが必要な機能をサポートしている必要があります。

**AbsolutePage** プロパティを取得または設定する際には、ADO により [AbsolutePosition](absoluteposition-property-ado.md) プロパティと [PageSize](pagesize-property-ado.md) プロパティが以下のように組み合わせて使用されます。

- **AbsolutePage** を取得する場合、ADO はまず **AbsolutePosition** の値を取得し、それを **PageSize** で割ります。

- **AbsolutePage** を設定する場合、ADO は、 **PageSize** に新しい **AbsolutePage** 値を掛けてからその値に 1 を加えることにより、 **AbsolutePosition** を移動します。 その結果**と、AbsolutePage**を正常に設定した後、**レコード セット**内の現在位置は、そのページの最初のレコードです。

**AbsolutePage** は、 **AbsolutePosition** プロパティと同じく 1 から始まる値で、 **Recordset** の先頭レコードがカレント レコードの場合に 1 になります。このプロパティを設定すると、特定のページの先頭レコードへと移動します。総ページ数は、 **PageCount** プロパティから取得できます。

