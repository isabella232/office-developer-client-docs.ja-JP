---
title: Errors.Refresh メソッド (DAO)
TOCTitle: Refresh Method
ms:assetid: dc352c5f-09d0-bfb3-b24a-4c3454dbf5aa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835359(v=office.15)
ms:contentKeyID: 48548127
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c01dc4400593853daa4f2f82597d20032c3517dc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924576"
---
# <a name="errorsrefresh-method-dao"></a><span data-ttu-id="41460-102">Errors.Refresh メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="41460-102">Errors.Refresh method (DAO)</span></span>


<span data-ttu-id="41460-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="41460-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="41460-104">指定されたコレクション内のオブジェクトを更新して、データベースの現在のスキーマを反映させます。</span><span class="sxs-lookup"><span data-stu-id="41460-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="41460-105">構文</span><span class="sxs-lookup"><span data-stu-id="41460-105">Syntax</span></span>

<span data-ttu-id="41460-106">*式*です。更新</span><span class="sxs-lookup"><span data-stu-id="41460-106">*expression* .Refresh</span></span>

<span data-ttu-id="41460-107">\*式\***エラー**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="41460-107">*expression* A variable that represents an **Errors** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="41460-108">注釈</span><span class="sxs-lookup"><span data-stu-id="41460-108">Remarks</span></span>

<span data-ttu-id="41460-p101">**Refresh** メソッドは、マルチユーザー環境で、他のユーザーがデータベースを変更する可能性がある場合に使用します。このメソッドは、データベースに対する変更によって間接的に影響を受けるコレクションでも使用する必要がある場合があります。たとえば、 **Users** コレクションを変更した場合は、 **Groups** コレクションを使用する前に、その **Groups** コレクションを変更する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="41460-p101">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="41460-p102">コレクション内のオブジェクトは、そのコレクションが最初に参照されたときに格納され、それ以降に他のユーザーが加えた変更が自動的に反映されることはありません。他のユーザーがコレクションを変更した可能性が高い場合は、そのコレクション内の特定のオブジェクトが存在すること、または存在しないことを仮定したタスクをアプリケーションで実行する直前に、そのコレクションで Refresh メソッドを使用します。これにより、そのコレクションを最新の状態にしておくことができます。一方で、Refresh を使用すると、パフォーマンスが必要以上に低下する場合があります。</span><span class="sxs-lookup"><span data-stu-id="41460-p102">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

