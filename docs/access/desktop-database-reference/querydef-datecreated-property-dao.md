---
title: QueryDef.DateCreated プロパティ (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d770decd0bf023a9c2ad8699a8aca4686d73491
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875414"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="21875-102">QueryDef.DateCreated プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="21875-102">QueryDef.DateCreated Property (DAO)</span></span>


<span data-ttu-id="21875-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="21875-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21875-p101">オブジェクトを作成した日付と時刻を取得します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。バリアント型 ( **Variant**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="21875-p101">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="21875-106">構文</span><span class="sxs-lookup"><span data-stu-id="21875-106">Syntax</span></span>

<span data-ttu-id="21875-107">*式*です。作成日時</span><span class="sxs-lookup"><span data-stu-id="21875-107">*expression* .DateCreated</span></span>

<span data-ttu-id="21875-108">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="21875-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="21875-109">注釈</span><span class="sxs-lookup"><span data-stu-id="21875-109">Remarks</span></span>

<span data-ttu-id="21875-p102">**DateCreated** プロパティおよび **LastUpdated** プロパティは、オブジェクトが作成された日付および時刻、または最後に更新された日付および時刻を取得します。マルチユーザー環境では、ユーザーがファイル サーバーから直接これらの設定を取得し、DateCreated プロパティおよび LastUpdated プロパティの設定値が一致しなくなるのを防ぐ必要があります。</span><span class="sxs-lookup"><span data-stu-id="21875-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

