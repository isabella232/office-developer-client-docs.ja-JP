---
title: Connection オブジェクト (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a8f324d7216eff2aeeb9045f5c506cdf37170f6
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863732"
---
# <a name="connection-object-dao"></a>Connection オブジェクト (DAO)


**適用されます**Access 2013 |。Office 2013

> [!NOTE]
> [!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。



**Connection** オブジェクトは、ODBC データベースへの接続を表します (ODBCDirect ワークスペースのみ)。

## <a name="remarks"></a>注釈

**Connection** は、リモート データベースへの接続を表す持続的でないオブジェクトです。**Connection** オブジェクトは、ODBCDirect ワークスペース (つまり種類を表すオプションを **dbUseODBC** に設定して作成された **Workspace** オブジェクト) でのみ使用できます。


> [!NOTE]
> [!メモ] 下位互換性を維持するために、以前のバージョンの DAO 向けに記述されたコードは **Database** オブジェクトを引き続き使用できますが、 **Connection** の新しい機能を使用するには、 **Connection** オブジェクトを使用するコードを変更する必要があります。 **Database** オブジェクトの **Connection** プロパティを確認して、 [Database](database-connection-property-dao.md) からの **Connection** オブジェクトへの参照を取得すると、コードの変換に便利です。反対に、 **Database** オブジェクトへの参照を **Connection** オブジェクトの **Database** プロパティから取得することもできます。


