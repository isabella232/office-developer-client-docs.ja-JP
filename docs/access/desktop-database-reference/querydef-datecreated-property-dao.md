---
title: datecreated プロパティプロパティ (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4a120eed6c20db73e1c23f31ea9329d00da2f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301072"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="6fb9a-102">datecreated プロパティプロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="6fb9a-102">QueryDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="6fb9a-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fb9a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6fb9a-104">オブジェクトが作成された日付と時刻を返します (Microsoft access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="6fb9a-104">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="6fb9a-105">バリアント型 (**Variant**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6fb9a-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fb9a-106">構文</span><span class="sxs-lookup"><span data-stu-id="6fb9a-106">Syntax</span></span>

<span data-ttu-id="6fb9a-107">*式*。datecreated プロパティ</span><span class="sxs-lookup"><span data-stu-id="6fb9a-107">*expression* .DateCreated</span></span>

<span data-ttu-id="6fb9a-108">\*式\***QueryDef**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="6fb9a-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fb9a-109">注釈</span><span class="sxs-lookup"><span data-stu-id="6fb9a-109">Remarks</span></span>

<span data-ttu-id="6fb9a-p102">**DateCreated** プロパティと **LastUpdated** プロパティは、それぞれオブジェクトが作成された日時、最後に更新された日時を返します。マルチユーザー環境では、DateCreated プロパティと LastUpdated プロパティの設定値が異なることを避けるために、これらの設定をファイル サーバーから直接取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fb9a-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

