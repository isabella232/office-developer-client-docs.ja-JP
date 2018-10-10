---
title: Connection オブジェクト (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bba06d593069051d2cc4f2e66b8cb91f36d920fb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477009"
---
# <a name="connection-object-dao"></a>Connection オブジェクト (DAO)


**適用されます**Access 2013 |。Office 2013


> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>



**Connection** オブジェクトは、ODBC データベースへの接続を表します (ODBCDirect ワークスペースのみ)。

## <a name="remarks"></a>注釈

**Connection** は、リモート データベースへの接続を表す持続的でないオブジェクトです。**Connection** オブジェクトは、ODBCDirect ワークスペース (つまり種類を表すオプションを **dbUseODBC** に設定して作成された **Workspace** オブジェクト) でのみ使用できます。


> [!NOTE]
> <P>[!メモ] 下位互換性を維持するために、以前のバージョンの DAO 向けに記述されたコードは <STRONG>Database</STRONG> オブジェクトを引き続き使用できますが、 <STRONG>Connection</STRONG> の新しい機能を使用するには、 <STRONG>Connection</STRONG> オブジェクトを使用するコードを変更する必要があります。 <STRONG>Database</STRONG> オブジェクトの <STRONG>Connection</STRONG> プロパティを確認して、 <A href="database-connection-property-dao.md">Database</A> からの <STRONG>Connection</STRONG> オブジェクトへの参照を取得すると、コードの変換に便利です。反対に、 <STRONG>Database</STRONG> オブジェクトへの参照を <STRONG>Connection</STRONG> オブジェクトの <STRONG>Database</STRONG> プロパティから取得することもできます。</P>


