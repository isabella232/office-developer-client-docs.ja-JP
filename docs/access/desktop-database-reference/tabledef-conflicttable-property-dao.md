---
title: TableDef.ConflictTable プロパティ (DAO)
TOCTitle: ConflictTable Property
ms:assetid: 0db8b975-eb6d-19c6-cfb7-6ce01230ebe4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845218(v=office.15)
ms:contentKeyID: 48543228
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053356
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0189a5163dd5e225ad34841264cf84e85785d7fb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718918"
---
# <a name="tabledefconflicttable-property-dao"></a><span data-ttu-id="9b68e-102">TableDef.ConflictTable プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="9b68e-102">TableDef.ConflictTable property (DAO)</span></span>


<span data-ttu-id="9b68e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9b68e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b68e-p101">2 つのレプリカの同期中に競合したデータベース レコードを含む競合テーブルの名前を返します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9b68e-p101">Returns the name of a conflict table containing the database records that conflicted during the synchronization of two replicas (Microsoft Access workspaces only). Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b68e-106">構文</span><span class="sxs-lookup"><span data-stu-id="9b68e-106">Syntax</span></span>

<span data-ttu-id="9b68e-107">*式*です。ConflictTable</span><span class="sxs-lookup"><span data-stu-id="9b68e-107">*expression* .ConflictTable</span></span>

<span data-ttu-id="9b68e-108">\*式\***テーブル定義**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="9b68e-108">*expression* An expression that returns a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b68e-109">注釈</span><span class="sxs-lookup"><span data-stu-id="9b68e-109">Remarks</span></span>

<span data-ttu-id="9b68e-110">競合テーブルがないか、またはデータベースがレプリカではない場合、戻り値は文字列型 ( **String**) の長さがゼロの文字列 ("") です。</span><span class="sxs-lookup"><span data-stu-id="9b68e-110">The return value is a **String** data type that is a zero-length string ("") if there is no conflict table or the database isn't a replica.</span></span>

<span data-ttu-id="9b68e-p102">2 つの別のレプリカで 2 人のユーザーがそれぞれデータベースの同じレコードを変更した場合、一方のユーザーが行った変更は、他方のレプリカには適用されません。したがって、変更に失敗したユーザーは競合を解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b68e-p102">If two users at two separate replicas each make a change to the same record in the database, the changes made by one user will fail to be applied to the other replica. Consequently, the user with the failed change must resolve the conflicts.</span></span>

<span data-ttu-id="9b68e-p103">競合は、フィールド間ではなくレコード レベルで発生します。たとえば、あるユーザーが "住所" フィールドを変更し、別のユーザーが同じレコードの "電話" フィールドを更新した場合、一方の変更は拒否されます。競合はレコード レベルで発生するため、正常に行われた変更および拒否された変更により、情報が競合する可能性が実際には低い場合でも、変更が拒否されます。</span><span class="sxs-lookup"><span data-stu-id="9b68e-p103">Conflicts occur at the record level, not between fields. For example, if one user changes the Address field and another updates the Phone field in the same record, then one change is rejected. Because conflicts occur at the record level, the rejection occurs even though the successful change and the rejected change are unlikely to result in a true conflict of information.</span></span>

<span data-ttu-id="9b68e-p104">同期メカニズムは、変更が正常に行われたらテーブルに配置されたはずの情報を含む競合テーブルを作成することで、レコードの競合を処理します。これらの競合テーブルを調べ、1 行ずつ作業し、適切になるように修正します。</span><span class="sxs-lookup"><span data-stu-id="9b68e-p104">The synchronization mechanism handles the record conflicts by creating conflict tables, which contain the information that would have been placed in the table, if the change had been successful. You can examine these conflict tables and work through them row by row, fixing whatever is appropriate.</span></span>

<span data-ttu-id="9b68e-118">すべての競合テーブルの名前は、テーブル\_テーブルは、最大のテーブル名の長さに切り詰められます、テーブルの元の名前の競合。</span><span class="sxs-lookup"><span data-stu-id="9b68e-118">All conflict tables are named table\_conflict, where table is the original name of the table, truncated to the maximum table name length.</span></span>

