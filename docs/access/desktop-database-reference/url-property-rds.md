---
title: URL プロパティ (RDS のデスクトップのデータベース参照のアクセス)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca1fdba5e5fd9b16b66fd71f2841890870de4d65
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925983"
---
# <a name="url-property-rds"></a>URL プロパティ (RDS)


**適用されます**Access 2013、Office 2013。



相対 URL または絶対 URL を格納する文字列を示します。

**URL** プロパティは、デザイン時に [DataControl](datacontrol-object-rds.md) オブジェクトの OBJECT タグで設定するか、実行時にスクリプト コードで設定できます。

## <a name="syntax"></a>構文

デザイン時:\<パラメーター名"URL"の値を = ="Server"\>

実行時間: DataControl.URL="Server]

## <a name="parameters"></a>パラメーター

  - *Server*

  - 有効な URL を格納する文字列型 ( **String** ) の値。

  - *DataControl*

  - **DataControl** オブジェクトを表すオブジェクト変数。

## <a name="remarks"></a>解説

通常、URL は、[Recordset](recordset-object-ado.md) を生成して返すことができる Active Server Page (.asp) ファイルを示します。したがって、サーバー側 **DataFactory** オブジェクトを呼び出したり、カスタム ビジネス オブジェクトをプログラムしたりしなくても、 [Recordset](datafactory-object-rdsserver.md) を取得できます。

**URL** プロパティが設定されている場合、 [SubmitChanges](submitchanges-method-rds.md) は URL で指定された場所に変更を送信します。

