---
title: WITH OWNERACCESS OPTION 宣言 (Microsoft Access SQL)
TOCTitle: WITH OWNERACCESS OPTION declaration (Microsoft Access SQL)
ms:assetid: 82e51071-12b2-e97e-07b4-27ffceda831e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196724(v=office.15)
ms:contentKeyID: 48545993
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277584
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 70420fd67047e2473e1e298dac75085915d83e3e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585033"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a>WITH OWNERACCESS OPTION 宣言 (Microsoft Access SQL)


**適用先:** Access 2013、Office 2013

セキュリティで保護されたワークグループを使用したマルチユーザー環境で、クエリを使用するユーザーにクエリの所有者と同等の権限を与える場合に使用します。

## <a name="syntax"></a>構文

*sqlstatement* OWNERACCESS オプションを使用する

## <a name="remarks"></a>注釈

WITH OWNERACCESS OPTION 宣言は省略可能です。

次の例は、Payroll テーブルの表示権限を持っているユーザーが作成したクエリで、その権限を持っていないユーザーでも給与情報を見ることができるようにするものです。

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

WITH OWNERACCESS OPTION 宣言を使用すると、テーブルの作成や追加の権限を持っていないユーザーでも、テーブル作成クエリや追加クエリを実行できるようになります。

ワークグループのセキュリティ設定とユーザー権限を適用する必要がある場合は、WITH OWNERACCESS OPTION 宣言を使用しないでください。

この宣言を使用するには、データベースに関連付けられたシステム データベース (System.mdw) へのアクセス権を持っていることが必要です。この宣言は、セキュリティで保護されたマルチユーザー環境でのみ有効です。

