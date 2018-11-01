---
title: Connection オブジェクト (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7170a28cb1d3ec9c8cdeca9229c255f264b9422e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883429"
---
# <a name="connection-object-dao"></a><span data-ttu-id="70b29-102">Connection オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="70b29-102">Connection Object (DAO)</span></span>


<span data-ttu-id="70b29-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="70b29-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="70b29-p101">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="70b29-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>



<span data-ttu-id="70b29-106">**Connection** オブジェクトは、ODBC データベースへの接続を表します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="70b29-106">A **Connection** object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="70b29-107">注釈</span><span class="sxs-lookup"><span data-stu-id="70b29-107">Remarks</span></span>

<span data-ttu-id="70b29-p102">**Connection** は、リモート データベースへの接続を表す持続的でないオブジェクトです。**Connection** オブジェクトは、ODBCDirect ワークスペース (つまり種類を表すオプションを **dbUseODBC** に設定して作成された **Workspace** オブジェクト) でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="70b29-p102">A **Connection** is a non-persistent object that represents a connection to a remote database. The **Connection** object is only available in ODBCDirect workspaces (that is, a **Workspace** object created with the type option set to **dbUseODBC**).</span></span>


> [!NOTE]
> <span data-ttu-id="70b29-p103">[!メモ] 下位互換性を維持するために、以前のバージョンの DAO 向けに記述されたコードは **Database** オブジェクトを引き続き使用できますが、 **Connection** の新しい機能を使用するには、 **Connection** オブジェクトを使用するコードを変更する必要があります。 **Database** オブジェクトの **Connection** プロパティを確認して、 [Database](database-connection-property-dao.md) からの **Connection** オブジェクトへの参照を取得すると、コードの変換に便利です。反対に、 **Database** オブジェクトへの参照を **Connection** オブジェクトの **Database** プロパティから取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="70b29-p103">Code written for earlier versions of DAO can continue to use the **Database** object for backward compatibility, but if the new features of a **Connection** are desired, you should revise code to use the **Connection** object. To help with code conversion, you can obtain a **Connection** object reference from a **Database** by reading the [Connection](database-connection-property-dao.md) property of the **Database** object. Conversely, you can obtain a **Database** object reference from the **Connection** object's **Database** property.</span></span>


