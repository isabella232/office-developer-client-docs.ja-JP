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
# <a name="databaseconnection-property-dao"></a>Connection プロパティ (DAO)


**適用先:** Access 2013、Office 2013

## <a name="syntax"></a>構文

*式*。接続

*式***Database**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**Connection** プロパティを使用して、**Database** に対応する **Connection** オブジェクトへの参照を取得します。 DAO では、**Connection** オブジェクトとそれに対応する **Database** オブジェクトは、同じオブジェクトへの 2 つの異なるオブジェクト変数参照です。 **connection**オブジェクトの**[database](connection-database-property-dao.md)** プロパティと**database**オブジェクトの**connection**プロパティを使用すると、Microsoft access データベースエンジンを使用して ODBCDirect を使用することで、ODBC データソースへの接続を簡単に変更できます。

