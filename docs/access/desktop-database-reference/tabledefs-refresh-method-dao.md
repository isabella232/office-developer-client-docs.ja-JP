---
title: TableDefs.Refresh メソッド (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6050e2d0b97421bda7a2914f068db4019459ee7a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714494"
---
# <a name="tabledefsrefresh-method-dao"></a><span data-ttu-id="53e45-102">TableDefs.Refresh メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="53e45-102">TableDefs.Refresh method (DAO)</span></span>


<span data-ttu-id="53e45-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="53e45-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53e45-104">指定されたコレクション内のオブジェクトを更新して、データベースの現在のスキーマを反映させます。</span><span class="sxs-lookup"><span data-stu-id="53e45-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="53e45-105">構文</span><span class="sxs-lookup"><span data-stu-id="53e45-105">Syntax</span></span>

<span data-ttu-id="53e45-106">*式*です。更新</span><span class="sxs-lookup"><span data-stu-id="53e45-106">*expression* .Refresh</span></span>

<span data-ttu-id="53e45-107">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="53e45-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="53e45-108">注釈</span><span class="sxs-lookup"><span data-stu-id="53e45-108">Remarks</span></span>

<span data-ttu-id="53e45-p101">Microsoft Access データベース エンジンで **QueryDef**、 **Recordset**、または **TableDef** の各オブジェクトの **Fields** コレクションに含まれる **Field** オブジェクトに使用される場所を確認するには、各 **Field** オブジェクトの **OrdinalPosition** プロパティを使用します。 **Field** オブジェクトの **OrdinalPosition** プロパティを変更しても、 **Refresh** メソッドを使用しない限り、コレクションにおける **Field** オブジェクトの順序は変化しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="53e45-p101">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object. Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="53e45-p102">**Refresh** メソッドは、マルチユーザー環境で、他のユーザーがデータベースを変更する可能性がある場合に使用します。このメソッドは、データベースに対する変更によって間接的に影響を受けるコレクションでも使用する必要がある場合があります。たとえば、 **Users** コレクションを変更した場合は、 **Groups** コレクションを使用する前に、その **Groups** コレクションを変更する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="53e45-p102">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="53e45-p103">コレクション内のオブジェクトは、そのコレクションが最初に参照されたときに格納され、それ以降に他のユーザーが加えた変更が自動的に反映されることはありません。他のユーザーがコレクションを変更した可能性が高い場合は、そのコレクション内の特定のオブジェクトが存在すること、または存在しないことを仮定したタスクをアプリケーションで実行する直前に、そのコレクションで Refresh メソッドを使用します。これにより、そのコレクションを最新の状態にしておくことができます。一方で、Refresh を使用すると、パフォーマンスが必要以上に低下する場合があります。</span><span class="sxs-lookup"><span data-stu-id="53e45-p103">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

