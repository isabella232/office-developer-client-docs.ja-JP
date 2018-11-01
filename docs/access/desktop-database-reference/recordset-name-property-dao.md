---
title: Recordset.Name プロパティ (DAO)
TOCTitle: Name Property
ms:assetid: 2a80b994-a135-cd61-3906-17dfa0580110
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192067(v=office.15)
ms:contentKeyID: 48543910
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e58b422165a1530a8ceb65298f0cac81d558c2a6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870227"
---
# <a name="recordsetname-property-dao"></a><span data-ttu-id="61ac0-102">Recordset.Name プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="61ac0-102">Recordset.Name Property (DAO)</span></span>


<span data-ttu-id="61ac0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="61ac0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="61ac0-p101">指定したオブジェクトの名前を取得します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="61ac0-p101">Returns the name of the specified object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="61ac0-106">構文</span><span class="sxs-lookup"><span data-stu-id="61ac0-106">Syntax</span></span>

<span data-ttu-id="61ac0-107">*式*です。名</span><span class="sxs-lookup"><span data-stu-id="61ac0-107">*expression* .Name</span></span>

<span data-ttu-id="61ac0-108">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="61ac0-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="61ac0-109">注釈</span><span class="sxs-lookup"><span data-stu-id="61ac0-109">Remarks</span></span>

<span data-ttu-id="61ac0-110">SQL ステートメントを使用して開いた **Recordset** オブジェクトの **Name** プロパティは、その SQL ステートメントの先頭 256 文字となります。</span><span class="sxs-lookup"><span data-stu-id="61ac0-110">The **Name** property of a **Recordset** object opened by using an SQL statement is the first 256 characters of the SQL statement.</span></span>

