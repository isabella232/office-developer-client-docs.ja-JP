---
title: ConnectionTimeout プロパティ (ADO)
TOCTitle: ConnectionTimeout property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 80b632ebe3f0181dc38de120ef7bf41caeab6e1f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589940"
---
# <a name="connectiontimeout-property-ado"></a>ConnectionTimeout プロパティ (ADO)


**適用先**: Access 2013、Office 2013

接続操作を中止して、エラーを生成するまでの待機時間を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

接続が開くまでの待機時間を秒単位で示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 15 です。

## <a name="remarks"></a>注釈

ネットワーク トラフィックやサーバーの過度の使用が原因で接続を開く試みを中止する必要がある場合は、**Connection** オブジェクトで [ConnectionTimeout](connection-object-ado.md) プロパティを使用します。接続が開かれる前に **ConnectionTimeout** プロパティで設定した時間が経過した場合は、エラーが発生して接続の試みが取り消されます。このプロパティを 0 に設定した場合は、ADO は接続が開かれるまで無限に待機します。コードを書き込むプロバイダーが、 **ConnectionTimeout** 機能をサポートしていることを確認してください。

**ConnectionTimeout** プロパティは、接続が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。

