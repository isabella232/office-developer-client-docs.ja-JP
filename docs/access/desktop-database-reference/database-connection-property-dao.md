---
title: Database.Connection プロパティ (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f0974051b1f10fa73caad6d9feafb2e2b769579
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882841"
---
# <a name="databaseconnection-property-dao"></a>Database.Connection プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

## <a name="syntax"></a>構文

*式*です。接続

*式***データベース**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Connection** プロパティを使用して、 **Database** に対応する **Connection** オブジェクトへの参照を取得します。DAO では、 **Connection** オブジェクトとそれに対応する **Database** オブジェクトは、同じオブジェクトへの 2 つの異なるオブジェクト変数参照です。 [Connection](connection-database-property-dao.md) オブジェクトの ****Database**** プロパティと **Database** オブジェクトの **Connection** プロパティを利用すると、Microsoft Office Access データベース エンジンを介した ODBC データ ソースへの接続を変更して ODBCDirect を使用することが容易になります。

