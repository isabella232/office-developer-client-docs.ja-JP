---
title: IsolateODBCTrans プロパティ (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 781679dfbd4050cfde219802db4cd9e1544d83ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302514"
---
# <a name="workspaceisolateodbctrans-property-dao"></a>IsolateODBCTrans プロパティ (DAO)


**適用先:** Access 2013、Office 2013

同じ Microsoft Access データベース エンジンに接続された ODBC データ ソースに関連する複数のトランザクションが分離されているかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*。IsolateODBCTrans

*式***Workspace**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

状況によっては、同じ ODBC 接続上で同時に発生する複数のトランザクションを保留状態にする必要があります。これを行うには、それぞれのトランザクションに対して別々の **Workspace** オブジェクトを開く必要があります。各 **Workspace** オブジェクトがデータベースに対して独自の ODBC 接続を確立できますが、これによりシステムのパフォーマンスが低下します。通常、トランザクションの分離は不要であるため、同じユーザーが開いた複数の **Workspace** オブジェクトからの ODBC 接続は、既定で共有されます。

Microsoft SQL Server などの一部の ODBC サーバーでは、単一の接続における複数のトランザクションの同時発生は許可されていません。このようなデータベースに対して同時に複数のトランザクションを保留状態にする必要がある場合は、各 **Workspace** オブジェクトを開いた直後に、その **IsolateODBCTrans** プロパティを **True** に設定します。これにより、各 **Workspace** オブジェクトの ODBC 接続が別々に確立されます。

