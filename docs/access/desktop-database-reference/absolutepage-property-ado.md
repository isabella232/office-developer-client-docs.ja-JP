---
title: AbsolutePage プロパティ (ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a0ad4caa6e31b6de39904016cd848e12690f72e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280685"
---
# <a name="absolutepage-property-ado"></a>AbsolutePage プロパティ (ADO)

**適用先:** Access 2013、Office 2013

カレント レコードがあるページを示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

1から[Recordset](recordset-object-ado.md)オブジェクトのページ数 ([PageCount](pagecount-property-ado.md)) までの**長整数型 (Long)** の値を設定するか、または[positionenum](positionenum.md)値の1つを取得します。

## <a name="remarks"></a>注釈

このプロパティを使用すると、カレント レコードが置かれているページのページ番号を識別できます。このプロパティは、[PageSize](pagesize-property-ado.md) プロパティを使用して、各ページが **PageSize** と等しいレコード数を持つように (ただし最終ページのみ例外で、レコード数が少なくなる場合があります) **Recordset** オブジェクトの行セットの合計カウントを一連のページへと論理的に分割します。このプロパティを使用するには、プロバイダーが必要な機能をサポートしている必要があります。

**AbsolutePage** プロパティを取得または設定する際には、ADO により [AbsolutePosition](absoluteposition-property-ado.md) プロパティと [PageSize](pagesize-property-ado.md) プロパティが以下のように組み合わせて使用されます。

- **AbsolutePage** を取得する場合、ADO はまず **AbsolutePosition** の値を取得し、それを **PageSize** で割ります。

- **AbsolutePage** を設定する場合、ADO は、 **PageSize** に新しい **AbsolutePage** 値を掛けてからその値に 1 を加えることにより、 **AbsolutePosition** を移動します。 その結果、 **AbsolutePage**が正常に設定された後の**Recordset**内の現在の位置は、そのページの最初のレコードになります。

**AbsolutePage** は、 **AbsolutePosition** プロパティと同じく 1 から始まる値で、 **Recordset** の先頭レコードがカレント レコードの場合に 1 になります。このプロパティを設定すると、特定のページの先頭レコードへと移動します。総ページ数は、 **PageCount** プロパティから取得できます。

