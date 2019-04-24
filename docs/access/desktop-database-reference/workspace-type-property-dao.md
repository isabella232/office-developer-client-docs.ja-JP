---
title: Workspace プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e698963d60809e8d88c4ff87532fb7b74cff275c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311306"
---
# <a name="workspacetype-property-dao"></a><span data-ttu-id="5cc31-102">Workspace プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="5cc31-102">Workspace.Type property (DAO)</span></span>


<span data-ttu-id="5cc31-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cc31-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5cc31-p101">オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得のみ可能です。整数型 (**Integer**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5cc31-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cc31-106">構文</span><span class="sxs-lookup"><span data-stu-id="5cc31-106">Syntax</span></span>

<span data-ttu-id="5cc31-107">*式*。種類</span><span class="sxs-lookup"><span data-stu-id="5cc31-107">*expression* .Type</span></span>

<span data-ttu-id="5cc31-108">\*式\***Workspace**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="5cc31-108">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cc31-109">注釈</span><span class="sxs-lookup"><span data-stu-id="5cc31-109">Remarks</span></span>

<span data-ttu-id="5cc31-110">**Workspace** オブジェクトの場合、設定できる値と戻り値は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="5cc31-110">For a **Workspace** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cc31-111">定数</span><span class="sxs-lookup"><span data-stu-id="5cc31-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="5cc31-112">ワークスペースの種類</span><span class="sxs-lookup"><span data-stu-id="5cc31-112">Workspace type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cc31-113"><strong>dbusejet</strong></span><span class="sxs-lookup"><span data-stu-id="5cc31-113"><strong>dbUseJet</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc31-114"><strong>Workspace</strong> は Microsoft Access データベース エンジンに接続されます。</span><span class="sxs-lookup"><span data-stu-id="5cc31-114">The <strong>Workspace</strong> is connected to the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc31-115"><strong>dbUseODBC</strong></span><span class="sxs-lookup"><span data-stu-id="5cc31-115"><strong>dbUseODBC</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc31-116"><strong>Workspace</strong> は ODBC データ ソースに接続されます。</span><span class="sxs-lookup"><span data-stu-id="5cc31-116">The <strong>Workspace</strong> is connected to an ODBC data source.</span></span></p></td>
</tr>
</tbody>
</table>

