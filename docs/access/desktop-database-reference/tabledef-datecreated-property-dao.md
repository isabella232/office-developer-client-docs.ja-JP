---
title: datecreated プロパティプロパティ (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5dc326b271e8444211bba0cd2d3c37c047ac205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314540"
---
# <a name="tabledefdatecreated-property-dao"></a><span data-ttu-id="3c80e-102">datecreated プロパティプロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="3c80e-102">TableDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="3c80e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c80e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c80e-104">オブジェクトが作成された日付と時刻を返します (Microsoft access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="3c80e-104">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="3c80e-105">バリアント型 (**Variant**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3c80e-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c80e-106">構文</span><span class="sxs-lookup"><span data-stu-id="3c80e-106">Syntax</span></span>

<span data-ttu-id="3c80e-107">*式*。datecreated プロパティ</span><span class="sxs-lookup"><span data-stu-id="3c80e-107">*expression* .DateCreated</span></span>

<span data-ttu-id="3c80e-108">\*式\***TableDef**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="3c80e-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c80e-109">注釈</span><span class="sxs-lookup"><span data-stu-id="3c80e-109">Remarks</span></span>

<span data-ttu-id="3c80e-p102">**DateCreated** プロパティと **LastUpdated** プロパティは、それぞれオブジェクトが作成された日時、最後に更新された日時を返します。マルチユーザー環境では、DateCreated プロパティと LastUpdated プロパティの設定値が異なることを避けるために、これらの設定をファイル サーバーから直接取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c80e-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

