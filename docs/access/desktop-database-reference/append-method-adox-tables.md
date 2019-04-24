---
title: Append メソッド (ADOX Tables)
TOCTitle: Append method (ADOX Tables)
ms:assetid: 9e9fd57c-a856-6179-013f-9f378c3b7df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249726(v=office.15)
ms:contentKeyID: 48546664
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d2bf2479c2a34291f245783ebaecd75ba31d2ac8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297075"
---
# <a name="append-method-adox-tables"></a><span data-ttu-id="82ad3-102">Append メソッド (ADOX Tables)</span><span class="sxs-lookup"><span data-stu-id="82ad3-102">Append method (ADOX Tables)</span></span>

<span data-ttu-id="82ad3-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="82ad3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82ad3-104">新しい [Table](table-object-adox.md) オブジェクトを [Tables](tables-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="82ad3-104">Adds a new [Table](table-object-adox.md) object to the [Tables](tables-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="82ad3-105">構文</span><span class="sxs-lookup"><span data-stu-id="82ad3-105">Syntax</span></span>

<span data-ttu-id="82ad3-106">*表\*\*テーブル*の追加</span><span class="sxs-lookup"><span data-stu-id="82ad3-106">*Tables*.Append*Table*</span></span>

## <a name="parameters"></a><span data-ttu-id="82ad3-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="82ad3-107">Parameters</span></span>

|<span data-ttu-id="82ad3-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="82ad3-108">Parameter</span></span>|<span data-ttu-id="82ad3-109">説明</span><span class="sxs-lookup"><span data-stu-id="82ad3-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="82ad3-110">*Table*</span><span class="sxs-lookup"><span data-stu-id="82ad3-110">*Table*</span></span> | <span data-ttu-id="82ad3-111">追加する **Table** への参照を含むバリアント型 ( **Variant** ) の値、または作成して追加するテーブルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="82ad3-111">A **Variant** value that contains a reference to the **Table** to append or the name of the table to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="82ad3-112">注釈</span><span class="sxs-lookup"><span data-stu-id="82ad3-112">Remarks</span></span>

<span data-ttu-id="82ad3-113">プロバイダーがテーブルの作成をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="82ad3-113">An error will occur if the provider does not support creating tables.</span></span>

