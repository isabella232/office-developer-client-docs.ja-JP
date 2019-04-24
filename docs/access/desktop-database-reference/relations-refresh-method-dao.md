---
title: Refresh メソッド (DAO)
TOCTitle: Refresh Method
ms:assetid: d71cecf2-da90-5f62-9e51-f994e660ad34
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835058(v=office.15)
ms:contentKeyID: 48547997
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9da7cdcead4f5143674f4b46f4a57d5c32dc62fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306770"
---
# <a name="relationsrefresh-method-dao"></a><span data-ttu-id="9b170-102">Refresh メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="9b170-102">Relations.Refresh method (DAO)</span></span>


<span data-ttu-id="9b170-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b170-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b170-104">指定されたコレクション内のオブジェクトを更新して、データベースの現在のスキーマを反映させます。</span><span class="sxs-lookup"><span data-stu-id="9b170-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b170-105">構文</span><span class="sxs-lookup"><span data-stu-id="9b170-105">Syntax</span></span>

<span data-ttu-id="9b170-106">*式*。更新</span><span class="sxs-lookup"><span data-stu-id="9b170-106">*expression* .Refresh</span></span>

<span data-ttu-id="9b170-107">\*式\***Relations**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="9b170-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b170-108">注釈</span><span class="sxs-lookup"><span data-stu-id="9b170-108">Remarks</span></span>

<span data-ttu-id="9b170-p101">**Refresh** メソッドは、他のユーザーがデータベースを変更する可能性のあるマルチユーザー環境で使用します。データベースに対する変更によって間接的に影響を受けるコレクションで、このメソッドを使用する必要があることもあります。たとえば、 **Users** コレクションを変更した場合は、 **Groups** コレクションを使用する前に **Groups** コレクションを更新する必要があることがあります。</span><span class="sxs-lookup"><span data-stu-id="9b170-p101">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="9b170-p102">コレクションのオブジェクトはそのコレクションが最初に参照されたときに設定され、それ以降に他のユーザーが行った変更は自動的には反映されません。他のユーザーがコレクションを変更した可能性がある場合は、コレクション内に特定のオブジェクトが存在する (または存在しない) ことを前提とするタスクをアプリケーションで実行する直前に、コレクションの Refresh メソッドを使用してください。これにより、コレクションを最新の状態にしておくことができます。一方、Refresh を使用すると、パフォーマンスが必要以上に低下する場合があります。</span><span class="sxs-lookup"><span data-stu-id="9b170-p102">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

