---
title: Errors.Count プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: ad135955-3b18-4f99-66d9-aff1492df13b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821719(v=office.15)
ms:contentKeyID: 48547028
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2cbbed2c7061b225d969dbd7554191e8db4a28a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707256"
---
# <a name="errorscount-property-dao"></a><span data-ttu-id="8c638-102">Errors.Count プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="8c638-102">Errors.Count property (DAO)</span></span>


<span data-ttu-id="8c638-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8c638-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c638-p101">指定したコレクション内のオブジェクトの数を取得します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="8c638-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c638-106">構文</span><span class="sxs-lookup"><span data-stu-id="8c638-106">Syntax</span></span>

<span data-ttu-id="8c638-107">*式*です。カウント</span><span class="sxs-lookup"><span data-stu-id="8c638-107">*expression* .Count</span></span>

<span data-ttu-id="8c638-108">*式*: **Errors** オブジェクトを表す変数。</span><span class="sxs-lookup"><span data-stu-id="8c638-108">*expression* A variable that represents an **Errors** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c638-109">注釈</span><span class="sxs-lookup"><span data-stu-id="8c638-109">Remarks</span></span>

<span data-ttu-id="8c638-p102">コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8c638-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="8c638-p103">**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。</span><span class="sxs-lookup"><span data-stu-id="8c638-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

