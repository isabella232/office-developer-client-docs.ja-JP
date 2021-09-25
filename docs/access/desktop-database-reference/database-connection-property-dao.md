---
title: Database.Connection プロパティ (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4bf01881184347f5a9d1f36cb0c4b997fb5baf38
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585950"
---
# <a name="databaseconnection-property-dao"></a>Database.Connection プロパティ (DAO)


**適用先**: Access 2013、Office 2013

## <a name="syntax"></a>構文

*式* .接続

*式* **Database** オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Connection** プロパティを使用して、**Database** に対応する **Connection** オブジェクトへの参照を取得します。DAO では、**Connection** オブジェクトとそれに対応する **Database** オブジェクトは、同じオブジェクトへの 2 つの異なるオブジェクト変数参照です。**Connection** オブジェクトの **[Database](connection-database-property-dao.md)** プロパティと **Database** オブジェクトの **Connection** プロパティを利用すると、Microsoft Office Access データベース エンジンを介した ODBC データ ソースへの接続を変更して ODBCDirect を使用することが容易になります。

