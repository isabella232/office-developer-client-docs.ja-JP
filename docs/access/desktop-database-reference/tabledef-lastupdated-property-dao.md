---
title: TableDef.LastUpdated プロパティ (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10d0203bd30c2e03f7cd2aaa761ac1cf76b12f94
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870864"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="9b45c-102">TableDef.LastUpdated プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="9b45c-102">TableDef.LastUpdated Property (DAO)</span></span>


<span data-ttu-id="9b45c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9b45c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b45c-p101">オブジェクトに対して行われた最新の変更の日付と時刻を取得します。値の取得のみ可能です。バリアント型 ( **Variant**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9b45c-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b45c-106">構文</span><span class="sxs-lookup"><span data-stu-id="9b45c-106">Syntax</span></span>

<span data-ttu-id="9b45c-107">*式*です。LastUpdated</span><span class="sxs-lookup"><span data-stu-id="9b45c-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="9b45c-108">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="9b45c-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b45c-109">注釈</span><span class="sxs-lookup"><span data-stu-id="9b45c-109">Remarks</span></span>

<span data-ttu-id="9b45c-p102">**DateCreated** プロパティおよび **LastUpdated** プロパティは、オブジェクトが作成された日付および時刻、または最後に更新された日付および時刻を取得します。マルチユーザー環境では、ユーザーがファイル サーバーから直接これらの設定を取得し、DateCreated プロパティおよび LastUpdated プロパティの設定値が一致しなくなるのを防ぐ必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b45c-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

