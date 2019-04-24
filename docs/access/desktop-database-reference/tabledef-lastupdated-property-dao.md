---
title: テーブルの lastupdated プロパティ (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 994543132fb5323566bd876da066419d0986bd91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308415"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="4c9e3-102">テーブルの lastupdated プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="4c9e3-102">TableDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="4c9e3-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c9e3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4c9e3-104">オブジェクトに対して最後に行われた変更の日付と時刻を返します。</span><span class="sxs-lookup"><span data-stu-id="4c9e3-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="4c9e3-105">バリアント型 (**Variant**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4c9e3-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c9e3-106">構文</span><span class="sxs-lookup"><span data-stu-id="4c9e3-106">Syntax</span></span>

<span data-ttu-id="4c9e3-107">*式*。LastUpdated</span><span class="sxs-lookup"><span data-stu-id="4c9e3-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="4c9e3-108">\*式\***TableDef**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="4c9e3-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c9e3-109">注釈</span><span class="sxs-lookup"><span data-stu-id="4c9e3-109">Remarks</span></span>

<span data-ttu-id="4c9e3-p102">**DateCreated** プロパティと **LastUpdated** プロパティは、それぞれオブジェクトが作成された日時、最後に更新された日時を返します。マルチユーザー環境では、DateCreated プロパティと LastUpdated プロパティの設定値が異なることを避けるために、これらの設定をファイル サーバーから直接取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c9e3-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

