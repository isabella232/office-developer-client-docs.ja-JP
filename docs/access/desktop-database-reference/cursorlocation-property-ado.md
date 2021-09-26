---
title: CursorLocation プロパティ (ADO)
TOCTitle: CursorLocation property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ff45fa942e7fc7852272969c4727875a6f032e83
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618337"
---
# <a name="cursorlocation-property-ado"></a>CursorLocation プロパティ (ADO)


**適用先**: Access 2013、Office 2013

カーソル サービスの場所を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

[CursorLocationEnum](cursorlocationenum.md) 値のいずれか 1 つに設定可能な長整数型 (**Long**) の値を設定または取得します。

## <a name="remarks"></a>注釈

このプロパティで、プロバイダーにアクセス可能なさまざまなカーソル ライブラリの中からカーソル サービスを選択します。通常は、クライアント側カーソル ライブラリ、またはサーバー側カーソル ライブラリから選択します。

このプロパティ設定は、プロパティが設定された後に確立された接続のみに作用します。 **CursorLocation** プロパティを変更しても既存の接続には影響しません。

[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) メソッドが返すカーソルは、この設定を継承します。 **Recordset** オブジェクトは、関連付けられた接続からこの設定を自動的に継承します。

このプロパティは、[Connection](connection-object-ado.md) または閉じている [Recordset](recordset-object-ado.md) 上では読み取り/書き込み可能ですが、開いている **Recordset** 上では読み取り専用になります。

**リモート データ サービスの使用状況** クライアント側の Recordset オブジェクトまたは **Connection** オブジェクト **で** 使用する場合 **、CursorLocation** プロパティは **adUseClient にのみ設定できます**。

