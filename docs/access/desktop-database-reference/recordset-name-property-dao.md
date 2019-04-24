---
title: Recordset.Name プロパティ (DAO)
TOCTitle: Name Property
ms:assetid: 2a80b994-a135-cd61-3906-17dfa0580110
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192067(v=office.15)
ms:contentKeyID: 48543910
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43f248ba529991190ae3d322a65a158bd9a4e6e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300380"
---
# <a name="recordsetname-property-dao"></a><span data-ttu-id="054b6-102">Recordset.Name プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="054b6-102">Recordset.Name property (DAO)</span></span>


<span data-ttu-id="054b6-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="054b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="054b6-104">指定したオブジェクトの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="054b6-104">Returns the name of the specified object.</span></span> <span data-ttu-id="054b6-105">読み取り専用 **文字列** です。</span><span class="sxs-lookup"><span data-stu-id="054b6-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="054b6-106">構文</span><span class="sxs-lookup"><span data-stu-id="054b6-106">Syntax</span></span>

<span data-ttu-id="054b6-107">*式*。拡張子</span><span class="sxs-lookup"><span data-stu-id="054b6-107">*expression* .Name</span></span>

<span data-ttu-id="054b6-108">\*式\***Recordset**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="054b6-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="054b6-109">注釈</span><span class="sxs-lookup"><span data-stu-id="054b6-109">Remarks</span></span>

<span data-ttu-id="054b6-110">SQL ステートメントを使用して開いた **Recordset** オブジェクトの **Name** プロパティには、SQL ステートメントの最初の 256 文字が設定されます。</span><span class="sxs-lookup"><span data-stu-id="054b6-110">The **Name** property of a **Recordset** object opened by using an SQL statement is the first 256 characters of the SQL statement.</span></span>

