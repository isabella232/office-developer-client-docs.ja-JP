---
title: SubmitChanges メソッド (RDS)
TOCTitle: SubmitChanges Method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 521728af91967d673a1c69f4e4812b0aaa73ce59
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883884"
---
# <a name="submitchanges-method-rds"></a>SubmitChanges メソッド (RDS)


**適用されます**Access 2013、Office 2013。

ローカルにキャッシュされていて更新可能な [Recordset](recordset-object-ado.md) の保留中の変更を、 [Connect](connect-property-rds.md) プロパティまたは [URL](url-property-rds.md) プロパティで指定されているデータ ソースに送信します。

## <a name="syntax"></a>構文

*DataControl*。SubmitChanges

*DataFactory*。SubmitChanges*接続*、*レコード セット*

## <a name="parameters"></a>パラメーター

  - *DataControl*

  - [RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数。

  - *DataFactory*

  - [RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトを表すオブジェクト変数を指定します。

  - *Connection*

  - **RDS.DataControl** オブジェクトの **Connect** プロパティで作成された接続を表す文字列型 ( **String** ) の値。

  - *Recordset*

  - **Recordset** オブジェクトを表すオブジェクト変数です。

## <a name="remarks"></a>解説

[RDS.DataControl](connect-property-rds.md) オブジェクトで [SubmitChanges](server-property-rds.md) メソッドを使用するには、その前に [Connect](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) プロパティ、 **Server** プロパティ、および **SQL** プロパティを設定しておく必要があります。

[SubmitChanges](cancelupdate-method-rds.md) を呼び出した後に同じ **Recordset** オブジェクトに対して **CancelUpdate** メソッドを呼び出しても、既に変更がコミットされているため、その **CancelUpdate** 呼び出しは失敗します。

変更を加えられたレコードだけが変更を反映させるために送信され、すべての変更が成功するか、またはすべてまとめて失敗します。

**SubmitChanges**は、*既定*の**RDSServer.DataFactory**オブジェクトでのみ使用できます。 カスタム ビジネス オブジェクトには、このメソッドは使用できません。

**URL** プロパティが設定されている場合、 **SubmitChanges** は、その URL で指定された場所に変更内容を送信します。

