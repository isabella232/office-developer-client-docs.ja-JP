---
title: 接続オブジェクト (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 73ede9cae5246db3d802125b0f7c4e6df5347930
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716790"
---
# <a name="connection-object-dao"></a>接続オブジェクト (DAO)

**適用されます**Access 2013、Office 2013。

> [!NOTE]
> [!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。

**Connection** オブジェクトは、ODBC データベースへの接続を表します (ODBCDirect ワークスペースのみ)。

## <a name="remarks"></a>注釈

**Connection** は、リモート データベースへの接続を表す持続的でないオブジェクトです。**Connection** オブジェクトは、ODBCDirect ワークスペース (つまり種類を表すオプションを **dbUseODBC** に設定して作成された **Workspace** オブジェクト) でのみ使用できます。

> [!NOTE]
> [!メモ] 下位互換性を維持するために、以前のバージョンの DAO 向けに記述されたコードは **Database** オブジェクトを引き続き使用できますが、 **Connection** の新しい機能を使用するには、 **Connection** オブジェクトを使用するコードを変更する必要があります。 **Database** オブジェクトの **Connection** プロパティを確認して、 [Database](database-connection-property-dao.md) からの **Connection** オブジェクトへの参照を取得すると、コードの変換に便利です。反対に、 **Database** オブジェクトへの参照を **Connection** オブジェクトの **Database** プロパティから取得することもできます。


