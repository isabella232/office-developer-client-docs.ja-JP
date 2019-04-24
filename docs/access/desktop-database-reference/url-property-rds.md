---
title: URL プロパティ (RDS-Access デスクトップデータベースリファレンス)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aafc8cc10410cafed21e38ad7fec269c391c1fa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313399"
---
# <a name="url-property-rds"></a>URL プロパティ (RDS)

**適用先:** Access 2013、Office 2013

相対 URL または絶対 URL を格納する文字列を示します。

**URL** プロパティは、デザイン時に [DataControl](datacontrol-object-rds.md) オブジェクトの OBJECT タグで設定するか、実行時にスクリプト コードで設定できます。

## <a name="syntax"></a>構文

デザイン時: \<パラメーター名 = "URL" 値 = "Server"\>

実行時間: DataControl = "Server"

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Server* |有効な URL を格納する文字列型 ( **String** ) の値。|
|*DataControl* |**DataControl** オブジェクトを表すオブジェクト変数。|

## <a name="remarks"></a>注釈

通常、URL は、[Recordset](recordset-object-ado.md) を生成して返すことができる Active Server Page (.asp) ファイルを示します。したがって、サーバー側 **DataFactory** オブジェクトを呼び出したり、カスタム ビジネス オブジェクトをプログラムしたりしなくても、 [Recordset](datafactory-object-rdsserver.md) を取得できます。

**URL** プロパティが設定されている場合、 [SubmitChanges](submitchanges-method-rds.md) は URL で指定された場所に変更を送信します。

