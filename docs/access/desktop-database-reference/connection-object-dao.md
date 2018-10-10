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
# <a name="connection-object-dao"></a><span data-ttu-id="5de79-102">Connection オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="5de79-102">Connection Object (DAO)</span></span>


<span data-ttu-id="5de79-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5de79-103">**Applies to**: Access 2013 | Office 2013</span></span>


> [!NOTE]
> <P><span data-ttu-id="5de79-p101">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="5de79-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>



<span data-ttu-id="5de79-106">**Connection** オブジェクトは、ODBC データベースへの接続を表します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="5de79-106">A **Connection** object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="5de79-107">注釈</span><span class="sxs-lookup"><span data-stu-id="5de79-107">Remarks</span></span>

<span data-ttu-id="5de79-p102">**Connection** は、リモート データベースへの接続を表す持続的でないオブジェクトです。**Connection** オブジェクトは、ODBCDirect ワークスペース (つまり種類を表すオプションを **dbUseODBC** に設定して作成された **Workspace** オブジェクト) でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="5de79-p102">A **Connection** is a non-persistent object that represents a connection to a remote database. The **Connection** object is only available in ODBCDirect workspaces (that is, a **Workspace** object created with the type option set to **dbUseODBC**).</span></span>


> [!NOTE]
> <P><span data-ttu-id="5de79-p103">[!メモ] 下位互換性を維持するために、以前のバージョンの DAO 向けに記述されたコードは <STRONG>Database</STRONG> オブジェクトを引き続き使用できますが、 <STRONG>Connection</STRONG> の新しい機能を使用するには、 <STRONG>Connection</STRONG> オブジェクトを使用するコードを変更する必要があります。 <STRONG>Database</STRONG> オブジェクトの <STRONG>Connection</STRONG> プロパティを確認して、 <A href="database-connection-property-dao.md">Database</A> からの <STRONG>Connection</STRONG> オブジェクトへの参照を取得すると、コードの変換に便利です。反対に、 <STRONG>Database</STRONG> オブジェクトへの参照を <STRONG>Connection</STRONG> オブジェクトの <STRONG>Database</STRONG> プロパティから取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="5de79-p103">Code written for earlier versions of DAO can continue to use the <STRONG>Database</STRONG> object for backward compatibility, but if the new features of a <STRONG>Connection</STRONG> are desired, you should revise code to use the <STRONG>Connection</STRONG> object. To help with code conversion, you can obtain a <STRONG>Connection</STRONG> object reference from a <STRONG>Database</STRONG> by reading the <A href="database-connection-property-dao.md">Connection</A> property of the <STRONG>Database</STRONG> object. Conversely, you can obtain a <STRONG>Database</STRONG> object reference from the <STRONG>Connection</STRONG> object's <STRONG>Database</STRONG> property.</span></span></P>


