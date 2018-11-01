---
title: QueryDef.Updatable プロパティ (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ad761c2941cb556ce67c9f716247663220f753f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873692"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="7c454-102">QueryDef.Updatable プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="7c454-102">QueryDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="7c454-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7c454-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7c454-p101">DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( **Boolean**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7c454-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c454-106">構文</span><span class="sxs-lookup"><span data-stu-id="7c454-106">Syntax</span></span>

<span data-ttu-id="7c454-107">*式*です。更新可能です</span><span class="sxs-lookup"><span data-stu-id="7c454-107">*expression* .Updatable</span></span>

<span data-ttu-id="7c454-108">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="7c454-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c454-109">注釈</span><span class="sxs-lookup"><span data-stu-id="7c454-109">Remarks</span></span>

<span data-ttu-id="7c454-110">クエリ結果の \*\*\*\*Recordset\*\*\*\* オブジェクトを更新できないときでも、クエリ定義を更新できる場合、 **QueryDef** オブジェクトの [Updatable](recordset-object-dao.md) プロパティは **True** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7c454-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

