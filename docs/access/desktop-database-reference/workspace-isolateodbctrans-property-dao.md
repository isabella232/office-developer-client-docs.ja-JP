---
title: Workspace.IsolateODBCTrans プロパティ (DAO)
TOCTitle: IsolateODBCTrans Property
ms:assetid: f7a48358-870b-cad3-d4ef-e46b50428e12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836924(v=office.15)
ms:contentKeyID: 48548770
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8a2696dfabe609042c920b33b2a0f5fd696d9833
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476234"
---
# <a name="workspaceisolateodbctrans-property-dao"></a><span data-ttu-id="dd1dd-102">Workspace.IsolateODBCTrans プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="dd1dd-102">Workspace.IsolateODBCTrans Property (DAO)</span></span>


<span data-ttu-id="dd1dd-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd1dd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dd1dd-104">同じ Microsoft Access データベース エンジンに接続された ODBC データ ソースに関連する複数のトランザクションが分離されているかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="dd1dd-104">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd1dd-105">構文</span><span class="sxs-lookup"><span data-stu-id="dd1dd-105">Syntax</span></span>

<span data-ttu-id="dd1dd-106">*式*です。IsolateODBCTrans</span><span class="sxs-lookup"><span data-stu-id="dd1dd-106">*expression* .IsolateODBCTrans</span></span>

<span data-ttu-id="dd1dd-107">\*式\***ワークスペース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="dd1dd-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd1dd-108">注釈</span><span class="sxs-lookup"><span data-stu-id="dd1dd-108">Remarks</span></span>

<span data-ttu-id="dd1dd-p101">状況によっては、同じ ODBC 接続上で同時に発生する複数のトランザクションを保留状態にする必要があります。これを行うには、それぞれのトランザクションに対して別々の **Workspace** オブジェクトを開く必要があります。各 **Workspace** オブジェクトがデータベースに対して独自の ODBC 接続を確立できますが、これによりシステムのパフォーマンスが低下します。通常、トランザクションの分離は不要であるため、同じユーザーが開いた複数の **Workspace** オブジェクトからの ODBC 接続は、既定で共有されます。</span><span class="sxs-lookup"><span data-stu-id="dd1dd-p101">In some situations, you need to have multiple simultaneous transactions pending on the same ODBC connection. To do this, you need to open a separate **Workspace** for each transaction. Although each **Workspace** can have its own ODBC connection to the database, this slows system performance. Because transaction isolation isn't usually required, ODBC connections from multiple **Workspace** objects opened by the same user are shared by default.</span></span>

<span data-ttu-id="dd1dd-p102">Microsoft SQL Server などの一部の ODBC サーバーでは、単一の接続における複数のトランザクションの同時発生は許可されていません。このようなデータベースに対して同時に複数のトランザクションを保留状態にする必要がある場合は、各 **Workspace** オブジェクトを開いた直後に、その **IsolateODBCTrans** プロパティを **True** に設定します。これにより、各 **Workspace** オブジェクトの ODBC 接続が別々に確立されます。</span><span class="sxs-lookup"><span data-stu-id="dd1dd-p102">Some ODBC servers, such as Microsoft SQL Server, don't allow simultaneous transactions on a single connection. If you need to have more than one transaction at a time pending against such a database, set the **IsolateODBCTrans** property to **True** on each **Workspace** as soon as you open it. This forces a separate ODBC connection for each **Workspace**.</span></span>

