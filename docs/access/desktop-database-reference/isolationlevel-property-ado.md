---
title: IsolationLevel プロパティ (ADO)
TOCTitle: IsolationLevel property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76978d33fc5f82c9b1f8137b64a663e7e95f2204
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883058"
---
# <a name="isolationlevel-property-ado"></a>IsolationLevel プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Connection](connection-object-ado.md) オブジェクトの分離レベルを示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

[IsolationLevelEnum](isolationlevelenum.md) の値を設定または取得します。既定値は **adXactChaos** です。

## <a name="remarks"></a>解説

**IsolationLevel** プロパティでは、 **Connection** オブジェクトの分離レベルを設定します。設定値は、次に [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) メソッドを呼び出すまで有効になりません。要求した分離レベルを使用できない場合、プロバイダーはその次に高い分離レベルを返します。

**IsolationLevel** プロパティは読み取り/書き込み可能です。

**リモート データ サービスの使用法**クライアント側の Connection オブジェクトで使用すると、 **IsolationLevel**プロパティは**adXactUnspecified**にのみ設定できます。

ユーザーは、クライアント側のキャッシュ上の接続されていない **Recordset** オブジェクトで作業するため、マルチユーザーの場合は問題になることがあります。たとえば、2 人のユーザーが同じレコードを更新しようとした際、リモート データ サービスは単純に先に操作を行ったユーザーの更新を受け付けます。2 番目のユーザーの更新要求はエラーになって失敗します。

