---
title: Refresh メソッド (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6050e2d0b97421bda7a2914f068db4019459ee7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306315"
---
# <a name="tabledefsrefresh-method-dao"></a><span data-ttu-id="8e4ef-102">Refresh メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="8e4ef-102">TableDefs.Refresh method (DAO)</span></span>


<span data-ttu-id="8e4ef-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e4ef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e4ef-104">指定されたコレクション内のオブジェクトを更新して、データベースの現在のスキーマを反映させます。</span><span class="sxs-lookup"><span data-stu-id="8e4ef-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e4ef-105">構文</span><span class="sxs-lookup"><span data-stu-id="8e4ef-105">Syntax</span></span>

<span data-ttu-id="8e4ef-106">*式*。更新</span><span class="sxs-lookup"><span data-stu-id="8e4ef-106">*expression* .Refresh</span></span>

<span data-ttu-id="8e4ef-107">\*式\***テーブル定義**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="8e4ef-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e4ef-108">注釈</span><span class="sxs-lookup"><span data-stu-id="8e4ef-108">Remarks</span></span>

<span data-ttu-id="8e4ef-p101">Microsoft Access データベース エンジンで **QueryDef**、 **Recordset**、または **TableDef** の各オブジェクトの **Fields** コレクションに含まれる **Field** オブジェクトに使用される場所を確認するには、各 **Field** オブジェクトの **OrdinalPosition** プロパティを使用します。 **Field** オブジェクトの **OrdinalPosition** プロパティを変更しても、 **Refresh** メソッドを使用しない限り、コレクションにおける **Field** オブジェクトの順序は変化しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="8e4ef-p101">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object. Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="8e4ef-p102">**Refresh** メソッドは、他のユーザーがデータベースを変更する可能性のあるマルチユーザー環境で使用します。データベースに対する変更によって間接的に影響を受けるコレクションで、このメソッドを使用する必要があることもあります。たとえば、 **Users** コレクションを変更した場合は、 **Groups** コレクションを使用する前に **Groups** コレクションを更新する必要があることがあります。</span><span class="sxs-lookup"><span data-stu-id="8e4ef-p102">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="8e4ef-p103">コレクションのオブジェクトはそのコレクションが最初に参照されたときに設定され、それ以降に他のユーザーが行った変更は自動的には反映されません。他のユーザーがコレクションを変更した可能性がある場合は、コレクション内に特定のオブジェクトが存在する (または存在しない) ことを前提とするタスクをアプリケーションで実行する直前に、コレクションの Refresh メソッドを使用してください。これにより、コレクションを最新の状態にしておくことができます。一方、Refresh を使用すると、パフォーマンスが必要以上に低下する場合があります。</span><span class="sxs-lookup"><span data-stu-id="8e4ef-p103">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

