---
title: WITH OWNERACCESS OPTION 宣言 (Microsoft Access SQL)
TOCTitle: WITH OWNERACCESS OPTION Declaration (Microsoft Access SQL)
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
ms.openlocfilehash: 0ef07e29258035486a89e1b2cc19519d3f2f7c9f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889967"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a><span data-ttu-id="286ff-102">WITH OWNERACCESS OPTION 宣言 (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="286ff-102">WITH OWNERACCESS OPTION Declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="286ff-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="286ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="286ff-104">セキュリティで保護されたワークグループを使用したマルチユーザー環境で、クエリを使用するユーザーにクエリの所有者と同等の権限を与える場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="286ff-104">In a multiuser environment with a secure workgroup, use this declaration with a query to give the user who runs the query the same permissions as the query's owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="286ff-105">構文</span><span class="sxs-lookup"><span data-stu-id="286ff-105">Syntax</span></span>

<span data-ttu-id="286ff-106">*連結*OWNERACCESS オプションを使用して</span><span class="sxs-lookup"><span data-stu-id="286ff-106">*sqlstatement* WITH OWNERACCESS OPTION</span></span>

## <a name="remarks"></a><span data-ttu-id="286ff-107">解説</span><span class="sxs-lookup"><span data-stu-id="286ff-107">Remarks</span></span>

<span data-ttu-id="286ff-108">WITH OWNERACCESS OPTION 宣言は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="286ff-108">The WITH OWNERACCESS OPTION declaration is optional.</span></span>

<span data-ttu-id="286ff-109">次の例は、Payroll テーブルの表示権限を持っているユーザーが作成したクエリで、その権限を持っていないユーザーでも給与情報を見ることができるようにするものです。</span><span class="sxs-lookup"><span data-stu-id="286ff-109">The following example enables the user to view salary information (even if the user does not otherwise have permission to view the Payroll table), provided that the query's owner does have that permission:</span></span>

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

<span data-ttu-id="286ff-110">WITH OWNERACCESS OPTION 宣言を使用すると、テーブルの作成や追加の権限を持っていないユーザーでも、テーブル作成クエリや追加クエリを実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="286ff-110">If a user is otherwise prevented from creating or adding to a table, you can use WITH OWNERACCESS OPTION to enable the user to run a make-table or append query.</span></span>

<span data-ttu-id="286ff-111">ワークグループのセキュリティ設定とユーザー権限を適用する必要がある場合は、WITH OWNERACCESS OPTION 宣言を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="286ff-111">If you want to enforce workgroup security settings and users' permissions, do not include the WITH OWNERACCESS OPTION declaration.</span></span>

<span data-ttu-id="286ff-p101">この宣言を使用するには、データベースに関連付けられたシステム データベース (System.mdw) へのアクセス権を持っていることが必要です。この宣言は、セキュリティで保護されたマルチユーザー環境でのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="286ff-p101">This option requires you to have access to the System.mdw file associated with the database. It is useful only in secured multiuser implementations.</span></span>

