---
title: Connection プロパティ (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77d9bfa30dbfab21fd75de36b336a25e6af3187e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294996"
---
# <a name="databaseconnection-property-dao"></a><span data-ttu-id="dcc26-102">Connection プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="dcc26-102">Database.Connection property (DAO)</span></span>


<span data-ttu-id="dcc26-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="dcc26-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc26-104">構文</span><span class="sxs-lookup"><span data-stu-id="dcc26-104">Syntax</span></span>

<span data-ttu-id="dcc26-105">*式*。接続</span><span class="sxs-lookup"><span data-stu-id="dcc26-105">*expression* .Connection</span></span>

<span data-ttu-id="dcc26-106">\*式\***Database**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="dcc26-106">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcc26-107">注釈</span><span class="sxs-lookup"><span data-stu-id="dcc26-107">Remarks</span></span>

<span data-ttu-id="dcc26-108">**Connection** プロパティを使用して、**Database** に対応する **Connection** オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="dcc26-108">Use the **Connection** property to obtain a reference to a **Connection** object that corresponds to the **Database**.</span></span> <span data-ttu-id="dcc26-109">DAO では、**Connection** オブジェクトとそれに対応する **Database** オブジェクトは、同じオブジェクトへの 2 つの異なるオブジェクト変数参照です。</span><span class="sxs-lookup"><span data-stu-id="dcc26-109">In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object.</span></span> <span data-ttu-id="dcc26-110">**connection**オブジェクトの**[database](connection-database-property-dao.md)** プロパティと**database**オブジェクトの**connection**プロパティを使用すると、Microsoft access データベースエンジンを使用して ODBCDirect を使用することで、ODBC データソースへの接続を簡単に変更できます。</span><span class="sxs-lookup"><span data-stu-id="dcc26-110">The **[Database](connection-database-property-dao.md)** property of a **Connection** object and the **Connection** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

