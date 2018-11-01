---
title: Append メソッド (ADOX Tables)
TOCTitle: Append Method (ADOX Tables)
ms:assetid: 9e9fd57c-a856-6179-013f-9f378c3b7df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249726(v=office.15)
ms:contentKeyID: 48546664
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9191b35bea8d2e714716551c0bce62f86d250d32
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887216"
---
# <a name="append-method-adox-tables"></a><span data-ttu-id="2da13-102">Append メソッド (ADOX Tables)</span><span class="sxs-lookup"><span data-stu-id="2da13-102">Append Method (ADOX Tables)</span></span>


<span data-ttu-id="2da13-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2da13-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="2da13-104">新しい [Table](table-object-adox.md) オブジェクトを [Tables](tables-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="2da13-104">Adds a new [Table](table-object-adox.md) object to the [Tables](tables-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da13-105">構文</span><span class="sxs-lookup"><span data-stu-id="2da13-105">Syntax</span></span>

<span data-ttu-id="2da13-106">*テーブル*です。*テーブル*を追加します。</span><span class="sxs-lookup"><span data-stu-id="2da13-106">*Tables*.Append*Table*</span></span>

## <a name="parameters"></a><span data-ttu-id="2da13-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2da13-107">Parameters</span></span>

  - <span data-ttu-id="2da13-108">*Table*</span><span class="sxs-lookup"><span data-stu-id="2da13-108">*Table*</span></span>

  - <span data-ttu-id="2da13-109">追加する **Table** への参照を含むバリアント型 ( **Variant** ) の値、または作成して追加するテーブルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="2da13-109">A **Variant** value that contains a reference to the **Table** to append or the name of the table to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="2da13-110">解説</span><span class="sxs-lookup"><span data-stu-id="2da13-110">Remarks</span></span>

<span data-ttu-id="2da13-111">プロバイダーがテーブルの作成をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2da13-111">An error will occur if the provider does not support creating tables.</span></span>

