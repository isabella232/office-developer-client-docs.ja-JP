---
title: Database.Connection プロパティ (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9aecffc135ab402f02b8fd4e1cc234f4a6eb37d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927327"
---
# <a name="databaseconnection-property-dao"></a><span data-ttu-id="f1956-102">Database.Connection プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="f1956-102">Database.Connection property (DAO)</span></span>


<span data-ttu-id="f1956-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f1956-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="f1956-104">構文</span><span class="sxs-lookup"><span data-stu-id="f1956-104">Syntax</span></span>

<span data-ttu-id="f1956-105">*式*です。接続</span><span class="sxs-lookup"><span data-stu-id="f1956-105">*expression* .Connection</span></span>

<span data-ttu-id="f1956-106">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="f1956-106">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1956-107">注釈</span><span class="sxs-lookup"><span data-stu-id="f1956-107">Remarks</span></span>

<span data-ttu-id="f1956-p101">**Connection** プロパティを使用して、 **Database** に対応する **Connection** オブジェクトへの参照を取得します。DAO では、 **Connection** オブジェクトとそれに対応する **Database** オブジェクトは、同じオブジェクトへの 2 つの異なるオブジェクト変数参照です。 [Connection](connection-database-property-dao.md) オブジェクトの \*\*\*\*Database\*\*\*\* プロパティと **Database** オブジェクトの **Connection** プロパティを利用すると、Microsoft Office Access データベース エンジンを介した ODBC データ ソースへの接続を変更して ODBCDirect を使用することが容易になります。</span><span class="sxs-lookup"><span data-stu-id="f1956-p101">Use the **Connection** property to obtain a reference to a **Connection** object that corresponds to the **Database**. In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object. The **[Database](connection-database-property-dao.md)** property of a **Connection** object and the **Connection** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

