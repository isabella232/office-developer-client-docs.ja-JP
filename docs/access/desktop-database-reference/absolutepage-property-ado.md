---
title: AbsolutePage プロパティ (ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 15c4fe003acc3fbc76723c8d0dc271a75b5318d3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569665"
---
# <a name="absolutepage-property-ado"></a>AbsolutePage プロパティ (ADO)

**適用先:** Access 2013、Office 2013

カレント レコードがあるページを示します。

## <a name="settings-and-return-values"></a>設定および戻り値

[Recordset](recordset-object-ado.md)オブジェクト[(PageCount)](pagecount-property-ado.md)のページ数に 1 から長い値を設定または返します。または[PositionEnum](positionenum.md)値のいずれかを返します。 

## <a name="remarks"></a>注釈

このプロパティを使用すると、カレント レコードが置かれているページのページ番号を識別できます。このプロパティは、[PageSize](pagesize-property-ado.md) プロパティを使用して、各ページが **PageSize** と等しいレコード数を持つように (ただし最終ページのみ例外で、レコード数が少なくなる場合があります) **Recordset** オブジェクトの行セットの合計カウントを一連のページへと論理的に分割します。このプロパティを使用するには、プロバイダーが必要な機能をサポートしている必要があります。

**AbsolutePage** プロパティを取得または設定する際には、ADO により [AbsolutePosition](absoluteposition-property-ado.md) プロパティと [PageSize](pagesize-property-ado.md) プロパティが以下のように組み合わせて使用されます。

- **AbsolutePage** を取得する場合、ADO はまず **AbsolutePosition** の値を取得し、それを **PageSize** で割ります。

- **AbsolutePage** を設定する場合、ADO は、 **PageSize** に新しい **AbsolutePage** 値を掛けてからその値に 1 を加えることにより、 **AbsolutePosition** を移動します。 その結果、AbsolutePage を正常に設定した **後** の **Recordset** の現在の位置は、そのページの最初のレコードになります。

**AbsolutePage** は、 **AbsolutePosition** プロパティと同じく 1 から始まる値で、 **Recordset** の先頭レコードがカレント レコードの場合に 1 になります。このプロパティを設定すると、特定のページの先頭レコードへと移動します。総ページ数は、 **PageCount** プロパティから取得できます。

