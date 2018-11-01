---
title: TableDef.RecordCount プロパティ (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7ef77f5882f4b215764a82d343d59f1f31487e58
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886117"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="71d33-102">TableDef.RecordCount プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="71d33-102">TableDef.RecordCount Property (DAO)</span></span>


<span data-ttu-id="71d33-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="71d33-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="71d33-p101">**[TableDef](tabledef-object-dao.md)** オブジェクトの全レコード数を取得します。値の取得のみ可能です。長整数型 ( **Long**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="71d33-p101">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d33-106">構文</span><span class="sxs-lookup"><span data-stu-id="71d33-106">Syntax</span></span>

<span data-ttu-id="71d33-107">*式*です。RecordCount</span><span class="sxs-lookup"><span data-stu-id="71d33-107">*expression* .RecordCount</span></span>

<span data-ttu-id="71d33-108">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="71d33-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="71d33-109">注釈</span><span class="sxs-lookup"><span data-stu-id="71d33-109">Remarks</span></span>

<span data-ttu-id="71d33-110">レコードを持たない **Recordset** オブジェクトまたは **TableDef** オブジェクトでは、 **RecordCount** プロパティの設定値が 0 となります。</span><span class="sxs-lookup"><span data-stu-id="71d33-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="71d33-111">リンクされた **TableDef** オブジェクトを使用する場合、**RecordCount** プロパティの設定値は常に -1 となります。</span><span class="sxs-lookup"><span data-stu-id="71d33-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

