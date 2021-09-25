---
title: URL プロパティ (RDS - Access デスクトップ データベース リファレンス)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c05bf1051a6c84d40225af8799c9ab2a4486331e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576829"
---
# <a name="url-property-rds"></a>URL プロパティ (RDS)

**適用先:** Access 2013、Office 2013

相対 URL または絶対 URL を格納する文字列を示します。

**URL** プロパティは、デザイン時に [DataControl](datacontrol-object-rds.md) オブジェクトの OBJECT タグで設定するか、実行時にスクリプト コードで設定できます。

## <a name="syntax"></a>構文

設計時間: \<PARAM NAME="URL" VALUE="Server"\>

実行時: DataControl.URL="Server"

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Server* |有効な URL を格納する文字列型 ( **String** ) の値。|
|*DataControl* |**DataControl** オブジェクトを表すオブジェクト変数。|

## <a name="remarks"></a>注釈

通常、URL は、[Recordset](recordset-object-ado.md) を生成して返すことができる Active Server Page (.asp) ファイルを示します。したがって、サーバー側 **DataFactory** オブジェクトを呼び出したり、カスタム ビジネス オブジェクトをプログラムしたりしなくても、 [Recordset](datafactory-object-rdsserver.md) を取得できます。

**URL** プロパティが設定されている場合、 [SubmitChanges](submitchanges-method-rds.md) は URL で指定された場所に変更を送信します。

